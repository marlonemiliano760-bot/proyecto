# marlon
from flask import Flask, render_template

app = Flask(__name__)


@app.route("/")
def inicio():
    return render_template("index.html")


@app.route("/productos")
def productos():
    return render_template("productos.html")


@app.route("/clientes")
def clientes():
    return render_template("clientes.html")


@app.route("/proveedores")
def proveedores():
    return render_template("proveedores.html")


@app.route("/facturacion")
def facturacion():
    return render_template("facturacion.html")


if __name__ == "__main__":
    app.run(debug=True)
    <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>{% block title %}Proyecto Integrador{% endblock %}</title>

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
          rel="stylesheet">

    <link rel="stylesheet"
          href="{{ url_for('static', filename='css/style.css') }}">
</head>

<body>

    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
        <div class="container">
            <a class="navbar-brand" href="{{ url_for('inicio') }}">
                Mi Proyecto
            </a>

            <button class="navbar-toggler"
                    type="button"
                    data-bs-toggle="collapse"
                    data-bs-target="#menu">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="menu">
                <ul class="navbar-nav ms-auto">

                    <li class="nav-item">
                        <a class="nav-link" href="{{ url_for('inicio') }}">
                            Inicio
                        </a>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link" href="{{ url_for('productos') }}">
                            Productos
                        </a>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link" href="{{ url_for('clientes') }}">
                            Clientes
                        </a>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link" href="{{ url_for('proveedores') }}">
                            Proveedores
                        </a>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link" href="{{ url_for('facturacion') }}">
                            Facturación
                        </a>
                    </li>

                </ul>
            </div>
        </div>
    </nav>

    <main class="container py-4">

        {% block content %}
        {% endblock %}

    </main>

    <footer class="bg-dark text-white text-center py-3 mt-5">
        <p class="mb-0">
            Proyecto Integrador &copy; 2026
        </p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js">
    </script>

    <script src="{{ url_for('static', filename='js/script.js') }}">
    </script>

</body>
</html>
{% extends "base.html" %}

{% block title %}Inicio{% endblock %}

{% block content %}

<div class="p-5 mb-4 bg-light rounded-3">
    <div class="container-fluid py-4">
        <h1 class="display-5 fw-bold">
            Bienvenidos a nuestro proyecto
        </h1>

        <p class="fs-5">
            Sistema web desarrollado como parte del Proyecto Integrador.
        </p>

        <a href="{{ url_for('productos') }}" class="btn btn-primary">
            Ver productos
        </a>
    </div>
</div>

<div class="row">

    <div class="col-md-4 mb-3">
        <div class="card h-100">
            <div class="card-body">
                <h5 class="card-title">Productos</h5>
                <p class="card-text">
                    Consulta los productos disponibles.
                </p>
                <a href="{{ url_for('productos') }}"
                   class="btn btn-primary">
                    Ver productos
                </a>
            </div>
        </div>
    </div>

    <div class="col-md-4 mb-3">
        <div class="card h-100">
            <div class="card-body">
                <h5 class="card-title">Clientes</h5>
                <p class="card-text">
                    Información de los clientes registrados.
                </p>
                <a href="{{ url_for('clientes') }}"
                   class="btn btn-primary">
                    Ver clientes
                </a>
            </div>
        </div>
    </div>

    <div class="col-md-4 mb-3">
        <div class="card h-100">
            <div class="card-body">
                <h5 class="card-title">Facturación</h5>
                <p class="card-text">
                    Consulta las facturas del sistema.
                </p>
                <a href="{{ url_for('facturacion') }}"
                   class="btn btn-primary">
                    Ver facturación
                </a>
            </div>
        </div>
    </div>

</div>

{% endblock %}
{% extends "base.html" %}

{% block title %}Productos{% endblock %}

{% block content %}

<h1 class="mb-4">Productos</h1>

<div class="row">

    <div class="col-md-4 mb-4">
        <div class="card h-100">
            <div class="card-body">
                <h5 class="card-title">Producto 1</h5>
                <p class="card-text">Producto de demostración.</p>
                <p><strong>Precio:</strong> $25.00</p>
                <button class="btn btn-success">
                    Ver producto
                </button>
            </div>
        </div>
    </div>

    <div class="col-md-4 mb-4">
        <div class="card h-100">
            <div class="card-body">
                <h5 class="card-title">Producto 2</h5>
                <p class="card-text">Producto de demostración.</p>
                <p><strong>Precio:</strong> $35.00</p>
                <button class="btn btn-success">
                    Ver producto
                </button>
            </div>
        </div>
    </div>

</div>

{% endblock %}
body {
    background-color: #f5f6f8;
}

.card {
    transition: transform 0.2s;
}

.card:hover {
    transform: translateY(-5px);
}

footer {
    margin-top: 50px;
}
console.log("Aplicación Flask cargada correctamente.");

document.addEventListener("DOMContentLoaded", function () {
    console.log("Documento cargado.");
});


from flask import Flask, render_template_string

app = Flask(__name__)

# ==========================================================
# DATOS DEL PROYECTO
# ==========================================================

nombre_empresa = "Ferretería El Constructor"

informacion = {
    "direccion": "Av. Principal y Calle 10",
    "telefono": "0991234567",
    "email": "info@elconstructor.com"
}

productos = [
    {
        "id": 1,
        "nombre": "Martillo",
        "categoria": "Herramientas",
        "precio": 8.50,
        "stock": 10
    },
    {
        "id": 2,
        "nombre": "Taladro",
        "categoria": "Herramientas eléctricas",
        "precio": 75.00,
        "stock": 5
    },
    {
        "id": 3,
        "nombre": "Destornillador",
        "categoria": "Herramientas",
        "precio": 4.50,
        "stock": 0
    },
    {
        "id": 4,
        "nombre": "Cemento",
        "categoria": "Construcción",
        "precio": 7.25,
        "stock": 20
    },
    {
        "id": 5,
        "nombre": "Pintura",
        "categoria": "Pinturas",
        "precio": 18.00,
        "stock": 8
    },
    {
        "id": 6,
        "nombre": "Brocha",
        "categoria": "Pinturas",
        "precio": 3.50,
        "stock": 0
    }
]

clientes = [
    {
        "id": 1,
        "nombre": "Juan Pérez",
        "telefono": "0991234567",
        "ciudad": "Guayaquil"
    },
    {
        "id": 2,
        "nombre": "María López",
        "telefono": "0987654321",
        "ciudad": "Machala"
    },
    {
        "id": 3,
        "nombre": "Carlos Sánchez",
        "telefono": "0974561238",
        "ciudad": "Huaquillas"
    },
    {
        "id": 4,
        "nombre": "Ana Torres",
        "telefono": "0963214567",
        "ciudad": "Guayaquil"
    }
]

proveedores = [
    {
        "id": 1,
        "empresa": "FerreMateriales S.A.",
        "contacto": "Pedro Gómez",
        "telefono": "0991112233",
        "estado": "Activo"
    },
    {
        "id": 2,
        "empresa": "ConstruMarket",
        "contacto": "Laura Ruiz",
        "telefono": "0982223344",
        "estado": "Activo"
    },
    {
        "id": 3,
        "empresa": "Herramientas del Sur",
        "contacto": "Miguel Castro",
        "telefono": "0973334455",
        "estado": "Inactivo"
    }
]

facturas = [
    {
        "numero": "FAC-001",
        "cliente": "Juan Pérez",
        "fecha": "20/08/2026",
        "total": 125.50,
        "estado": "Pagada"
    },
    {
        "numero": "FAC-002",
        "cliente": "María López",
        "fecha": "21/08/2026",
        "total": 85.75,
        "estado": "Pendiente"
    },
    {
        "numero": "FAC-003",
        "cliente": "Carlos Sánchez",
        "fecha": "22/08/2026",
        "total": 210.00,
        "estado": "Pagada"
    },
    {
        "numero": "FAC-004",
        "cliente": "Ana Torres",
        "fecha": "23/08/2026",
        "total": 65.25,
        "estado": "Pendiente"
    }
]


# ==========================================================
# PLANTILLA HTML COMPLETA
# ==========================================================

