# sistema_bancario
import tkinter as tk

# Função para adicionar aluno à lista
def add_client():
    name = name_entry.get()
    address = address_entry.get()
    add_client_class = class_entry.get()

    if name and address and student_class:
        student_data = f"Nome: {name}, Endereço: {address}, Turma: {student_class}"
        students.append(student_data)

        # Limpar os campos de entrada
        name_entry.delete(0, tk.END)
        address_entry.delete(0, tk.END)
        class_entry.delete(0, tk.END)
    else:
        print("Por favor, preencha todos os campos!")

# Função para exibir lista de alunos
def show_students():
    text_area.delete(1.0, tk.END)
    for student in students:
        text_area.insert(tk.END, student + "\n")

# Configuração da janela principal
janela = tk.Tk()
janela.title("Cadastro de Alunos")
janela.geometry("400x400")

# Lista para armazenar os dados dos alunos
students = []

# Campos para entrada de dados
tk.Label(janela, text="Nome:").pack()
name_entry = tk.Entry(janela)
name_entry.pack()

tk.Label(janela, text="Endereço:").pack()
address_entry = tk.Entry(janela)
address_entry.pack()

tk.Label(janela, text="Turma:").pack()
class_entry = tk.Entry(janela)
class_entry.pack()

# Botão para cadastrar aluno
tk.Button(janela, text="Cadastrar", command=add_student).pack(pady=10)

# Botão para exibir lista de alunos
tk.Button(janela, text="Exibir Lista", command=show_students).pack(pady=10)

# Área de texto para exibir a lista de alunos
text_area = tk.Text(janela, width=50, height=10)
text_area.pack(pady=10)

# Iniciando o loop principal
janela.mainloop()



[![](https://mermaid.ink/img/pako:eNqVkk1O5DAQha9S8pq-QBYjQYeGZkBCwAYlLAq70m0R26FsNxoQhxnNYg4wmhP0xcZ2En4kNpNVnLz66r1yvQjpFIlKdL17klvkADd1ayE9h83lLdyjfbiDxeIbHDVXhAoMgXQG0MPA2ko9oPbQRbv_vf9LHhA8MRmQrFGhvxtRR4WwbM61DwiKgOkxaq-DSxhkhGjgPlETR2pn0ZANDpQDHHotMeidm0jLQqqbZeIzKI0bRlOQV-_IrwrrUnjc1OTJ7ly_IwaX40mXqxUqN7s9LtLV1EPu_yi9yVR6z5mUo3ZVtCfNCp8L8KOjJfrCjn42cVLUp80NpTnwW9xep_Y0t_8IXn_y27GzYUFWVbC2gbhDSdP8fNz_ZD33WZfis7mPzFcReDIzKj0Q6AzBlOhX-oXjMTM_GTktrO_N4cDZSpj1Li2AG7OudM7wnEY4VZ79Z404EIbYoFZpE18yoxVhS4ZaUaVXRR3GPrSita9JijG46x9WiipwpAPBLm62ouqw9-kUB4WB6vEe3r6SSpvBF-Oul5V__QexlQb7?type=png)](https://mermaid.live/edit#pako:eNqVkk1O5DAQha9S8pq-QBYjQYeGZkBCwAYlLAq70m0R26FsNxoQhxnNYg4wmhP0xcZ2En4kNpNVnLz66r1yvQjpFIlKdL17klvkADd1ayE9h83lLdyjfbiDxeIbHDVXhAoMgXQG0MPA2ko9oPbQRbv_vf9LHhA8MRmQrFGhvxtRR4WwbM61DwiKgOkxaq-DSxhkhGjgPlETR2pn0ZANDpQDHHotMeidm0jLQqqbZeIzKI0bRlOQV-_IrwrrUnjc1OTJ7ly_IwaX40mXqxUqN7s9LtLV1EPu_yi9yVR6z5mUo3ZVtCfNCp8L8KOjJfrCjn42cVLUp80NpTnwW9xep_Y0t_8IXn_y27GzYUFWVbC2gbhDSdP8fNz_ZD33WZfis7mPzFcReDIzKj0Q6AzBlOhX-oXjMTM_GTktrO_N4cDZSpj1Li2AG7OudM7wnEY4VZ79Z404EIbYoFZpE18yoxVhS4ZaUaVXRR3GPrSita9JijG46x9WiipwpAPBLm62ouqw9-kUB4WB6vEe3r6SSpvBF-Oul5V__QexlQb7)