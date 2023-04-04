# Distance-calculator
This calculates the distance based on time and speed. 

//Benjamin Glass
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace B_Glass_Coding_Assignment_March
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void label1_Click(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            //each variable represents its relative name in the assignment
            int speed;
            int hours;
            int distance;
            //tests to make sure if the number is valid and if it is, it will do the math and have the text output. 
            if (int.TryParse(textBox1.Text, out speed) && int.TryParse (textBox2.Text, out hours))
            { 
                for (int i = 1; i <= hours; i++) {
                    distance = speed * i;
                    textBox3.Text = i.ToString(" After hour " + i + " the vehicle traveled " + distance.ToString("n") + "miles");
                }
            }
            else
                textBox3.Text=("Please Enter a valid number ");
        }
    }
}