HTML = """
<!DOCTYPE html>
<html lang="es">

<head>

    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <title>{{ titulo }} - Ferretería El Constructor</title>

    <link
        href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
        rel="stylesheet">

    <style>

        body {
            background-color: #f4f6f9;
            min-height: 100vh;
        }

        .navbar-brand {
            font-weight: bold;
        }

        .card {
            border: none;
            border-radius: 12px;
        }

        .card:hover {
            transform: translateY(-3px);
            transition: 0.2s;
        }

        footer {
            margin-top: 60px;
        }

    </style>

</head>


<body>


<!-- ======================================================
     NAVBAR
======================================================= -->

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">

    <div class="container">

        <a class="navbar-brand"
           href="/">
            El Constructor
        </a>

        <button
            class="navbar-toggler"
            data-bs-toggle="collapse"
            data-bs-target="#menu">

            <span class="navbar-toggler-icon"></span>

        </button>

        <div
            class="collapse navbar-collapse"
            id="menu">

            <ul class="navbar-nav ms-auto">

                <li class="nav-item">

                    <a class="nav-link"
                       href="/">
                        Inicio
                    </a>

                </li>

                <li class="nav-item">

                    <a class="nav-link"
                       href="/productos">
                        Productos
                    </a>

                </li>

                <li class="nav-item">

                    <a class="nav-link"
                       href="/clientes">
                        Clientes
                    </a>

                </li>

                <li class="nav-item">

                    <a class="nav-link"
                       href="/proveedores">
                        Proveedores
                    </a>

                </li>

                <li class="nav-item">

                    <a class="nav-link"
                       href="/facturacion">
                        Facturación
                    </a>

                </li>

            </ul>

        </div>

    </div>

</nav>


<!-- ======================================================
     CONTENIDO
======================================================= -->

<div class="container py-5">


{% if pagina == "inicio" %}


    <!-- ================= INICIO ================= -->

    <div class="text-center mb-5">

        <h1 class="display-5 fw-bold">

            {{ nombre_empresa }}

        </h1>

        <p class="lead">

            Sistema de gestión comercial

        </p>

        <p>

            Bienvenido a
            <strong>{{ nombre_empresa|upper }}</strong>

        </p>

    </div>


    <div class="row g-4">


        <div class="col-md-3">

            <div class="card shadow text-center">

                <div class="card-body">

                    <h5>Productos</h5>

                    <h2>
                        {{ productos|length }}
                    </h2>

                </div>

            </div>

        </div>


        <div class="col-md-3">

            <div class="card shadow text-center">

                <div class="card-body">

                    <h5>Clientes</h5>

                    <h2>
                        {{ clientes|length }}
                    </h2>

                </div>

            </div>

        </div>


        <div class="col-md-3">

            <div class="card shadow text-center">

                <div class="card-body">

                    <h5>Proveedores</h5>

                    <h2>
                        {{ proveedores|length }}
                    </h2>

                </div>

            </div>

        </div>


        <div class="col-md-3">

            <div class="card shadow text-center">

                <div class="card-body">

                    <h5>Facturas</h5>

                    <h2>
                        {{ facturas|length }}
                    </h2>

                </div>

            </div>

        </div>

    </div>


    <div class="card shadow mt-5">

        <div class="card-body">

            <h3>
                Información de contacto
            </h3>

            <p>
                <strong>Dirección:</strong>
                {{ informacion.direccion }}
            </p>

            <p>
                <strong>Teléfono:</strong>
                {{ informacion.telefono }}
            </p>

            <p>
                <strong>Correo:</strong>
                {{ informacion.email }}
            </p>

        </div>

    </div>


{% elif pagina == "productos" %}


    <!-- ================= PRODUCTOS ================= -->

    <h1 class="mb-4">
        Productos
    </h1>


    <div class="row g-4">


        {% for producto in productos %}


        <div class="col-md-4">


            <div class="card shadow h-100">

                <div class="card-body">


                    <span class="badge bg-secondary">

                        {{ producto.categoria }}

                    </span>


                    <h4 class="mt-3">

                        {{ producto.nombre|upper }}

                    </h4>


                    <p>

                        <strong>Precio:</strong>

                        ${{ "%.2f"|format(producto.precio) }}

                    </p>


                    <p>

                        <strong>Stock:</strong>

                        {{ producto.stock }}

                    </p>


                    {% if producto.stock > 0 %}

                        <span class="badge bg-success">

                            Disponible

                        </span>

                    {% else %}

                        <span class="badge bg-danger">

                            Agotado

                        </span>

                    {% endif %}


                </div>

            </div>


        </div>


        {% endfor %}


    </div>


{% elif pagina == "clientes" %}


    <!-- ================= CLIENTES ================= -->

    <h1 class="mb-4">
        Clientes
    </h1>


    <div class="table-responsive">


        <table class="table table-striped table-hover shadow-sm">


            <thead class="table-dark">

                <tr>

                    <th>ID</th>
                    <th>Nombre</th>
                    <th>Teléfono</th>
                    <th>Ciudad</th>

                </tr>

            </thead>


            <tbody>


                {% for cliente in clientes %}

                <tr>

                    <td>
                        {{ cliente.id }}
                    </td>

                    <td>
                        {{ cliente.nombre }}
                    </td>

                    <td>
                        {{ cliente.telefono }}
                    </td>

                    <td>
                        {{ cliente.ciudad }}
                    </td>

                </tr>

                {% endfor %}


            </tbody>

        </table>


    </div>


    {% if clientes %}

        <div class="alert alert-success">

            Se encontraron
            {{ clientes|length }}
            clientes registrados.

        </div>

    {% else %}

        <div class="alert alert-warning">

            No existen clientes registrados.

        </div>

    {% endif %}


{% elif pagina == "proveedores" %}


    <!-- ================= PROVEEDORES ================= -->

    <h1 class="mb-4">
        Proveedores
    </h1>


    <div class="row g-4">


        {% for proveedor in proveedores %}


        <div class="col-md-4">


            <div class="card shadow h-100">

                <div class="card-body">

                    <h5>

                        {{ proveedor.empresa }}

                    </h5>

                    <hr>

                    <p>

                        <strong>Contacto:</strong>

                        {{ proveedor.contacto }}

                    </p>

                    <p>

                        <strong>Teléfono:</strong>

                        {{ proveedor.telefono }}

                    </p>


                    {% if proveedor.estado == "Activo" %}

                        <span class="badge bg-success">

                            Proveedor activo

                        </span>

                    {% else %}

                        <span class="badge bg-danger">

                            Proveedor inactivo

                        </span>

                    {% endif %}


                </div>

            </div>


        </div>


        {% endfor %}


    </div>


{% elif pagina == "facturacion" %}


    <!-- ================= FACTURACIÓN ================= -->

    <h1 class="mb-4">
        Facturación
    </h1>


    <div class="table-responsive">


        <table class="table table-bordered table-hover shadow-sm">


            <thead class="table-dark">

                <tr>

                    <th>Número</th>
                    <th>Cliente</th>
                    <th>Fecha</th>
                    <th>Total</th>
                    <th>Estado</th>

                </tr>

            </thead>


            <tbody>


                {% for factura in facturas %}


                <tr>

                    <td>

                        {{ factura.numero }}

                    </td>

                    <td>

                        {{ factura.cliente }}

                    </td>

                    <td>

                        {{ factura.fecha }}

                    </td>

                    <td>

                        ${{ "%.2f"|format(factura.total) }}

                    </td>

                    <td>


                        {% if factura.estado == "Pagada" %}

                            <span class="badge bg-success">

                                Pagada

                            </span>

                        {% else %}

                            <span class="badge bg-warning text-dark">

                                Pendiente

                            </span>

                        {% endif %}


                    </td>

                </tr>


                {% endfor %}


            </tbody>


        </table>


    </div>


{% endif %}


</div>


<!-- ======================================================
     FOOTER
======================================================= -->

<footer class="bg-dark text-white text-center py-4">

    <p class="mb-1">

        © 2026 Ferretería El Constructor

    </p>

    <small>

        Proyecto Integrador - Flask y Jinja2

    </small>

</footer>


<script
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js">
</script>


</body>

</html>
"""


# ==========================================================
# RUTAS
# ==========================================================

@app.route("/")
def index():

    return render_template_string(
        HTML,
        titulo="Inicio",
        pagina="inicio",
        nombre_empresa=nombre_empresa,
        informacion=informacion,
        productos=productos,
        clientes=clientes,
        proveedores=proveedores,
        facturas=facturas
    )


@app.route("/productos")
def ver_productos():

    return render_template_string(
        HTML,
        titulo="Productos",
        pagina="productos",
        productos=productos
    )


@app.route("/clientes")
def ver_clientes():

    return render_template_string(
        HTML,
        titulo="Clientes",
        pagina="clientes",
        clientes=clientes
    )


@app.route("/proveedores")
def ver_proveedores():

    return render_template_string(
        HTML,
        titulo="Proveedores",
        pagina="proveedores",
        proveedores=proveedores
    )


@app.route("/facturacion")
def ver_facturacion():

    return render_template_string(
        HTML,
        titulo="Facturación",
        pagina="facturacion",
        facturas=facturas
    )


# ==========================================================
# EJECUTAR APLICAC

# =========================
# ARCHIVO: app.py
# =========================

from flask import Flask, render_template, redirect, url_for, flash

from forms.producto_form import ProductoForm
from forms.cliente_form import ClienteForm
from forms.proveedor_form import ProveedorForm
from forms.facturacion_form import FacturacionForm

app = Flask(__name__)

# Clave necesaria para Flask-WTF y protección CSRF
app.config["SECRET_KEY"] = "clave-secreta-proyecto-integrador-2026"

# Datos temporales. No se utiliza base de datos en esta semana.
productos = []
clientes = []
proveedores = []
facturas = []


# =========================
# INICIO
# =========================

@app.route("/")
def index():
    return render_template(
        "index.html",
        productos=productos,
        clientes=clientes,
        proveedores=proveedores,
        facturas=facturas
    )


# =========================
# PRODUCTOS
# =========================

@app.route("/productos")
def productos_lista():
    return render_template(
        "productos.html",
        productos=productos
    )


@app.route("/productos/nuevo", methods=["GET", "POST"])
def nuevo_producto():

    form = ProductoForm()

    if form.validate_on_submit():

        producto = {
            "nombre": form.nombre.data,
            "descripcion": form.descripcion.data,
            "precio": form.precio.data,
            "stock": form.stock.data
        }

        productos.append(producto)

        flash(
            "Producto registrado correctamente.",
            "success"
        )

        return redirect(url_for("productos_lista"))

    return render_template(
        "formulario_producto.html",
        form=form
    )


# =========================
# CLIENTES
# =========================

@app.route("/clientes")
def clientes_lista():
    return render_template(
        "clientes.html",
        clientes=clientes
    )


@app.route("/clientes/nuevo", methods=["GET", "POST"])
def nuevo_cliente():

    form = ClienteForm()

    if form.validate_on_submit():

        cliente = {
            "nombre": form.nombre.data,
            "email": form.email.data,
            "telefono": form.telefono.data,
            "direccion": form.direccion.data
        }

        clientes.append(cliente)

        flash(
            "Cliente registrado correctamente.",
            "success"
        )

        return redirect(url_for("clientes_lista"))

    return render_template(
        "formulario_cliente.html",
        form=form
    )


# =========================
# PROVEEDORES
# =========================

@app.route("/proveedores")
def proveedores_lista():
    return render_template(
        "proveedores.html",
        proveedores=proveedores
    )


@app.route("/proveedores/nuevo", methods=["GET", "POST"])
def nuevo_proveedor():

    form = ProveedorForm()

    if form.validate_on_submit():

        proveedor = {
            "empresa": form.empresa.data,
            "contacto": form.contacto.data,
            "email": form.email.data,
            "telefono": form.telefono.data,
            "direccion": form.direccion.data
        }

        proveedores.append(proveedor)

        flash(
            "Proveedor registrado correctamente.",
            "success"
        )

        return redirect(url_for("proveedores_lista"))

    return render_template(
        "formulario_proveedor.html",
        form=form
    )


# =========================
# FACTURACIÓN
# =========================

@app.route("/facturacion")
def facturacion_lista():
    return render_template(
        "facturacion.html",
        facturas=facturas
    )


@app.route("/facturacion/nueva", methods=["GET", "POST"])
def nueva_factura():

    form = FacturacionForm()

    if form.validate_on_submit():

        total = form.cantidad.data * form.precio.data

        factura = {
            "cliente": form.cliente.data,
            "producto": form.producto.data,
            "cantidad": form.cantidad.data,
            "precio": form.precio.data,
            "total": total
        }

        facturas.append(factura)

        flash(
            "Factura registrada correctamente.",
            "success"
        )

        return redirect(url_for("facturacion_lista"))

    return render_template(
        "formulario_facturacion.html",
        form=form
    )


# =========================
# EJECUTAR APLICACIÓN
# =========================

if __name__ == "__main__":
    app.run(debug=True)


# ============================================================
# ARCHIVO: forms/__init__.py
# ============================================================

# Formularios del Proyecto Integrador


# ============================================================
# ARCHIVO: forms/producto_form.py
# ============================================================

from flask_wtf import FlaskForm
from wtforms import StringField, FloatField, IntegerField, SubmitField
from wtforms.validators import DataRequired, Length, NumberRange


class ProductoForm(FlaskForm):

    nombre = StringField(
        "Nombre del producto",
        validators=[
            DataRequired(
                message="El nombre del producto es obligatorio."
            ),
            Length(
                min=3,
                max=100,
                message="El nombre debe tener entre 3 y 100 caracteres."
            )
        ]
    )

    descripcion = StringField(
        "Descripción",
        validators=[
            DataRequired(
                message="La descripción es obligatoria."
            ),
            Length(
                min=5,
                max=200,
                message="La descripción debe tener entre 5 y 200 caracteres."
            )
        ]
    )

    precio = FloatField(
        "Precio",
        validators=[
            DataRequired(
                message="El precio es obligatorio."
            ),
            NumberRange(
                min=0.01,
                message="El precio debe ser mayor que 0."
            )
        ]
    )

    stock = IntegerField(
        "Stock",
        validators=[
            DataRequired(
                message="El stock es obligatorio."
            ),
            NumberRange(
                min=0,
                message="El stock no puede ser negativo."
            )
        ]
    )

    submit = SubmitField("Guardar producto")


