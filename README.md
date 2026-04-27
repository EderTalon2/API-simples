from flask import Flask, jsonify

app = Flask(__name__)

@app.route('/')
def home():
    return jsonify({"mensagem": "API funcionando!"})

@app.route('/usuario/<nome>')
def usuario(nome):
    return jsonify({"usuario": nome})

if __name__ == '__main__':
    app.run(debug=True)
