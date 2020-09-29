#include <iostream>

using namespace std;

class Forma{
  public:
  double perimetro;
  double area;

  Forma() {}
  double devolverArea() {
  cout << "El área de la figura es: " << area << endl;
  return area;
  }

  double devolverPerimetro() {
  cout << "El perimetro de la figura es: " << perimetro << endl;
  return perimetro;
  }
};

class CTriangulo : public Forma{
protected:
double base;
double altura;

double lado1;
double lado2;
double lado3;

public:
CTriangulo(double _base, double _altura, double _lado1, double _lado2, double _lado3) : base(_base), altura(_altura), lado1(_lado1), lado2(_lado2), lado3(_lado3) {}

double calcularArea(){
double a = (base*altura);
area = a/2;
return area;
}

double calcularPerimetro(){
perimetro = lado1 + lado2 + lado3;
return perimetro;
}

};

class CCuadrado : public Forma {

 protected:
 double ladoc;

 public:
  CCuadrado(double _ladoc) : ladoc(_ladoc) {}
  
  double areacuadrado()
  {
     area = ladoc * ladoc;
     return area;
  }

  double perimetrocuadrado()
  {
    perimetro = ladoc * 4;
    return perimetro;
  }

};

class Crectangulo : public Forma 
{
  protected:
  double base;
  double altura;

  public:
  Crectangulo(double _base, double _altura) :  base(_base), altura(_altura) {}
   
   double arearectangulo()
   {
     area = base * altura;
     return area;
   }
   
  double perimetrorectangulo()
   {
     perimetro = 2 * base + 2 * altura;
     return perimetro;
   }

};

class Crombo : public Forma 
{
  protected:
  double dmenor;
  double dmayor;
  double lado;

  public:
Crombo(double _dmenor, double _dmayor, double _lado) : 
dmenor(_dmenor), dmayor(_dmayor), lado(_lado) {}

double arearombo()
{
  area = dmenor * dmayor / 2;
  return area;
}

double perimetrorombo()
{
  perimetro = lado * 4;
  return perimetro;
}

};

class Cromboide : public Forma 
{
  protected:
  double base;
  double altura;

  public:
  Cromboide(double _base, double _altura) :  base(_base), altura(_altura) {}
   
   double arearomboide()
   {
     area = base * altura;
     return area;
   }
   
  double perimetroromboide()
   {
     perimetro = 2 * base + 2 * altura;
     return perimetro;
   }

};

class Ctrapecio : public Forma
{
  protected:
double basemenor;
double basemayor;
double altura;

double lado1;
double lado2;
double lado3;
double lado4;

public:
Ctrapecio (double _basemenor, double _basemayor, double _altura, double _lado1, double _lado2, double _lado3, double _lado4) : basemenor(_basemenor), basemayor(_basemayor), altura(_altura), lado1(_lado1), lado2(_lado2), lado3(_lado3), lado4(_lado4) {}

double areatrapecio()
{
  area = altura * (basemayor + basemenor) / 2;
  return area;
}

double Perimetrotrapecio(){
perimetro = lado1 + lado2 + lado3 + lado4;
return perimetro;
}

};

int main() {
 CTriangulo triangulo(5,10,5,7,10);
 CCuadrado cuadrado(10);
 Crectangulo rectangulo(10, 20);
 Crombo rombo(10,10,15);
 Cromboide romboide(10, 20);
 Ctrapecio trapecio(10,15,10,5,5,5,5);

 cout << " -- Triángulo -- " << endl;
 triangulo.calcularArea();
 triangulo.calcularPerimetro();
 triangulo.devolverPerimetro();
 triangulo.devolverArea();
 cout << endl;
 cout << " -- Cuadrado-- " << endl;
 cuadrado.areacuadrado();
 cuadrado.perimetrocuadrado();
 cuadrado.devolverPerimetro();
 cuadrado.devolverArea();
 cout << endl;
 cout << " -- Rectángulo -- " << endl;
 rectangulo.arearectangulo();
 rectangulo.perimetrorectangulo();
 rectangulo.devolverPerimetro();
 rectangulo.devolverArea();
 cout << endl;
 cout << " -- Rombo -- " << endl;
 rombo.arearombo();
 rombo.perimetrorombo();
 rombo.devolverPerimetro();
 rombo.devolverArea();
 cout << endl;
 cout << " -- Romboide -- " << endl;
 romboide.arearomboide();
 romboide.perimetroromboide();
 romboide.devolverPerimetro();
 romboide.devolverArea();
cout << endl;
 cout << " -- Trapecio -- " << endl;
 trapecio.areatrapecio();
 trapecio.Perimetrotrapecio();
 trapecio.devolverPerimetro();
 trapecio.devolverArea();


 return 0;
}