# ============================================================
# ARCHIVO: forms/cliente_form.py
# ============================================================

from flask_wtf import FlaskForm
from wtforms import StringField, EmailField, TelField, SubmitField
from wtforms.validators import DataRequired, Length, Email


class ClienteForm(FlaskForm):

    nombre = StringField(
        "Nombre completo",
        validators=[
            DataRequired(
                message="El nombre es obligatorio."
            ),
            Length(
                min=3,
                max=100,
                message="El nombre debe tener entre 3 y 100 caracteres."
            )
        ]
    )

    email = EmailField(
        "Correo electrónico",
        validators=[
            DataRequired(
                message="El correo electrónico es obligatorio."
            ),
            Email(
                message="Ingrese un correo electrónico válido."
            )
        ]
    )

    telefono = TelField(
        "Teléfono",
        validators=[
            DataRequired(
                message="El teléfono es obligatorio."
            ),
            Length(
                min=7,
                max=15,
                message="El teléfono debe tener entre 7 y 15 caracteres."
            )
        ]
    )

    direccion = StringField(
        "Dirección",
        validators=[
            DataRequired(
                message="La dirección es obligatoria."
            ),
            Length(
                min=5,
                max=150,
                message="La dirección debe tener entre 5 y 150 caracteres."
            )
        ]
    )

    submit = SubmitField("Guardar cliente")


# ============================================================
# ARCHIVO: forms/proveedor_form.py
# ============================================================

from flask_wtf import FlaskForm
from wtforms import StringField, EmailField, TelField, SubmitField
from wtforms.validators import DataRequired, Length, Email


class ProveedorForm(FlaskForm):

    empresa = StringField(
        "Empresa",
        validators=[
            DataRequired(
                message="El nombre de la empresa es obligatorio."
            ),
            Length(
                min=3,
                max=100,
                message="La empresa debe tener entre 3 y 100 caracteres."
            )
        ]
    )

    contacto = StringField(
        "Persona de contacto",
        validators=[
            DataRequired(
                message="El contacto es obligatorio."
            ),
            Length(
                min=3,
                max=100,
                message="Ingrese un nombre válido."
            )
        ]
    )

    email = EmailField(
        "Correo electrónico",
        validators=[
            DataRequired(
                message="El correo electrónico es obligatorio."
            ),
            Email(
                message="Ingrese un correo electrónico válido."
            )
        ]
    )

    telefono = TelField(
        "Teléfono",
        validators=[
            DataRequired(
                message="El teléfono es obligatorio."
            ),
            Length(
                min=7,
                max=15,
                message="El teléfono debe tener entre 7 y 15 caracteres."
            )
        ]
    )

    direccion = StringField(
        "Dirección",
        validators=[
            DataRequired(
                message="La dirección es obligatoria."
            ),
            Length(
                min=5,
                max=150,
                message="La dirección debe tener entre 5 y 150 caracteres."
            )
        ]
    )

    submit = SubmitField("Guardar proveedor")


# ============================================================
# ARCHIVO: forms/facturacion_form.py
# ============================================================

from flask_wtf import FlaskForm
from wtforms import StringField, FloatField, IntegerField, SubmitField
from wtforms.validators import DataRequired, NumberRange


class FacturacionForm(FlaskForm):

    cliente = StringField(
        "Cliente",
        validators=[
            DataRequired(
                message="El cliente es obligatorio."
            )
        ]
    )

    producto = StringField(
        "Producto",
        validators=[
            DataRequired(
                message="El producto es obligatorio."
            )
        ]
    )

    cantidad = IntegerField(
        "Cantidad",
        validators=[
            DataRequired(
                message="La cantidad es obligatoria."
            ),
            NumberRange(
                min=1,
                message="La cantidad debe ser mayor o igual a 1."
            )
        ]
    )

    precio = FloatField(
        "Precio unitario",
        validators=[
            DataRequired(
                message="El precio es obligatorio."
            ),
            NumberRange(
                min=0.01,
                message="El precio debe ser mayor que 0."
            )
        ]
    )

    submit = SubmitField("Generar factura")


# ============================================================
# ARCHIVO: templates/base.html
# ============================================================

<!DOCTYPE html>
<html lang="es">

<head>

    <meta charset="UTF-8">

    <meta name="viewport"
          content="width=device-width, initial-scale=1.0">

    <title>Proyecto Integrador</title>

    <link
        href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
        rel="stylesheet">

    <link
        rel="stylesheet"
        href="{{ url_for('static', filename='css/style.css') }}">

</head>

<body>

    {% include "components/navbar.html" %}

    {% with messages = get_flashed_messages(with_categories=true) %}

        {% if messages %}

            <div class="container mt-3">

                {% for category, message in messages %}

                    <div class="alert alert-{{ category }}">
                        {{ message }}
                    </div>

                {% endfor %}

            </div>

        {% endif %}

    {% endwith %}

    <main>
        {% block content %}
        {% endblock %}
    </main>

    {% include "components/footer.html" %}

    <script
        src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js">
    </script>

</body>

</html>


# ============================================================
# ARCHIVO: templates/components/navbar.html
# ============================================================

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">

    <div class="container">

        <a class="navbar-brand"
           href="{{ url_for('index') }}">
            Proyecto Integrador
        </a>

        <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#menu">

            <span class="navbar-toggler-icon"></span>

        </button>

        <div class="collapse navbar-collapse" id="menu">

            <ul class="navbar-nav ms-auto">

                <li class="nav-item">
                    <a class="nav-link"
                       href="{{ url_for('index') }}">
                        Inicio
                    </a>
                </li>

                <li class="nav-item">
                    <a class="nav-link"
                       href="{{ url_for('productos_lista') }}">
                        Productos
                    </a>
                </li>

                <li class="nav-item">
                    <a class="nav-link"
                       href="{{ url_for('clientes_lista') }}">
                        Clientes
                    </a>
                </li>

                <li class="nav-item">
                    <a class="nav-link"
                       href="{{ url_for('proveedores_lista') }}">
                        Proveedores
                    </a>
                </li>

                <li class="nav-item">
                    <a class="nav-link"
                       href="{{ url_for('facturacion_lista') }}">
                        Facturación
                    </a>
                </li>

            </ul>

        </div>

    </div>

</nav>


# ============================================================
# ARCHIVO: templates/components/footer.html
# ============================================================

<footer class="bg-dark text-white text-center p-3 mt-5">

    <p class="mb-0">
        Proyecto Integrador - Desarrollo de Aplicaciones Web
    </p>

    <p class="mb-0">
        Avance 11/16 - Flask-WTF y WTForms
    </p>

</footer>


# ============================================================
# ARCHIVO: templates/index.html
# ============================================================

{% extends "base.html" %}

{% block content %}

<div class="container mt-5">

    <div class="text-center">

        <h1>Proyecto Integrador</h1>

        <p class="lead">
            Sistema de gestión desarrollado con Flask,
            Jinja2, Flask-WTF y WTForms.
        </p>

    </div>

    <div class="row mt-5">

        <div class="col-md-3">
            <div class="card text-center shadow">
                <div class="card-body">

                    <h5>Productos</h5>

                    <h2>{{ productos|length }}</h2>

                    <a
                        href="{{ url_for('productos_lista') }}"
                        class="btn btn-primary">
                        Ver productos
                    </a>

                </div>
            </div>
        </div>


        <div class="col-md-3">

            <div class="card text-center shadow">

                <div class="card-body">

                    <h5>Clientes</h5>

                    <h2>{{ clientes|length }}</h2>

                    <a
                        href="{{ url_for('clientes_lista') }}"
                        class="btn btn-primary">
                        Ver clientes
                    </a>

                </div>

            </div>

        </div>


        <div class="col-md-3">

            <div class="card text-center shadow">

                <div class="card-body">

                    <h5>Proveedores</h5>

                    <h2>{{ proveedores|length }}</h2>

                    <a
                        href="{{ url_for('proveedores_lista') }}"
                        class="btn btn-primary">
                        Ver proveedores
                    </a>

                </div>

            </div>

        </div>


        <div class="col-md-3">

            <div class="card text-center shadow">

                <div class="card-body">

                    <h5>Facturas</h5>

                    <h2>{{ facturas|length }}</h2>

                    <a
                        href="{{ url_for('facturacion_lista') }}"
                        class="btn btn-primary">
                        Ver facturas
                    </a>

                </div>

            </div>

        </div>

    </div>

</div>

{% endblock %}


# ============================================================
# ARCHIVO: templates/formulario_producto.html
# ============================================================

{% extends "base.html" %}

{% block content %}

<div class="container mt-5">

    <div class="card shadow">

        <div class="card-header bg-primary text-white">

            <h2 class="mb-0">
                Registrar producto
            </h2>

        </div>

        <div class="card-body">

            <form method="POST">

                {{ form.hidden_tag() }}

                <div class="mb-3">

                    {{ form.nombre.label(
                        class="form-label"
                    ) }}

                    {{ form.nombre(
                        class="form-control"
                    ) }}

                    {% for error in form.nombre.errors %}

                        <div class="text-danger">
                            {{ error }}
                        </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.descripcion.label(
                        class="form-label"
                    ) }}

                    {{ form.descripcion(
                        class="form-control"
                    ) }}

                    {% for error in form.descripcion.errors %}

                        <div class="text-danger">
                            {{ error }}
                        </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.precio.label(
                        class="form-label"
                    ) }}

                    {{ form.precio(
                        class="form-control"
                    ) }}

                    {% for error in form.precio.errors %}

                        <div class="text-danger">
                            {{ error }}
                        </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.stock.label(
                        class="form-label"
                    ) }}

                    {{ form.stock(
                        class="form-control"
                    ) }}

                    {% for error in form.stock.errors %}

                        <div class="text-danger">
                            {{ error }}
                        </div>

                    {% endfor %}

                </div>


                {{ form.submit(
                    class="btn btn-primary"
                ) }}

                <a
                    href="{{ url_for('productos_lista') }}"
                    class="btn btn-secondary">
                    Cancelar
                </a>

            </form>

        </div>

    </div>

</div>

{% endblock %}


# ============================================================
# ARCHIVO: templates/productos.html
# ============================================================

{% extends "base.html" %}

{% block content %}

