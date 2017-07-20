# PokemonStatConversion

 public frmMain()
        {
            InitializeComponent();

            Random _r = new Random();
            const int CONST_minimum_value = 1;
            const int CONST_maximum_value = 11;
            int playerVal = 0;
            int remainTime;

        }
        private void btnDeal_Click(object sender, EventArgs e)
        {
             playerVal = _r.Next(CONST_minimum_value, CONST_maximum_value);
            playerValue.Text = playerVal.ToString();
            dealerValue.Text = "";
            btnDeal.Enabled = false;
       
        }
        private void btnHigher_Click(object sender, EventArgs e)
        {
            
           int dealerVa = _r.Next(CONST_minimum_value, CONST_maximum_value);
            
            dealerValue.Text = dealerVa.ToString();

            if (playerVal > dealerVa) {
                txtOutput.AppendText("Not a winner. Keep trying. Dealer's \n" + dealerVa + " is not higher than Player's \n" + playerVal + "\n");
               
                txtDealerSc.Text = (Convert.ToInt32(txtDealerSc.Text)+ 1).ToString();
                
                pnlPlayer.BackColor = Color.Red;
                pnlPlayer.ForeColor = Color.White;
            }
            else
            {
                txtOutput.AppendText("Winner: Dealer's \n" + dealerVa + " is higher than Player's \n" + playerVal + "\n");
                txtPlayerSc.Text = (Convert.ToInt32(txtPlayerSc.Text) + 1).ToString();
                pnlPlayer.BackColor = Color.Green;
                pnlPlayer.ForeColor = Color.White;

            }
            btnDeal.Enabled = true;
        }

        private void btnLower_Click(object sender, EventArgs e)
        {
            
            int dealerVa = _r.Next(CONST_minimum_value, CONST_maximum_value);
            dealerValue.Text = dealerVa.ToString();

            if (playerVal > dealerVa)
            {
                txtOutput.AppendText("Winner: Player's \n" + playerVal + " is higher than Dealer's \n" + dealerVa + "\n");
                txtPlayerSc.Text = (Convert.ToInt32(txtPlayerSc.Text) + 1).ToString();

                pnlPlayer.BackColor = Color.Green;
                pnlPlayer.ForeColor = Color.White;

            }
            else 
            {
                txtOutput.AppendText("Not a winner. Keep trying. Player's \n" + playerVal + " is not higher than Dealer's \n" + dealerVa + "\n");
                 txtDealerSc.Text = (Convert.ToInt32(txtDealerSc.Text) + 1).ToString();

                pnlPlayer.BackColor = Color.Red;
                pnlPlayer.ForeColor = Color.White;
            }
            btnDeal.Enabled = true;
        }
        

        private void textBox1_TextChanged_1(object sender, EventArgs e)
        {

        }

        private void btnClose_Click(object sender, EventArgs e)
        {
            this.Close();
        }

    }
