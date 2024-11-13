import requests

class CatalogoProductos:
    def __init__(self, api_url):
        self.api_url = api_url
        self.productos = []

    def obtener_productos(self):
        response = requests.get(self.api_url)
        if response.status_code == 200:
            self.productos = response.json()
        else:
            print("Error al obtener el catálogo")

    def mostrar_catalogo(self):
        for producto in self.productos:
            print(f"{producto['nombre']} - Precio: {producto['precio']}")

# Uso
catalogo = CatalogoProductos("https://api.example.com/catalogo")
catalogo.obtener_productos()
catalogo.mostrar_catalogo()