<div class="container mt-5">

    <div class="d-flex justify-content-between">

        <h1>Productos</h1>

        <a
            href="{{ url_for('nuevo_producto') }}"
            class="btn btn-primary">
            Nuevo producto
        </a>

    </div>

    <hr>

    {% if productos %}

    <div class="table-responsive">

        <table class="table table-striped table-bordered">

            <thead class="table-dark">

                <tr>
                    <th>Nombre</th>
                    <th>Descripción</th>
                    <th>Precio</th>
                    <th>Stock</th>
                </tr>

            </thead>

            <tbody>

                {% for producto in productos %}

                <tr>

                    <td>{{ producto.nombre }}</td>

                    <td>{{ producto.descripcion }}</td>

                    <td>
                        ${{ "%.2f"|format(producto.precio) }}
                    </td>

                    <td>{{ producto.stock }}</td>

                </tr>

                {% endfor %}

            </tbody>

        </table>

    </div>

    {% else %}

    <div class="alert alert-info">
        No existen productos registrados.
    </div>

    {% endif %}

</div>

{% endblock %}


# ============================================================
# ARCHIVO: templates/formulario_cliente.html
# ============================================================

{% extends "base.html" %}

{% block content %}

<div class="container mt-5">

    <div class="card shadow">

        <div class="card-header bg-primary text-white">

            <h2>Registrar cliente</h2>

        </div>

        <div class="card-body">

            <form method="POST">

                {{ form.hidden_tag() }}

                <div class="mb-3">

                    {{ form.nombre.label(
                        class="form-label"
                    ) }}

                    {{ form.nombre(
                        class="form-control"
                    ) }}

                    {% for error in form.nombre.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.email.label(
                        class="form-label"
                    ) }}

                    {{ form.email(
                        class="form-control"
                    ) }}

                    {% for error in form.email.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.telefono.label(
                        class="form-label"
                    ) }}

                    {{ form.telefono(
                        class="form-control"
                    ) }}

                    {% for error in form.telefono.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.direccion.label(
                        class="form-label"
                    ) }}

                    {{ form.direccion(
                        class="form-control"
                    ) }}

                    {% for error in form.direccion.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                {{ form.submit(
                    class="btn btn-primary"
                ) }}

                <a
                    href="{{ url_for('clientes_lista') }}"
                    class="btn btn-secondary">
                    Cancelar
                </a>

            </form>

        </div>

    </div>

</div>

{% endblock %}


# ============================================================
# ARCHIVO: templates/clientes.html
# ============================================================

{% extends "base.html" %}

{% block content %}

<div class="container mt-5">

    <div class="d-flex justify-content-between">

        <h1>Clientes</h1>

        <a
            href="{{ url_for('nuevo_cliente') }}"
            class="btn btn-primary">
            Nuevo cliente
        </a>

    </div>

    <hr>

    {% if clientes %}

    <table class="table table-striped table-bordered">

        <thead class="table-dark">

            <tr>
                <th>Nombre</th>
                <th>Email</th>
                <th>Teléfono</th>
                <th>Dirección</th>
            </tr>

        </thead>

        <tbody>

            {% for cliente in clientes %}

            <tr>

                <td>{{ cliente.nombre }}</td>
                <td>{{ cliente.email }}</td>
                <td>{{ cliente.telefono }}</td>
                <td>{{ cliente.direccion }}</td>

            </tr>

            {% endfor %}

        </tbody>

    </table>

    {% else %}

    <div class="alert alert-info">
        No existen clientes registrados.
    </div>

    {% endif %}

</div>

{% endblock %}


# ============================================================
# ARCHIVO: templates/formulario_proveedor.html
# ============================================================

{% extends "base.html" %}

{% block content %}

<div class="container mt-5">

    <div class="card shadow">

        <div class="card-header bg-primary text-white">

            <h2>Registrar proveedor</h2>

        </div>

        <div class="card-body">

            <form method="POST">

                {{ form.hidden_tag() }}

                <div class="mb-3">

                    {{ form.empresa.label(
                        class="form-label"
                    ) }}

                    {{ form.empresa(
                        class="form-control"
                    ) }}

                    {% for error in form.empresa.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.contacto.label(
                        class="form-label"
                    ) }}

                    {{ form.contacto(
                        class="form-control"
                    ) }}

                    {% for error in form.contacto.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.email.label(
                        class="form-label"
                    ) }}

                    {{ form.email(
                        class="form-control"
                    ) }}

                    {% for error in form.email.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.telefono.label(
                        class="form-label"
                    ) }}

                    {{ form.telefono(
                        class="form-control"
                    ) }}

                    {% for error in form.telefono.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.direccion.label(
                        class="form-label"
                    ) }}

                    {{ form.direccion(
                        class="form-control"
                    ) }}

                    {% for error in form.direccion.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                {{ form.submit(
                    class="btn btn-primary"
                ) }}

                <a
                    href="{{ url_for('proveedores_lista') }}"
                    class="btn btn-secondary">
                    Cancelar
                </a>

            </form>

        </div>

    </div>

</div>

{% endblock %}


# ============================================================
# ARCHIVO: templates/proveedores.html
# ============================================================

{% extends "base.html" %}

{% block content %}

<div class="container mt-5">

    <div class="d-flex justify-content-between">

        <h1>Proveedores</h1>

        <a
            href="{{ url_for('nuevo_proveedor') }}"
            class="btn btn-primary">
            Nuevo proveedor
        </a>

    </div>

    <hr>

    {% if proveedores %}

    <table class="table table-striped table-bordered">

        <thead class="table-dark">

            <tr>
                <th>Empresa</th>
                <th>Contacto</th>
                <th>Email</th>
                <th>Teléfono</th>
                <th>Dirección</th>
            </tr>

        </thead>

        <tbody>

            {% for proveedor in proveedores %}

            <tr>

                <td>{{ proveedor.empresa }}</td>
                <td>{{ proveedor.contacto }}</td>
                <td>{{ proveedor.email }}</td>
                <td>{{ proveedor.telefono }}</td>
                <td>{{ proveedor.direccion }}</td>

            </tr>

            {% endfor %}

        </tbody>

    </table>

    {% else %}

    <div class="alert alert-info">
        No existen proveedores registrados.
    </div>

    {% endif %}

</div>

{% endblock %}


# ============================================================
# ARCHIVO: templates/formulario_facturacion.html
# ============================================================

{% extends "base.html" %}

{% block content %}

<div class="container mt-5">

    <div class="card shadow">

        <div class="card-header bg-success text-white">

            <h2>Nueva factura</h2>

        </div>

        <div class="card-body">

            <form method="POST">

                {{ form.hidden_tag() }}

                <div class="mb-3">

                    {{ form.cliente.label(
                        class="form-label"
                    ) }}

                    {{ form.cliente(
                        class="form-control"
                    ) }}

                    {% for error in form.cliente.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.producto.label(
                        class="form-label"
                    ) }}

                    {{ form.producto(
                        class="form-control"
                    ) }}

                    {% for error in form.producto.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.cantidad.label(
                        class="form-label"
                    ) }}

                    {{ form.cantidad(
                        class="form-control"
                    ) }}

                    {% for error in form.cantidad.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                <div class="mb-3">

                    {{ form.precio.label(
                        class="form-label"
                    ) }}

                    {{ form.precio(
                        class="form-control"
                    ) }}

                    {% for error in form.precio.errors %}

                    <div class="text-danger">
                        {{ error }}
                    </div>

                    {% endfor %}

                </div>


                {{ form.submit(
                    class="btn btn-success"
                ) }}

                <a
                    href="{{ url_for('facturacion_lista') }}"
                    class="btn btn-secondary">
                    Cancelar
                </a>

            </form>

        </div>

    </div>

</div>

{% endblock %}


# ============================================================
# ARCHIVO: templates/facturacion.html
# ============================================================

{% extends "base.html" %}

{% block content %}

<div class="container mt-5">

    <div class="d-flex justify-content-between">

        <h1>Facturación</h1>

        <a
            href="{{ url_for('nueva_factura') }}"
            class="btn btn-success">
            Nueva factura
        </a>

    </div>

    <hr>

    {% if facturas %}

    <table class="table table-striped table-bordered">

        <thead class="table-dark">

            <tr>
                <th>Cliente</th>
                <th>Producto</th>
                <th>Cantidad</th>
                <th>Precio unitario</th>
                <th>Total</th>
            </tr>

        </thead>

        <tbody>

            {% for factura in facturas %}

            <tr>

                <td>{{ factura.cliente }}</td>

                <td>{{ factura.producto }}</td>

                <td>{{ factura.cantidad }}</td>

                <td>
                    ${{ "%.2f"|format(factura.precio) }}
                </td>

                <td>
                    ${{ "%.2f"|format(factura.total) }}
                </td>

            </tr>

            {% endfor %}

        </tbody>

    </table>

    {% else %}

    <div class="alert alert-info">
        No existen facturas registradas.
    </div>

    {% endif %}

</div>

{% endblock %}


# ============================================================
# ARCHIVO: static/css/style.css
# ============================================================

body {
    background-color: #f5f5f5;
}

.card {
    border-radius: 10px;
}

h1, h2 {
    font-weight: 600;
}

.text-danger {
    font-size: 0.9rem;
    margin-top: 5px;
}
from flask import Flask, render_template, redirect, url_for, flash
from forms.producto_form import ProductoForm
import sqlite3
import os

app = Flask(__name__)
app.config["SECRET_KEY"] = "clave-secreta-proyecto"

BASE_DIR = os.path.dirname(os.path.abspath(__file__))
DATA_DIR = os.path.join(BASE_DIR, "data")
DATABASE = os.path.join(DATA_DIR, "ferreteria.db")

os.makedirs(DATA_DIR, exist_ok=True)

def get_db_connection():
    conn = sqlite3.connect(DATABASE)
    conn.row_factory = sqlite3.Row
    return conn

def init_db():
    conn = get_db_connection()
    conn.execute("""
        CREATE TABLE IF NOT EXISTS productos (
            id INTEGER PRIMARY KEY AUTOINCREMENT,
            nombre TEXT NOT NULL,
            descripcion TEXT NOT NULL,
            precio REAL NOT NULL,
            stock INTEGER NOT NULL
        )
    """)
    conn.commit()
    conn.close()

@app.route("/")
def index():
    return render_template("index.html")

@app.route("/productos", methods=["GET", "POST"])
def productos():
    form = ProductoForm()
    if form.validate_on_submit():
        conn = get_db_connection()
        conn.execute(
            "INSERT INTO productos (nombre, descripcion, precio, stock) VALUES (?, ?, ?, ?)",
            (
                form.nombre.data,
                form.descripcion.data,
                form.precio.data,
                form.stock.data
            )
        )
        conn.commit()
        conn.close()
        flash("Producto registrado correctamente.", "success")
        return redirect(url_for("productos"))
    conn = get_db_connection()
    productos = conn.execute("SELECT id, nombre, descripcion, precio, stock FROM productos ORDER BY id DESC").fetchall()
    conn.close()
    return render_template("productos.html", form=form, productos=productos)

@app.route("/productos/nuevo", methods=["GET", "POST"])
def nuevo_producto():
    form = ProductoForm()
    if form.validate_on_submit():
        conn = get_db_connection()
        conn.execute(
            "INSERT INTO productos (nombre, descripcion, precio, stock) VALUES (?, ?, ?, ?)",
            (
                form.nombre.data,
                form.descripcion.data,
                form.precio.data,
                form.stock.data
            )
        )
        conn.commit()
        conn.close()
        flash("Producto guardado correctamente.", "success")
        return redirect(url_for("productos"))
    return render_template("formulario_producto.html", form=form)

@app.route("/productos/eliminar/<int:id>", methods=["POST"])
def eliminar_producto(id):
    conn = get_db_connection()
    conn.execute("DELETE FROM productos WHERE id = ?", (id,))
    conn.commit()
    conn.close()
    flash("Producto eliminado correctamente.", "success")
    return redirect(url_for("productos"))

@app.route("/clientes")
def clientes():
    return render_template("clientes.html")

@app.route("/proveedores")
def proveedores():
    return render_template("proveedores.html")

@app.route("/facturacion")
def facturacion():
    return render_template("facturacion.html")

if __name__ == "__main__":
    init_db()
    app.run(debug=True)


    ==================================================
ESTRUCTURA DEL PROYECTO
==================================================

Proyecto_Ferreteria/
│
├── app.py
├── requirements.txt
├── .env
├── .gitignore
│
├── conexion/
│   ├── __init__.py
│   └── conexion.py
│
├── sql/
│   └── esquema.sql
│
├── forms/
│   ├── __init__.py
│   └── producto_form.py
│
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── productos.html
│   └── formulario_producto.html
│
└── static/
    └── css/
        └── style.css


==================================================
ARCHIVO: requirements.txt
==================================================

Flask
Flask-WTF
WTForms
mysql-connector-python
python-dotenv


==================================================
ARCHIVO: .env
==================================================

DB_HOST=localhost
DB_PORT=3306
DB_USER=root
DB_PASSWORD=TU_CONTRASEÑA_DE_MYSQL
DB_NAME=ferreteria_db


==================================================
ARCHIVO: .gitignore
==================================================

.env
__pycache__/
*.pyc
.venv/
venv/


==================================================
ARCHIVO: conexion/__init__.py
==================================================

(Puede permanecer vacío)


==================================================
ARCHIVO: conexion/conexion.py
==================================================

import os
import mysql.connector
from dotenv import load_dotenv

load_dotenv()


def obtener_conexion():
    return mysql.connector.connect(
        host=os.getenv("DB_HOST", "localhost"),
        port=int(os.getenv("DB_PORT", "3306")),
        user=os.getenv("DB_USER", "root"),
        password=os.getenv("DB_PASSWORD", ""),
        database=os.getenv("DB_NAME", "ferreteria_db")
    )


==================================================
ARCHIVO: sql/esquema.sql
==================================================

CREATE DATABASE IF NOT EXISTS ferreteria_db
CHARACTER SET utf8mb4
COLLATE utf8mb4_unicode_ci;

USE ferreteria_db;

CREATE TABLE IF NOT EXISTS proveedores (
    id_proveedor INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    telefono VARCHAR(20),
    correo VARCHAR(100)
);

CREATE TABLE IF NOT EXISTS clientes (
    id_cliente INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    cedula VARCHAR(20) UNIQUE,
    telefono VARCHAR(20),
    correo VARCHAR(100)
);

CREATE TABLE IF NOT EXISTS productos (
    id_producto INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    precio DECIMAL(10,2) NOT NULL,
    stock INT NOT NULL DEFAULT 0,
    id_proveedor INT,
    CONSTRAINT fk_producto_proveedor
        FOREIGN KEY (id_proveedor)
        REFERENCES proveedores(id_proveedor)
        ON UPDATE CASCADE
        ON DELETE SET NULL
);

CREATE TABLE IF NOT EXISTS facturas (
    id_factura INT AUTO_INCREMENT PRIMARY KEY,
    id_cliente INT,
    fecha DATETIME DEFAULT CURRENT_TIMESTAMP,
    total DECIMAL(10,2) NOT NULL DEFAULT 0.00,
    CONSTRAINT fk_factura_cliente
        FOREIGN KEY (id_cliente)
        REFERENCES clientes(id_cliente)
        ON UPDATE CASCADE
        ON DELETE SET NULL
);

INSERT INTO proveedores (nombre, telefono, correo)
SELECT 'Distribuidora Ferretera S.A.', '0991234567',
       'ventas@distribuidora.com'
WHERE NOT EXISTS (
    SELECT 1 FROM proveedores
    WHERE correo = 'ventas@distribuidora.com'
);

INSERT INTO proveedores (nombre, telefono, correo)
SELECT 'Importadora El Constructor', '0987654321',
       'contacto@constructor.com'
WHERE NOT EXISTS (
    SELECT 1 FROM proveedores
    WHERE correo = 'contacto@constructor.com'
);


==================================================
ARCHIVO: forms/__init__.py
==================================================

(Puede permanecer vacío)


==================================================
ARCHIVO: forms/producto_form.py
==================================================

from flask_wtf import FlaskForm
from wtforms import StringField, DecimalField, IntegerField, SelectField, SubmitField
from wtforms.validators import DataRequired, Length, NumberRange, Optional


class ProductoForm(FlaskForm):

    nombre = StringField(
        "Nombre del producto",
        validators=[
            DataRequired(message="El nombre es obligatorio."),
            Length(
                min=2,
                max=100,
                message="El nombre debe tener entre 2 y 100 caracteres."
            )
        ]
    )

    precio = DecimalField(
        "Precio",
        validators=[
            DataRequired(message="El precio es obligatorio."),
            NumberRange(
                min=0,
                message="El precio no puede ser negativo."
            )
        ],
        places=2
    )

    stock = IntegerField(
        "Stock",
        validators=[
            DataRequired(message="El stock es obligatorio."),
            NumberRange(
                min=0,
                message="El stock no puede ser negativo."
            )
        ]
    )

    id_proveedor = SelectField(
        "Proveedor",
        coerce=int,
        validators=[Optional()]
    )

    submit = SubmitField("Guardar producto")


==================================================
ARCHIVO: app.py
==================================================

from flask import Flask, render_template, redirect, url_for, flash, request
from dotenv import load_dotenv

from conexion.conexion import obtener_conexion
from forms.producto_form import ProductoForm

load_dotenv()

app = Flask(__name__)

app.config["SECRET_KEY"] = "clave-desarrollo-ferreteria-2026"


def obtener_proveedores():
    conexion = None
    cursor = None

    try:
        conexion = obtener_conexion()
        cursor = conexion.cursor(dictionary=True)

        cursor.execute("""
            SELECT id_proveedor, nombre
            FROM proveedores
            ORDER BY nombre ASC
        """)

        return cursor.fetchall()

    except Exception as error:
        print(f"Error al obtener proveedores: {error}")
        return []

    finally:
        if cursor is not None:
            cursor.close()

        if conexion is not None and conexion.is_connected():
            conexion.close()


def cargar_opciones_proveedores(form):
    proveedores = obtener_proveedores()

    form.id_proveedor.choices = [
        (0, "Sin proveedor")
    ] + [
        (proveedor["id_proveedor"], proveedor["nombre"])
        for proveedor in proveedores
    ]


@app.route("/")
def index():
    return render_template("index.html")


@app.route("/productos")
def productos():
    conexion = None
    cursor = None
    productos_registrados = []

    try:
        conexion = obtener_conexion()
        cursor = conexion.cursor(dictionary=True)

        consulta = """
            SELECT
                p.id_producto,
                p.nombre,
                p.precio,
                p.stock,
                p.id_proveedor,
                COALESCE(pr.nombre, 'Sin proveedor') AS proveedor
            FROM productos p
            LEFT JOIN proveedores pr
                ON p.id_proveedor = pr.id_proveedor
            ORDER BY p.id_producto DESC
        """

        cursor.execute(consulta)
        productos_registrados = cursor.fetchall()

    except Exception as error:
        flash(f"Error al consultar los productos: {error}", "danger")

    finally:
        if cursor is not None:
            cursor.close()

        if conexion is not None and conexion.is_connected():
            conexion.close()

    return render_template(
        "productos.html",
        productos=productos_registrados
    )


@app.route("/productos/nuevo", methods=["GET", "POST"])
def nuevo_producto():
    form = ProductoForm()
    cargar_opciones_proveedores(form)

    if form.validate_on_submit():
        conexion = None
        cursor = None

        try:
            conexion = obtener_conexion()
            cursor = conexion.cursor()

            id_proveedor = form.id_proveedor.data

            if id_proveedor == 0:
                id_proveedor = None

            consulta = """
                INSERT INTO productos
                    (nombre, precio, stock, id_proveedor)
                VALUES (%s, %s, %s, %s)
            """

            valores = (
                form.nombre.data,
                form.precio.data,
                form.stock.data,
                id_proveedor
            )

            cursor.execute(consulta, valores)
            conexion.commit()

            flash(
                "Producto agregado correctamente a MySQL.",
                "success"
            )

            return redirect(url_for("productos"))

        except Exception as error:
            if conexion is not None:
                conexion.rollback()

            flash(
                f"Error al agregar el producto: {error}",
                "danger"
            )

        finally:
            if cursor is not None:
                cursor.close()

            if conexion is not None and conexion.is_connected():
                conexion.close()

    return render_template(
        "formulario_producto.html",
        form=form,
        titulo="Agregar producto"
    )


@app.route("/productos/editar/<int:id_producto>", methods=["GET", "POST"])
def editar_producto(id_producto):
    conexion = None
    cursor = None
    producto = None

    try:
        conexion = obtener_conexion()
        cursor = conexion.cursor(dictionary=True)

        cursor.execute("""
            SELECT id_producto, nombre, precio, stock, id_proveedor
            FROM productos
            WHERE id_producto = %s
        """, (id_producto,))

        producto = cursor.fetchone()

    except Exception as error:
        flash(
            f"Error al recuperar el producto: {error}",
            "danger"
        )

        return redirect(url_for("productos"))

    finally:
        if cursor is not None:
            cursor.close()

        if conexion is not None and conexion.is_connected():
            conexion.close()

    if producto is None:
        flash("El producto no existe.", "warning")
        return redirect(url_for("productos"))

    form = ProductoForm()
    cargar_opciones_proveedores(form)

    if request.method == "GET":
        form.nombre.data = producto["nombre"]
        form.precio.data = producto["precio"]
        form.stock.data = producto["stock"]
        form.id_proveedor.data = producto["id_proveedor"] or 0

    if form.validate_on_submit():
        conexion = None
        cursor = None

        try:
            conexion = obtener_conexion()
            cursor = conexion.cursor()

            id_proveedor = form.id_proveedor.data

            if id_proveedor == 0:
                id_proveedor = None

            consulta = """
                UPDATE productos
                SET nombre = %s,
                    precio = %s,
                    stock = %s,
                    id_proveedor = %s
                WHERE id_producto = %s
            """

            valores = (
                form.nombre.data,
                form.precio.data,
                form.stock.data,
                id_proveedor,
                id_producto
            )

            cursor.execute(consulta, valores)
            conexion.commit()

            flash(
                "Producto modificado correctamente en MySQL.",
                "success"
            )

            return redirect(url_for("productos"))

        except Exception as error:
            if conexion is not None:
                conexion.rollback()

            flash(
                f"Error al modificar el producto: {error}",
                "danger"
            )

        finally:
            if cursor is not None:
                cursor.close()

            if conexion is not None and conexion.is_connected():
                conexion.close()

    return render_template(
        "formulario_producto.html",
        form=form,
        titulo="Modificar producto"
    )


@app.route("/productos/eliminar/<int:id_producto>", methods=["POST"])
def eliminar_producto(id_producto):
    conexion = None
    cursor = None

    try:
        conexion = obtener_conexion()
        cursor = conexion.cursor()

        consulta = """
            DELETE FROM productos
            WHERE id_producto = %s
        """

        cursor.execute(consulta, (id_producto,))
        conexion.commit()

        if cursor.rowcount > 0:
            flash(
                "Producto eliminado correctamente de MySQL.",
                "success"
            )
        else:
            flash("El producto no existe.", "warning")

    except Exception as error:
        if conexion is not None:
            conexion.rollback()

        flash(
            f"Error al eliminar el producto: {error}",
            "danger"
        )

    finally:
        if cursor is not None:
            cursor.close()

        if conexion is not None and conexion.is_connected():
            conexion.close()

    return redirect(url_for("productos"))


if __name__ == "__main__":
    app.run(debug=True)


==================================================
ARCHIVO: templates/base.html
==================================================

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>{% block title %}Ferretería{% endblock %}</title>

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
          rel="stylesheet">

    <link rel="stylesheet"
          href="{{ url_for('static', filename='css/style.css') }}">
</head>

<body class="bg-light">

    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
        <div class="container">

            <a class="navbar-brand fw-bold"
               href="{{ url_for('index') }}">
                Ferretería El Constructor
            </a>

            <button class="navbar-toggler"
                    type="button"
                    data-bs-toggle="collapse"
                    data-bs-target="#menu">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="menu">
                <ul class="navbar-nav ms-auto">

                    <li class="nav-item">
                        <a class="nav-link"
                           href="{{ url_for('index') }}">
                            Inicio
                        </a>
                    </li>

                    <li class="nav-item">
                        <a class="nav-link"
                           href="{{ url_for('productos') }}">
                            Productos
                        </a>
                    </li>

                </ul>
            </div>

        </div>
    </nav>

    <main class="container py-4">

        {% with mensajes = get_flashed_messages(with_categories=true) %}
            {% if mensajes %}
                {% for categoria, mensaje in mensajes %}

                    <div class="alert alert-{{ categoria }} alert-dismissible fade show"
                         role="alert">

                        {{ mensaje }}

                        <button type="button"
                                class="btn-close"
                                data-bs-dismiss="alert">
                        </button>

                    </div>

                {% endfor %}
            {% endif %}
        {% endwith %}

        {% block content %}{% endblock %}

    </main>

    <footer class="bg-dark text-white text-center py-3 mt-5">
        <p class="mb-0">
            Proyecto Integrador — Gestión de Ferretería
        </p>

        <small>
            Flask + MySQL + Flask-WTF
        </small>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

</body>
</html>


==================================================
ARCHIVO: templates/index.html
==================================================

{% extends "base.html" %}

{% block title %}Inicio - Ferretería{% endblock %}

{% block content %}

<div class="p-5 mb-4 bg-white rounded-3 shadow-sm">

    <div class="container-fluid py-4">

        <h1 class="display-5 fw-bold">
            Sistema de Gestión de Ferretería
        </h1>

        <p class="col-md-8 fs-5">
            Aplicación web desarrollada con Flask, Flask-WTF y MySQL
            para administrar productos y proveedores.
        </p>

        <a href="{{ url_for('productos') }}"
           class="btn btn-primary btn-lg">
            Administrar productos
        </a>

    </div>

</div>

<div class="row g-4">

    <div class="col-md-4">
        <div class="card shadow-sm h-100">
            <div class="card-body">
                <h5 class="card-title">Base de datos</h5>
                <p class="card-text">
                    Información almacenada de forma persistente en MySQL.
                </p>
            </div>
        </div>
    </div>

    <div class="col-md-4">
        <div class="card shadow-sm h-100">
            <div class="card-body">
                <h5 class="card-title">Productos</h5>
                <p class="card-text">
                    Registro, consulta, modificación y eliminación
                    de productos.
                </p>
            </div>
        </div>
    </div>

    <div class="col-md-4">
        <div class="card shadow-sm h-100">
            <div class="card-body">
                <h5 class="card-title">Validaciones</h5>
                <p class="card-text">
                    Formularios validados mediante Flask-WTF y WTForms.
                </p>
            </div>
        </div>
    </div>

</div>

{% endblock %}


==================================================
ARCHIVO: templates/productos.html
==================================================

{% extends "base.html" %}

{% block title %}Productos - Ferretería{% endblock %}

{% block content %}

<div class="d-flex justify-content-between align-items-center mb-4">

    <div>
        <h1 class="mb-1">Productos</h1>
        <p class="text-muted mb-0">
            Registros almacenados en la base de datos MySQL.
        </p>
    </div>

    <a href="{{ url_for('nuevo_producto') }}"
       class="btn btn-success">
        + Agregar producto
    </a>

</div>

<div class="card shadow-sm">

    <div class="card-body">

        {% if productos %}

        <div class="table-responsive">

            <table class="table table-striped table-hover align-middle">

                <thead class="table-primary">
                    <tr>
                        <th>ID</th>
                        <th>Producto</th>
                        <th>Precio</th>
                        <th>Stock</th>
                        <th>Proveedor</th>
                        <th class="text-center">Acciones</th>
                    </tr>
                </thead>

                <tbody>

                    {% for producto in productos %}

                    <tr>

                        <td>{{ producto.id_producto }}</td>

                        <td>{{ producto.nombre }}</td>

                        <td>
                            ${{ "%.2f"|format(producto.precio) }}
                        </td>

                        <td>{{ producto.stock }}</td>

                        <td>{{ producto.proveedor }}</td>

                        <td class="text-center">

                            <a href="{{ url_for('editar_producto', id_producto=producto.id_producto) }}"
                               class="btn btn-warning btn-sm">
                                Editar
                            </a>

                            <form action="{{ url_for('eliminar_producto', id_producto=producto.id_producto) }}"
                                  method="POST"
                                  class="d-inline"
                                  onsubmit="return confirm('¿Está seguro de eliminar este producto?');">

                                <input type="hidden"
                                       name="csrf_token"
                                       value="{{ csrf_token() }}">

                                <button type="submit"
                                        class="btn btn-danger btn-sm">
                                    Eliminar
                                </button>

                            </form>

                        </td>

                    </tr>

                    {% endfor %}

                </tbody>

            </table>

        </div>

        {% else %}

        <div class="alert alert-info mb-0">
            No existen productos registrados en la base de datos.
        </div>

        {% endif %}

    </div>

</div>

{% endblock %}


==================================================
ARCHIVO: templates/formulario_producto.html
==================================================

{% extends "base.html" %}

{% block title %}{{ titulo }} - Ferretería{% endblock %}

{% block content %}

<div class="row justify-content-center">

    <div class="col-md-7 col-lg-6">

        <div class="card shadow-sm">

            <div class="card-header bg-primary text-white">
                <h4 class="mb-0">{{ titulo }}</h4>
            </div>

            <div class="card-body">

                <form method="POST">

                    {{ form.hidden_tag() }}

                    <div class="mb-3">

                        {{ form.nombre.label(class="form-label") }}

                        {{ form.nombre(
                            class="form-control",
                            placeholder="Ejemplo: Martillo"
                        ) }}

                        {% for error in form.nombre.errors %}
                            <div class="text-danger small">
                                {{ error }}
                            </div>
                        {% endfor %}

                    </div>

                    <div class="mb-3">

                        {{ form.precio.label(class="form-label") }}

                        {{ form.precio(
                            class="form-control",
                            placeholder="Ejemplo: 15.50",
                            step="0.01"
                        ) }}

                        {% for error in form.precio.errors %}
                            <div class="text-danger small">
                                {{ error }}
                            </div>
                        {% endfor %}

                    </div>

                    <div class="mb-3">

                        {{ form.stock.label(class="form-label") }}

                        {{ form.stock(
                            class="form-control",
                            placeholder="Ejemplo: 25"
                        ) }}

                        {% for error in form.stock.errors %}
                            <div class="text-danger small">
                                {{ error }}
                            </div>
                        {% endfor %}

                    </div>

                    <div class="mb-3">

                        {{ form.id_proveedor.label(class="form-label") }}

                        {{ form.id_proveedor(class="form-select") }}

                        {% for error in form.id_proveedor.errors %}
                            <div class="text-danger small">
                                {{ error }}
                            </div>
                        {% endfor %}

                    </div>

                    <div class="d-flex justify-content-between">

                        <a href="{{ url_for('productos') }}"
                           class="btn btn-secondary">
                            Cancelar
                        </a>

                        {{ form.submit(class="btn btn-primary") }}

                    </div>

                </form>

            </div>

        </div>

    </div>

</div>

{% endblock %}


==================================================
ARCHIVO: static/css/style.css
==================================================

body {
    font-family: Arial, sans-serif;
}

.navbar-brand {
    letter-spacing: 0.3px;
}

.card {
    border: none;
}

.table th {
    white-space: nowrap;
}

.table td {
    vertical-align: middle;
}

footer {
    margin-top: 50px;
}
# ============================================================
# PROYECTO INTEGRADOR U4 - AVANCE 14/16
# IMPLEMENTACIÓN DE UN SISTEMA DE LOGIN FUNCIONAL
# FLASK + MYSQL + FLASK-LOGIN + FLASK-WTF + WERKZEUG
# ============================================================
#
# INSTALAR:
# pip install flask flask-login flask-wtf mysql-connector-python werkzeug
# pip freeze > requirements.txt
#
# ESTRUCTURA:
#
# Proyecto/
# ├── app.py
# ├── models.py
# ├── requirements.txt
# ├── conexion/
# │   ├── __init__.py
# │   └── conexion.py
# ├── forms/
# │   ├── __init__.py
# │   ├── login_form.py
# │   └── usuario_form.py
# ├── sql/
# │   └── esquema.sql
# ├── templates/
# │   ├── base.html
# │   ├── index.html
# │   ├── login.html
# │   ├── registro.html
# │   ├── dashboard.html
# │   ├── productos.html
# │   ├── clientes.html
# │   ├── proveedores.html
# │   └── facturacion.html
# └── static/
#     └── css/
#         └── style.css
#
# ============================================================
# 1. BASE DE DATOS MYSQL
# ============================================================
#
# CREATE DATABASE proyecto_integrador;
# USE proyecto_integrador;
#
# CREATE TABLE usuarios (
#     id INT AUTO_INCREMENT PRIMARY KEY,
#     usuario VARCHAR(50) UNIQUE NOT NULL,
#     password VARCHAR(255) NOT NULL
# );
#
# ------------------------------------------------------------
# TABLAS DEL CRUD DE SEMANA 13
# Estas tablas deben mantenerse si ya las tienes.
# Ejemplo:
#
# CREATE TABLE productos (
#     id INT AUTO_INCREMENT PRIMARY KEY,
#     nombre VARCHAR(100) NOT NULL,
#     precio DECIMAL(10,2) NOT NULL,
#     stock INT NOT NULL
# );
#
# CREATE TABLE clientes (
#     id INT AUTO_INCREMENT PRIMARY KEY,
#     nombre VARCHAR(100) NOT NULL,
#     correo VARCHAR(100) NOT NULL,
#     telefono VARCHAR(20)
# );
#
# CREATE TABLE proveedores (
#     id INT AUTO_INCREMENT PRIMARY KEY,
#     nombre VARCHAR(100) NOT NULL,
#     telefono VARCHAR(20),
#     correo VARCHAR(100)
# );
#
# CREATE TABLE facturacion (
#     id INT AUTO_INCREMENT PRIMARY KEY,
#     cliente VARCHAR(100) NOT NULL,
#     producto VARCHAR(100) NOT NULL,
#     cantidad INT NOT NULL,
#     total DECIMAL(10,2) NOT NULL
# );
#
# ============================================================
# 2. conexion/conexion.py
# ============================================================

import mysql.connector

def obtener_conexion():
    return mysql.connector.connect(
        host="localhost",
        user="root",
        password="TU_PASSWORD",
        database="proyecto_integrador"
    )


# ============================================================
# 3. models.py
# ============================================================

from flask_login import UserMixin


class Usuario(UserMixin):

    def __init__(self, id, usuario, password):
        self.id = id
        self.usuario = usuario
        self.password = password


# ============================================================
# 4. forms/login_form.py
# ============================================================

from flask_wtf import FlaskForm
from wtforms import StringField, PasswordField, SubmitField
from wtforms.validators import DataRequired


class LoginForm(FlaskForm):

    usuario = StringField(
        "Usuario",
        validators=[DataRequired()]
    )

    password = PasswordField(
        "Contraseña",
        validators=[DataRequired()]
    )

    submit = SubmitField(
        "Iniciar sesión"
    )


# ============================================================
# 5. forms/usuario_form.py
# ============================================================

from flask_wtf import FlaskForm
from wtforms import StringField, PasswordField, SubmitField
from wtforms.validators import (
    DataRequired,
    Length,
    EqualTo
)


class UsuarioForm(FlaskForm):

    usuario = StringField(
        "Usuario",
        validators=[
            DataRequired(),
            Length(min=3, max=50)
        ]
    )

    password = PasswordField(
        "Contraseña",
        validators=[
            DataRequired(),
            Length(min=6, max=100)
        ]
    )

    confirmar_password = PasswordField(
        "Confirmar contraseña",
        validators=[
            DataRequired(),
            EqualTo(
                "password",
                message="Las contraseñas no coinciden."
            )
        ]
    )

    submit = SubmitField(
        "Registrarse"
    )


# ============================================================
# 6. app.py
# ============================================================

from flask import (
    Flask,
    render_template,
    redirect,
    url_for,
    flash,
    request
)

from flask_login import (
    LoginManager,
    login_user,
    logout_user,
    login_required,
    current_user
)

from werkzeug.security import (
    generate_password_hash,
    check_password_hash
)

from conexion.conexion import obtener_conexion

from models import Usuario

from forms.login_form import LoginForm

from forms.usuario_form import UsuarioForm


# ------------------------------------------------------------
# CONFIGURACIÓN DE FLASK
# ------------------------------------------------------------

app = Flask(__name__)

app.config["SECRET_KEY"] = "clave-secreta-proyecto-integrador"


# ------------------------------------------------------------
# CONFIGURACIÓN FLASK-LOGIN
# ------------------------------------------------------------

login_manager = LoginManager()

login_manager.init_app(app)

login_manager.login_view = "login"

login_manager.login_message = (
    "Debe iniciar sesión para acceder a esta página."
)

login_manager.login_message_category = "warning"


# ------------------------------------------------------------
# CARGAR USUARIO
# ------------------------------------------------------------

@login_manager.user_loader
def load_user(user_id):

    conexion = obtener_conexion()

    cursor = conexion.cursor(
        dictionary=True
    )

    cursor.execute(
        """
        SELECT id, usuario, password
        FROM usuarios
        WHERE id = %s
        """,
        (user_id,)
    )

    datos = cursor.fetchone()

    cursor.close()

    conexion.close()

    if datos:

        return Usuario(
            datos["id"],
            datos["usuario"],
            datos["password"]
        )

    return None


# ============================================================
# PÁGINA PRINCIPAL
# ============================================================

@app.route("/")
def index():

    return render_template(
        "index.html"
    )


# ============================================================
# REGISTRO DE USUARIO
# ============================================================

@app.route(
    "/registro",
    methods=["GET", "POST"]
)
def registro():

    form = UsuarioForm()

    if form.validate_on_submit():

        usuario = form.usuario.data

        password = form.password.data

        conexion = obtener_conexion()

        cursor = conexion.cursor(
            dictionary=True
        )

        # Verificar si ya existe
        cursor.execute(
            """
            SELECT id
            FROM usuarios
            WHERE usuario = %s
            """,
            (usuario,)
        )

        usuario_existente = cursor.fetchone()

        if usuario_existente:

            cursor.close()

            conexion.close()

            flash(
                "El usuario ya existe.",
                "danger"
            )

            return render_template(
                "registro.html",
                form=form
            )

        # ----------------------------------------------------
        # CREAR HASH SEGURO
        # ----------------------------------------------------

        password_hash = generate_password_hash(
            password
        )

        # ----------------------------------------------------
        # INSERT PARAMETRIZADO
        # ----------------------------------------------------

        cursor.execute(
            """
            INSERT INTO usuarios
            (usuario, password)
            VALUES (%s, %s)
            """,
            (
                usuario,
                password_hash
            )
        )

        conexion.commit()

        cursor.close()

        conexion.close()

        flash(
            "Usuario registrado correctamente.",
            "success"
        )

        return redirect(
            url_for("login")
        )

    return render_template(
        "registro.html",
        form=form
    )


# ============================================================
# LOGIN
# ============================================================

@app.route(
    "/login",
    methods=["GET", "POST"]
)
def login():

    if current_user.is_authenticated:

        return redirect(
            url_for("dashboard")
        )

    form = LoginForm()

    if form.validate_on_submit():

        usuario = form.usuario.data

        password = form.password.data

        conexion = obtener_conexion()

        cursor = conexion.cursor(
            dictionary=True
        )

        # ----------------------------------------------------
        # BUSCAR USUARIO
        # ----------------------------------------------------

        cursor.execute(
            """
            SELECT id, usuario, password
            FROM usuarios
            WHERE usuario = %s
            """,
            (usuario,)
        )

        datos = cursor.fetchone()

        cursor.close()

        conexion.close()

        # ----------------------------------------------------
        # COMPROBAR CONTRASEÑA
        # ----------------------------------------------------

        if datos and check_password_hash(
            datos["password"],
            password
        ):

            usuario_obj = Usuario(
                datos["id"],
                datos["usuario"],
                datos["password"]
            )

            # ------------------------------------------------
            # CREAR SESIÓN
            # ------------------------------------------------

            login_user(
                usuario_obj
            )

            flash(
                "Inicio de sesión exitoso.",
                "success"
            )

            # Si intentó entrar a una ruta protegida
            siguiente = request.args.get(
                "next"
            )

            if siguiente:
                return redirect(siguiente)

            return redirect(
                url_for("dashboard")
            )

        flash(
            "Usuario o contraseña incorrectos.",
            "danger"
        )

    return render_template(
        "login.html",
        form=form
    )


# ============================================================
# DASHBOARD
# ============================================================

@app.route("/dashboard")
@login_required
def dashboard():

    return render_template(
        "dashboard.html"
    )


# ============================================================
# PRODUCTOS
# ============================================================

@app.route("/productos")
@login_required
def productos():

    conexion = obtener_conexion()

    cursor = conexion.cursor(
        dictionary=True
    )

    cursor.execute(
        "SELECT * FROM productos"
    )

    productos = cursor.fetchall()

    cursor.close()

    conexion.close()

    return render_template(
        "productos.html",
        productos=productos
    )


# ============================================================
# CLIENTES
# ============================================================

@app.route("/clientes")
@login_required
def clientes():

    conexion = obtener_conexion()

    cursor = conexion.cursor(
        dictionary=True
    )

    cursor.execute(
        "SELECT * FROM clientes"
    )

    clientes = cursor.fetchall()

    cursor.close()

    conexion.close()

    return render_template(
        "clientes.html",
        clientes=clientes
    )


# ============================================================
# PROVEEDORES
# ============================================================

@app.route("/proveedores")
@login_required
def proveedores():

    conexion = obtener_conexion()

    cursor = conexion.cursor(
        dictionary=True
    )

    cursor.execute(
        "SELECT * FROM proveedores"
    )

    proveedores = cursor.fetchall()

    cursor.close()

    conexion.close()

    return render_template(
        "proveedores.html",
        proveedores=proveedores
    )


# ============================================================
# FACTURACIÓN
# ============================================================

@app.route("/facturacion")
@login_required
def facturacion():

    conexion = obtener_conexion()

    cursor = conexion.cursor(
        dictionary=True
    )

    cursor.execute(
        "SELECT * FROM facturacion"
    )

    facturas = cursor.fetchall()

    cursor.close()

    conexion.close()

    return render_template(
        "facturacion.html",
        facturas=facturas
    )


# ============================================================
# LOGOUT
# ============================================================

@app.route("/logout")
@login_required
def logout():

    logout_user()

    flash(
        "Sesión cerrada correctamente.",
        "success"
    )

    return redirect(
        url_for("login")
    )


# ============================================================
# EJECUTAR APLICACIÓN
# ============================================================

if __name__ == "__main__":

    app.run(
        debug=True
    )


# ============================================================
# 7. templates/base.html
# ============================================================

"""
<!DOCTYPE html>

<html lang="es">

<head>

    <meta charset="UTF-8">

    <meta
        name="viewport"
        content="width=device-width, initial-scale=1.0"
    >

    <title>
        {% block title %}
        Sistema Web
        {% endblock %}
    </title>

    <link
        href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
        rel="stylesheet"
    >

    <link
        rel="stylesheet"
        href="{{ url_for('static', filename='css/style.css') }}"
    >

</head>

<body>

<nav class="navbar navbar-dark bg-dark">

    <div class="container">

        <a
            class="navbar-brand"
            href="{{ url_for('index') }}"
        >
            Sistema de Gestión
        </a>

        <div>

            {% if current_user.is_authenticated %}

                <span class="text-white me-3">

                    Usuario:
                    {{ current_user.usuario }}

                </span>

                <a
                    href="{{ url_for('dashboard') }}"
                    class="btn btn-outline-light me-2"
                >
                    Dashboard
                </a>

                <a
                    href="{{ url_for('logout') }}"
                    class="btn btn-danger"
                >
                    Cerrar sesión
                </a>

            {% else %}

                <a
                    href="{{ url_for('login') }}"
                    class="btn btn-outline-light me-2"
                >
                    Iniciar sesión
                </a>

                <a
                    href="{{ url_for('registro') }}"
                    class="btn btn-success"
                >
                    Registrarse
                </a>

            {% endif %}

        </div>

    </div>

</nav>


<div class="container mt-4">

    {% with mensajes =
        get_flashed_messages(
            with_categories=true
        )
    %}

        {% if mensajes %}

            {% for categoria, mensaje in mensajes %}

                <div
                    class="alert alert-{{ categoria }}"
                >
                    {{ mensaje }}
                </div>

            {% endfor %}

        {% endif %}

    {% endwith %}


    {% block content %}
    {% endblock %}

</div>

</body>

</html>
"""


# ============================================================
# 8. templates/index.html
# ============================================================

"""
{% extends "base.html" %}

{% block title %}
Inicio
{% endblock %}

{% block content %}

<div class="text-center mt-5">

    <h1>
        Sistema de Gestión
    </h1>

    <p class="lead">
        Proyecto Integrador U4
    </p>

    <p>
        Desarrollo de Aplicaciones Web
    </p>

    {% if current_user.is_authenticated %}

        <a
            href="{{ url_for('dashboard') }}"
            class="btn btn-primary"
        >
            Ir al Dashboard
        </a>

    {% else %}

        <a
            href="{{ url_for('login') }}"
            class="btn btn-primary me-2"
        >
            Iniciar sesión
        </a>

        <a
            href="{{ url_for('registro') }}"
            class="btn btn-success"
        >
            Registrarse
        </a>

    {% endif %}

</div>

{% endblock %}
"""


# ============================================================
# 9. templates/login.html
# ============================================================

"""
{% extends "base.html" %}

{% block title %}
Iniciar sesión
{% endblock %}

{% block content %}

<div class="row justify-content-center">

    <div class="col-md-5">

        <div class="card shadow">

            <div class="card-header bg-primary text-white">

                <h3 class="text-center">
                    Iniciar sesión
                </h3>

            </div>

            <div class="card-body">

                <form method="POST">

                    {{ form.hidden_tag() }}

                    <div class="mb-3">

                        {{ form.usuario.label(
                            class="form-label"
                        ) }}

                        {{ form.usuario(
                            class="form-control",
                            placeholder="Ingrese usuario"
                        ) }}

                    </div>

                    <div class="mb-3">

                        {{ form.password.label(
                            class="form-label"
                        ) }}

                        {{ form.password(
                            class="form-control",
                            placeholder="Ingrese contraseña"
                        ) }}

                    </div>

                    <div class="d-grid">

                        {{ form.submit(
                            class="btn btn-primary"
                        ) }}

                    </div>

                </form>

                <div class="text-center mt-3">

                    <a
                        href="{{ url_for('registro') }}"
                    >
                        Crear una cuenta
                    </a>

                </div>

            </div>

        </div>

    </div>

</div>

{% endblock %}
"""


# ============================================================
# 10. templates/registro.html
# ============================================================

"""
{% extends "base.html" %}

{% block title %}
Registro
{% endblock %}

{% block content %}

<div class="row justify-content-center">

    <div class="col-md-5">

        <div class="card shadow">

            <div class="card-header bg-success text-white">

                <h3 class="text-center">
                    Registro de usuario
                </h3>

            </div>

            <div class="card-body">

                <form method="POST">

                    {{ form.hidden_tag() }}

                    <div class="mb-3">

                        {{ form.usuario.label(
                            class="form-label"
                        ) }}

                        {{ form.usuario(
                            class="form-control"
                        ) }}

                    </div>

                    <div class="mb-3">

                        {{ form.password.label(
                            class="form-label"
                        ) }}

                        {{ form.password(
                            class="form-control"
                        ) }}

                    </div>

                    <div class="mb-3">

                        {{ form.confirmar_password.label(
                            class="form-label"
                        ) }}

                        {{ form.confirmar_password(
                            class="form-control"
                        ) }}

                    </div>

                    <div class="d-grid">

                        {{ form.submit(
                            class="btn btn-success"
                        ) }}

                    </div>

                </form>

            </div>

        </div>

    </div>

</div>

{% endblock %}
"""


# ============================================================
# 11. templates/dashboard.html
# ============================================================

"""
{% extends "base.html" %}

{% block title %}
Dashboard
{% endblock %}

{% block content %}

<div class="text-center">

    <h1>
        Panel de Administración
    </h1>

    <p class="lead">

        Bienvenido,
        <strong>
            {{ current_user.usuario }}
        </strong>

    </p>

</div>


<div class="row mt-4">

    <div class="col-md-3 mb-3">

        <a
            href="{{ url_for('productos') }}"
            class="btn btn-primary w-100 p-3"
        >
            Productos
        </a>

    </div>


    <div class="col-md-3 mb-3">

        <a
            href="{{ url_for('clientes') }}"
            class="btn btn-success w-100 p-3"
        >
            Clientes
        </a>

    </div>


    <div class="col-md-3 mb-3">

        <a
            href="{{ url_for('proveedores') }}"
            class="btn btn-warning w-100 p-3"
        >
            Proveedores
        </a>

    </div>


    <div class="col-md-3 mb-3">

        <a
            href="{{ url_for('facturacion') }}"
            class="btn btn-info w-100 p-3"
        >
            Facturación
        </a>

    </div>

</div>


<div class="text-center mt-4">

    <a
        href="{{ url_for('logout') }}"
        class="btn btn-danger"
    >
        Cerrar sesión
    </a>

</div>

{% endblock %}
"""


# ============================================================
# 12. templates/productos.html
# ============================================================

"""
{% extends "base.html" %}

{% block title %}
Productos
{% endblock %}

{% block content %}

<h1>
    Productos
</h1>

<p>
    Usuario autenticado:
    <strong>
        {{ current_user.usuario }}
    </strong>
</p>

<table class="table table-bordered table-striped">

    <thead>

        <tr>

            <th>ID</th>
            <th>Nombre</th>
            <th>Precio</th>
            <th>Stock</th>

        </tr>

    </thead>

    <tbody>

        {% for producto in productos %}

        <tr>

            <td>
                {{ producto.id }}
            </td>

            <td>
                {{ producto.nombre }}
            </td>

            <td>
                {{ producto.precio }}
            </td>

            <td>
                {{ producto.stock }}
            </td>

        </tr>

        {% else %}

        <tr>

            <td
                colspan="4"
                class="text-center"
            >
                No existen productos registrados.
            </td>

        </tr>

        {% endfor %}

    </tbody>

</table>

{% endblock %}
"""


# ============================================================
# 13. templates/clientes.html
# ============================================================

"""
{% extends "base.html" %}

{% block title %}
Clientes
{% endblock %}

{% block content %}

<h1>
    Clientes
</h1>

<table class="table table-bordered">

    <thead>

        <tr>

            <th>ID</th>
            <th>Nombre</th>
            <th>Correo</th>
            <th>Teléfono</th>

        </tr>

    </thead>

    <tbody>

        {% for cliente in clientes %}

        <tr>

            <td>
                {{ cliente.id }}
            </td>

            <td>
                {{ cliente.nombre }}
            </td>

            <td>
                {{ cliente.correo }}
            </td>

            <td>
                {{ cliente.telefono }}
            </td>

        </tr>

        {% else %}

        <tr>

            <td
                colspan="4"
                class="text-center"
            >
                No existen clientes registrados.
            </td>

        </tr>

        {% endfor %}

    </tbody>

</table>

{% endblock %}
"""


# ============================================================
# 14. templates/proveedores.html
# ============================================================

"""
{% extends "base.html" %}

{% block title %}
Proveedores
{% endblock %}

{% block content %}

<h1>
    Proveedores
</h1>

<table class="table table-bordered">

    <thead>

        <tr>

            <th>ID</th>
            <th>Nombre</th>
            <th>Teléfono</th>
            <th>Correo</th>

        </tr>

    </thead>

    <tbody>

        {% for proveedor in proveedores %}

        <tr>

            <td>
                {{ proveedor.id }}
            </td>

            <td>
                {{ proveedor.nombre }}
            </td>

            <td>
                {{ proveedor.telefono }}
            </td>

            <td>
                {{ proveedor.correo }}
            </td>

        </tr>

        {% else %}

        <tr>

            <td
                colspan="4"
                class="text-center"
            >
                No existen proveedores registrados.
            </td>

        </tr>

        {% endfor %}

    </tbody>

</table>

{% endblock %}
"""


# ============================================================
# 15. templates/facturacion.html
# ============================================================

"""
{% extends "base.html" %}

{% block title %}
Facturación
{% endblock %}

{% block content %}

<h1>
    Facturación
</h1>

<table class="table table-bordered">

    <thead>

        <tr>

            <th>ID</th>
            <th>Cliente</th>
            <th>Producto</th>
            <th>Cantidad</th>
            <th>Total</th>

        </tr>

    </thead>

    <tbody>

        {% for factura in facturas %}

        <tr>

            <td>
                {{ factura.id }}
            </td>

            <td>
                {{ factura.cliente }}
            </td>

            <td>
                {{ factura.producto }}
            </td>

            <td>
                {{ factura.cantidad }}
            </td>

            <td>
                {{ factura.total }}
            </td>

        </tr>

        {% else %}

        <tr>

            <td
                colspan="5"
                class="text-center"
            >
                No existen facturas registradas.
            </td>

        </tr>

        {% endfor %}

    </tbody>

</table>

{% endblock %}
"""


# ============================================================
# 16. static/css/style.css
# ============================================================

"""
body {
    background-color: #f4f6f9;
}

.card {
    border-radius: 10px;
}

.navbar-brand {
    font-weight: bold;
}

h1 {
    margin-bottom: 20px;
}
"""


# ============================================================
# 17. requirements.txt
# ============================================================

"""
Flask
Flask-Login
Flask-WTF
Werkzeug
mysql-connector-python
WTForms
"""


# ============================================================
# FUNCIONAMIENTO DEL SISTEMA
# ============================================================
#
# 1. El usuario entra a /registro.
#
# 2. Introduce usuario y contraseña.
#
# 3. generate_password_hash() transforma la contraseña.
#
# 4. El hash se almacena en MySQL.
#
# 5. El usuario entra a /login.
#
# 6. Se consulta el usuario mediante SELECT.
#
# 7. check_password_hash() comprueba la contraseña.
#
# 8. Si es correcta, login_user() crea la sesión.
#
# 9. El usuario entra al dashboard.
#
# 10. @login_required protege:
#
#     /dashboard
#     /productos
#     /clientes
#     /proveedores
#     /facturacion
#
# 11. current_user permite identificar al usuario activo.
#
# 12. /logout ejecuta logout_user().
#
# 13. Después del logout, las rutas protegidas vuelven
#     a enviar al usuario hacia /login.
#
# ============================================================
