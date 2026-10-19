# Instalação — GitHub Profile FS SYSTEMS v2

Repositório de destino: https://github.com/fesalvian/fesalvian

## Método mais fácil — Git + VS Code

```powershell
git clone https://github.com/fesalvian/fesalvian.git
cd fesalvian
```

Extraia **o conteúdo** deste ZIP dentro da pasta `fesalvian/`, mantendo a estrutura de diretórios e confirmando a substituição dos arquivos de mesmo nome. O README foi baseado na versão que já está publicada; antes de sobrescrever, preserve quaisquer alterações suas posteriores.

```powershell
git status
git add README.md hud-banner.svg assets/ .github/workflows/profile-3d.yml profile-3d-contrib/
git commit -m "feat: add project hangar, hardware lab, boot terminal and 3D contributions"
git push origin main
```

## Ligar o calendário 3D

1. Abra https://github.com/fesalvian/fesalvian/actions .
2. Habilite Actions no repositório se solicitado.
3. Clique em **GitHub Profile | 3D Contributions**.
4. Clique em **Run workflow** e confirme a execução na branch `main`.
5. Ao terminar, a Action substitui `profile-3d-contrib/profile-night-view.svg` (que começa como uma tela de inicialização) pelo calendário com dados reais. A partir daí, tenta atualizar diariamente.

Se o passo de commit/push falhar por permissão, confira **Settings → Actions → General → Workflow permissions** e a política do repositório. Em algumas configurações é necessário selecionar **Read and write permissions**. O arquivo workflow já pede `contents: write`.

## Arquivos usados

- `README.md`: perfil completo.
- `hud-banner.svg`: banner anterior, preservado no local onde seu GitHub já o usa.
- `assets/boot-terminal.svg`: console de inicialização animado.
- `assets/project-hangar.svg`: visualização do hangar.
- `assets/hardware-lab.svg`: ilustração técnica de hardware (não são fotos de protótipos reais).
- `.github/workflows/profile-3d.yml`: execução manual e diária do gerador.
- `profile-3d-contrib/profile-night-view.svg`: imagem inicial substituída pela Action.

**Nota:** SVGs são animações renderizadas como imagens. GitHub pode limitar certos efeitos; os SVGs continuam legíveis estáticos. A geração do gráfico depende de GitHub Actions estar habilitado.
