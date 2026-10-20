function calcularIMC(peso, altura) {
if (typeof peso !== "number" || typeof altura !== "number" || peso <= 0 || altura <= 0) {
throw new Error("El peso y la altura deben ser números mayores que 0.");
}

    return peso / (altura * altura);

}

function clasificarIMC(imc) {
if (imc < 18.5) {
return "Bajo peso";
} else if (imc < 25) {
return "Normal";
} else if (imc < 30) {
return "Sobrepeso";
} else {
return "Obesidad";
}
}

// Ejemplo
try {
const peso = 70;
const altura = 1.75;

    const imc = calcularIMC(peso, altura);

    console.log("IMC:", imc.toFixed(2));
    console.log("Clasificación:", clasificarIMC(imc));

} catch (error) {
console.log("Error:", error.message);
}
