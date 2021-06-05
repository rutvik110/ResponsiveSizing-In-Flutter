# ResponsiveSizing-In-Flutter

```
class Sizescaleconfig {
  static final double refrenceheight = 715.0;
  static final double referencewidth = 320.0;
  static double screenheight;
  static double screenwidth;
  static double heightscaleratio;
  static double widthscaleratio;
  static double textscalefactor;

  static void calculaterscaleratio() {
    heightscaleratio = screenheight / refrenceheight;
    widthscaleratio = screenwidth / referencewidth;
  }

  static double scalehightfactor(double actualheight) {
    return actualheight * heightscaleratio;
  }

  static double scalewidthfactor(double actualwidth) {
    return actualwidth * widthscaleratio;
  }

  static double scaletextfactor(double actualfontsize) {
    return actualfontsize * heightscaleratio * textscalefactor;
  }
}

void setsizescaleconfig(double screenheight, double screenwidth, double textscalefactor) {
  Sizescaleconfig.screenheight = screenheight;
  Sizescaleconfig.screenwidth = screenwidth;
  Sizescaleconfig.textscalefactor = textscalefactor;

  Sizescaleconfig.calculaterscaleratio();
}

```
