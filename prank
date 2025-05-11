using System;
using System.Windows.Forms;
using System.Drawing;

class PrankApp : Form
{
    public PrankApp()
    {
        // تنظیمات فرم
        this.Text = "Prank";
        this.WindowState = FormWindowState.Maximized;
        this.FormBorderStyle = FormBorderStyle.None;
        this.BackColor = Color.Red;
        this.DoubleBuffered = true;

        // لیبل متن
        Label label = new Label();
        label.Text = "آب حمام داغه، بیا لیف بزنیم!";
        label.Font = new Font("Arial", 48, FontStyle.Bold);
        label.ForeColor = Color.White;
        label.AutoSize = true;
        label.TextAlign = ContentAlignment.MiddleCenter;
        label.Location = new Point((this.Width - label.Width) / 2, (this.Height - label.Height) / 2);
        this.Controls.Add(label);

        // Timer برای بستن خودکار پس از 20 ثانیه
        Timer timer = new Timer();
        timer.Interval = 20000; // 20 ثانیه
        timer.Tick += (sender, e) => this.Close();
        timer.Start();

        // جلوگیری از بستن دستی
        this.FormClosing += (sender, e) =>
        {
            if (timer.Enabled)
                e.Cancel = true; // اجازه بستن نده تا زمانی که تایمر فعال است
        };
    }

    static void Main()
    {
        Application.EnableVisualStyles();
        Application.Run(new PrankApp());
    }
}
