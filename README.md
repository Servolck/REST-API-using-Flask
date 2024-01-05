# REST-API-using-Flask
Implements a simple REST API with Flask.
from flask import Flask, jsonify, request

app = Flask(__name__)

@app.route('/api/greet', methods=['POST'])
def greet():
    data = request.get_json()
    name = data['name']
    return jsonify({'message': f'Hello, {name}!'})

if __name__ == '__main__':
    app.run(debug=True)
