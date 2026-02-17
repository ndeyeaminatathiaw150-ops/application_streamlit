import streamlit as st

st.title("Calculateur d'IMC")

st.write("Entrez vos informations pour calculer votre IMC.")

# Entrées utilisateur
poids = st.number_input("Poids (en kg)", min_value=0.0, step=0.1)
taille = st.number_input("Taille (en mètres)", min_value=0.0, step=0.01)

# Bouton de calcul
if st.button("Calculer IMC"):
    if taille > 0:
        imc = poids / (taille ** 2)
        st.success(f"Votre IMC est : {imc:.2f}")

        # Interprétation
        if imc < 18.5:
            st.info("Insuffisance pondérale")
        elif imc < 25:
            st.info("Poids normal")
        elif imc < 30:
            st.warning("Surpoids")
        else:
            st.error("Obésité")
    else:
        st.error("Veuillez entrer une taille valide.")
