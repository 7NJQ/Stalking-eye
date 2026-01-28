require('dotenv').config();
const express = require('express');
const cors = require('cors');
const { createClient } = require('@supabase/supabase-js');

const app = express();
app.use(cors());
app.use(express.json());

const S_URL = process.env.SUPABASE_URL;
const S_KEY = process.env.SUPABASE_KEY;

const supabase = createClient(S_URL, S_KEY);

app.post('/login', async (req, res) => {
    try {
        const { data, error } = await supabase.auth.signInWithOAuth({
            provider: 'github',
            options: { redirectTo: process.env.REDIRECT_URL }
        });
        if (error) throw error;
        res.json(data);
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
});

app.post('/add-target', async (req, res) => {
    const { targetName, userId } = req.body;

    try {
        const { data, error } = await supabase.from('targets').insert([
            { target_name: targetName, github_user_id: userId, usernames: [targetName] }
        ]);
        if (error) throw error;
        res.json({ success: true, data });
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
});

const PORT = process.env.PORT || 5000;
app.listen(PORT, () => console.log(`الخادم يعمل على المنفذ ${PORT}`));