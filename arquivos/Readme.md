# Arquivos

```java
public class Arquivo {

    public boolean writeStringToFile(String nomeDoArquivo, String texto) {
        File arquivo = new File(nomeDoArquivo);

        try (FileWriter fwArquivo = new FileWriter(arquivo, arquivo.exists());
             BufferedWriter bwArquivo = new BufferedWriter(fwArquivo);
        ) {
            bwArquivo.write(texto + "\n");
        } catch (IOException e) {
            e.printStackTrace();
        }

        return false;
    }

    public void lerArquivo(String nomeDoArquivo) {
        File arquivo = new File(nomeDoArquivo);

        try {
            Scanner leitor = new Scanner(arquivo);

            while (leitor.hasNextLine()) {
                String linha = leitor.nextLine();
                System.out.println(linha);
            }
            leitor.close();
        } catch (FileNotFoundException e) {
            e.printStackTrace();
        }
    }

    public void SalvarPessoaEmDisco(String nomeDoArquivo, Pessoa p) {
        try (FileOutputStream fout = new FileOutputStream(new File(nomeDoArquivo));
             ObjectOutputStream oos = new ObjectOutputStream(fout);
        ) {

            oos.writeObject(p);

        } catch (FileNotFoundException e) {
            e.printStackTrace();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }

    public void lerPessoaDoDisco(String nomeDoArquivo) {
        try (FileInputStream fin = new FileInputStream(new File(nomeDoArquivo));
             ObjectInputStream ois = new ObjectInputStream(fin);
        ) {

            Pessoa nova = (Pessoa) ois.readObject();

        } catch (FileNotFoundException e) {
            e.printStackTrace();
        } catch (IOException e) {
            e.printStackTrace();
        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        }
    }

    public void SalvarAgendaEmDisco(String nomeDoArquivo, ArrayList<Pessoa> p) {
        try (FileOutputStream fout = new FileOutputStream(new File(nomeDoArquivo));
             ObjectOutputStream oos = new ObjectOutputStream(fout);
        ) {

            oos.writeObject(p);

        } catch (FileNotFoundException e) {
            e.printStackTrace();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }

    public ArrayList<Pessoa> lerAgendaDoDisco(String nomeDoArquivo) {
        try (FileInputStream fin = new FileInputStream(new File(nomeDoArquivo));
             ObjectInputStream ois = new ObjectInputStream(fin);
        ) {

            ArrayList<Pessoa> nova = (ArrayList<Pessoa>) ois.readObject();
            return nova;

        } catch (FileNotFoundException e) {
            e.printStackTrace();
        } catch (IOException e) {
            e.printStackTrace();
        } catch (ClassNotFoundException e) {
            e.printStackTrace();
        }
        return null;
    }
}
```
