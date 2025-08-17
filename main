from flask import Flask, jsonify
import os
from datetime import datetime

app = Flask(__name__)

# Configuration Agitips
CHANNEL_ID = "UCS1m_ZhEAbQKfvIdAwoax2A"
GENESIS_DATE = "2020-11-16"

@app.route('/')
def home():
    return jsonify({
        "service": "YouTube Analytics V2",
        "status": "✅ RUNNING",
        "channel": "Agitips",
        "channel_id": CHANNEL_ID,
        "genesis_date": GENESIS_DATE,
        "timestamp": datetime.now().isoformat(),
        "version": "2.0-clean"
    })

@app.route('/health')
def health():
    return jsonify({
        "status": "healthy",
        "uptime": "OK"
    })

@app.route('/test')
def test():
    return jsonify({
        "message": "Test endpoint working",
        "ready_for": "YouTube API integration"
    })

if __name__ == '__main__':
    port = int(os.environ.get('PORT', 5000))
    app.run(host='0.0.0.0', port=port, debug=False)
