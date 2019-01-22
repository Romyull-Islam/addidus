#include<windows.h>
#include<GL/glut.h>


void display(void)
{
    glClear(GL_COLOR_BUFFER_BIT);

   ///addidus
    glBegin(GL_POLYGON);
     glColor3f (0.0, 0.0, 0.0);

     glVertex2f (2,2);
     glVertex2f (4.2,2);
     glVertex2f (3.4,3.4);
     glVertex2f (1.75,2.45);
    glEnd();

    glBegin(GL_POLYGON);
     glColor3f (0.0, 0.0, 0.0);
     glVertex2f (5,2);
     glVertex2f (7.2,2);
     glVertex2f (5.3,5.15);
     glVertex2f (3.75,4.2);
    glEnd();

     glBegin(GL_POLYGON);
     glColor3f (0.0, 0.0, 0.0);
     glVertex2f (8,2);
     glVertex2f (10.2,2);
     glVertex2f (7.2,6.7);
     glVertex2f (5.7,5.8);
    glEnd();


    glFlush ();

}

void init(void)
{
    glClearColor(1.0,1.0,1.0,0.0);
    glMatrixMode(GL_PROJECTION);
    glLoadIdentity();
    glOrtho(0.0,20.0,0.0,12.0,0,50); //graph matrix


}
int main(int argc, char** argv)
{
    glutInit(&argc, argv);
    glutInitDisplayMode (GLUT_SINGLE | GLUT_RGB);
    glutInitWindowSize (1000, 600); //display size
    glutInitWindowPosition (10, 10);
    glutCreateWindow ("1");
    init ();
    glutDisplayFunc(display);
    glutMainLoop();
    return 0;
}

