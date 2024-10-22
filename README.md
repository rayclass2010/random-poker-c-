# random-poker-c-
the easy poker game
 
    {
        public Form1()
        {
            InitializeComponent();
        }
        int poker, pc;
        Random random = new Random();
        Random pcs = new Random();

        
        private void button1_Click(object sender, EventArgs e)
        {
            timer1.Start();
            pc = pcs.Next(13);
            pictureBox1.Image = imageList1.Images[pc];

        }

        private void Form1_Load(object sender, EventArgs e)
        {
            label3.Text = "";
            timer1.Interval = 100;
            pictureBox2.SizeMode = PictureBoxSizeMode.StretchImage;
            pictureBox1.SizeMode = PictureBoxSizeMode.StretchImage;
        }

        private void button2_Click(object sender, EventArgs e)
        {
            timer1.Stop();

            if (poker > pc)
            {
                label3.Text = "win";
            }
            else if (poker < pc)
            {
                label3.Text = "gameover";
            }
            else
            {
                label3.Text = "draw";
            }
            
        }

        private void timer1_Tick(object sender, EventArgs e)
        {

            poker = random.Next(13);
            pictureBox2.Image = imageList1.Images[poker];
            
        }
    }
