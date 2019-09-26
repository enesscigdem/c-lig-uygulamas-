/// ARKADAŞLAR UYGULAMAMIZ 2 FORMDAN OLUŞMAKTADIR.DIKKAT EDINIZ.
FORM 1 DEKİ KULLANICI ADI- ADMİN ŞİFRE-12345
FORM1 ------------------------

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Futbol_ligi_oyunu
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Button1_Click(object sender, EventArgs e)
        {
            if(textBox1.Text=="admin" && textBox2.Text=="12345")
            {
                Form2 yeni = new Form2();
                yeni.Show();
                this.Hide();
            }
            else
            {
                MessageBox.Show("Hatalı giriş yaptınız.");
                textBox1.Clear();
                textBox2.Clear();
            }
        }

        private void Button2_Click(object sender, EventArgs e)
        {
            Form2 yeni = new Form2();
            yeni.Show();
            this.Hide();
        }
    }
}

FORM 2 --------------------------------------------------------------------------




using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace Futbol_ligi_oyunu
{
    public partial class Form2 : Form
    {
        public Form2()
        {
            InitializeComponent();
        }

        private void Button1_Click(object sender, EventArgs e)
        {
            Random rastgele = new Random();
            int a = rastgele.Next(0, 4);
            int b = rastgele.Next(0, 4);
            int c = rastgele.Next(0, 4);
            int d = rastgele.Next(0, 4);
            label3.Text = a.ToString();
            label2.Text = b.ToString();
            label10.Text = c.ToString();
            label8.Text = d.ToString();
            
            if(Convert.ToInt32(label3.Text)>Convert.ToInt32(label2.Text))
            {
                int sayi = 0;
                sayi = sayi + 3;
                label15.Text = sayi.ToString();
            }


            if (Convert.ToInt32(label3.Text) == Convert.ToInt32(label2.Text))
            {
                int sayi = 0;
                sayi = sayi + 1;
                label15.Text = sayi.ToString();
                label16.Text = sayi.ToString();

            }
            if (Convert.ToInt32(label2.Text) > Convert.ToInt32(label3.Text))
            {
                int sayi = 0;
                sayi = sayi + 3;
                label16.Text = sayi.ToString();

            }

            if (Convert.ToInt32(label10.Text) > Convert.ToInt32(label8.Text))
            {
                int sayi = 0;
                sayi = sayi + 3;
                label17.Text = sayi.ToString();
            }


            if (Convert.ToInt32(label10.Text) == Convert.ToInt32(label8.Text))
            {
                int sayi = 0;
                sayi = sayi + 1;
                label17.Text = sayi.ToString();
                label18.Text = sayi.ToString();

            }
            if (Convert.ToInt32(label10.Text) < Convert.ToInt32(label8.Text))
            {
                int sayi = 0;
                sayi = sayi + 3;
                label18.Text = sayi.ToString();

            }





        }

        private void Button2_Click(object sender, EventArgs e)
        {


            Random rastgele2 = new Random();
            int x = rastgele2.Next(0, 4);
            int y = rastgele2.Next(0, 4);
            int z = rastgele2.Next(0, 4);
            int t = rastgele2.Next(0, 4);
            label28.Text = x.ToString();
            label26.Text = y.ToString();
            label23.Text = z.ToString();
            label21.Text = t.ToString();


            if (Convert.ToInt32(label28.Text)>Convert.ToInt32(label26.Text))
            {
                int sayi2 = Convert.ToInt32(label15.Text);
                sayi2 = sayi2 + 3;
                label15.Text = sayi2.ToString();
            }
            if (Convert.ToInt32(label28.Text) == Convert.ToInt32(label26.Text))
            {
                int a = Convert.ToInt32(label15.Text);
                int b = Convert.ToInt32(label17.Text);
                a = a + 1;
                b = b + 1;
                label15.Text = a.ToString();
                label17.Text = b.ToString();

            }

            if (Convert.ToInt32(label26.Text) > Convert.ToInt32(label28.Text))
            {
                int sayi2 = Convert.ToInt32(label17.Text);
                sayi2 = sayi2 + 3;
                label17.Text = sayi2.ToString();
            }
            if(Convert.ToInt32(label23.Text)>Convert.ToInt32(label21.Text))
            {
                int c = Convert.ToInt32(label16.Text);
                c = c + 3;
                label16.Text = c.ToString();
            }
            if(Convert.ToInt32(label23.Text)==Convert.ToInt32(label21.Text))
            {
                int l = Convert.ToInt32(label16.Text);
                int ş = Convert.ToInt32(label18.Text);
                l = l + 1;
                ş = ş + 1;
                label16.Text = l.ToString();
                label18.Text = ş.ToString();
            }
            if(Convert.ToInt32(label21.Text)>Convert.ToInt32(label23.Text))
            {
                int k = Convert.ToInt32(label18.Text);
                k = k + 3;
                label18.Text = k.ToString();
            }

        }

        private void Button3_Click(object sender, EventArgs e)
        {
            Random rastgele2 = new Random();
            int x = rastgele2.Next(0, 4);
            int y = rastgele2.Next(0, 4);
            int z = rastgele2.Next(0, 4);
            int t = rastgele2.Next(0, 4);
            label38.Text = x.ToString();
            label36.Text = y.ToString();
            label33.Text = z.ToString();
            label31.Text = t.ToString();

            if(Convert.ToInt32(label38.Text)>Convert.ToInt32(label36.Text))
            {
                int a = Convert.ToInt32(label16.Text);
                a = a + 3;
                label16.Text = a.ToString();
            }
            if(Convert.ToInt32(label38.Text)==Convert.ToInt32(label36.Text))
            {
                int l = Convert.ToInt32(label16.Text);
                int ş = Convert.ToInt32(label17.Text);
                l = l + 1;
                ş = ş + 1;
                label16.Text = l.ToString();
                label17.Text = ş.ToString();

            }
            if (Convert.ToInt32(label36.Text) > Convert.ToInt32(label38.Text))
            {
                int k = Convert.ToInt32(label17.Text);
                k = k + 3;
                label17.Text = k.ToString();
            }
            if (Convert.ToInt32(label33.Text) > Convert.ToInt32(label31.Text))
            {
                int a = Convert.ToInt32(label16.Text);
                a = a + 3;
                label18.Text = a.ToString();
            }
             if(Convert.ToInt32(label33.Text)==Convert.ToInt32(label31.Text))
            {
                int l = Convert.ToInt32(label15.Text);
                int ş = Convert.ToInt32(label18.Text);
                l = l + 1;
                ş = ş + 1;
                label15.Text = l.ToString();
                label18.Text = ş.ToString();

            }
            if (Convert.ToInt32(label31.Text) > Convert.ToInt32(label33.Text))
            {
                int k = Convert.ToInt32(label15.Text);
                k = k + 3;
                label15.Text = k.ToString();
            }
            if(Convert.ToInt32(label15.Text)>Convert.ToInt32(label16.Text) && Convert.ToInt32(label15.Text)>Convert.ToInt32(label17.Text)&& Convert.ToInt32(label15.Text)>Convert.ToInt32(label18.Text))
            {
                label39.Text = "ŞAMPİYON GALATASARAY";
            }
            if (Convert.ToInt32(label16.Text) > Convert.ToInt32(label15.Text) && Convert.ToInt32(label16.Text) > Convert.ToInt32(label17.Text) && Convert.ToInt32(label16.Text) > Convert.ToInt32(label18.Text))
            {
                label39.Text = "ŞAMPİYON FENERBAHÇE";
            }
            if (Convert.ToInt32(label17.Text) > Convert.ToInt32(label16.Text) && Convert.ToInt32(label17.Text) > Convert.ToInt32(label18.Text) && Convert.ToInt32(label17.Text) > Convert.ToInt32(label15.Text))
            {
                label39.Text = "ŞAMPİYON BEŞİKTAŞ";
            }
            if (Convert.ToInt32(label18.Text) > Convert.ToInt32(label16.Text) && Convert.ToInt32(label18.Text) > Convert.ToInt32(label17.Text) && Convert.ToInt32(label18.Text) > Convert.ToInt32(label15.Text))
            {
                label39.Text = "ŞAMPİYON TRABZONSPOR";
            }







        }
    }
}
