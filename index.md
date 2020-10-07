## Welcome to Skadezy's GPC Page


Slide Cancel V3:

```markdown
int slide_enable = FALSE;



// Main
main {

if((get_val(PS4_LY) < -60) || (get_val(PS4_LY) > 60) || (get_val(PS4_LX) < -60) || (get_val(PS4_LX) > 60)) {
 
if(get_rumble(RUMBLE_A) == 87) { slide_enable = TRUE } // Detects that the slide has started
if(get_rumble(RUMBLE_A) == 0) { slide_enable = FALSE } // Detects that the slide has stopped

if(slide_enable) {
if(event_release (PS4_CIRCLE)){ combo_run(ASC) }
}
  }
	}
// Combo section	
combo ASC { 
wait(20); 
set_val(PS4_CIRCLE, 100);
wait(20); 
set_val(PS4_CIRCLE, 100);
set_val(PS4_CROSS, 100);
wait(20);
set_val(PS4_CIRCLE, 0);
set_val(PS4_CROSS, 100);
wait(20);
set_val(PS4_CROSS, 0);
}
```

