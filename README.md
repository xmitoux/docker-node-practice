# Vue 3 テンプレート

-   Vue 3用のテンプレートリポジトリです。
-   試す場合は右上の**Use this template**から**Create a new repository**を選択し、新しくリポジトリを作ってください。

## 構成

Vite + Vue 3 + TypeScript + ESLint + Prettier

## クイックスタート

※パッケージ管理に`pnpm`を使用します。なければ[こちら](https://pnpm.io/ja/installation)からインストールしてください。

```
pnpm i
pnpm run dev
```

## デプロイ

-   [Vercel](https://vercel.com/)にデプロイすることで簡単にWeb公開が可能です。
-   このリポジトリをデプロイしたページ → [https://vue3-template-psi.vercel.app/](https://vue3-template-xmitoux.vercel.app/)

### 手順

1. Vercelに登録し、GitHubアカウントを連携します。
2. \***\*Overview\*\***右上の\***\*Add New Project\*\***を選択します。
3. \***\*Import Git Repository\*\***内にあるこのテンプレートから作成したリポジトリを選択します。
4. \***\*Build and Output Settings\*\***の\***\*Build Command\*\***を`pnpm run build`、**Install Command**を`pnpm install`に設定します。
5. **Deploy**を押せばデプロイ完了です。

## VSCode設定

-   エディタにはVSCodeを使用します。
-   以下の拡張機能のインストールが必要です。
    -   Volar: Vueのコーディングに必須
    -   ESLint: JS, TS用のlinter
    -   Prettier: コードフォーマッタ
    <details>
    <summary>Vite Orginal README</summary>

# Vue 3 + TypeScript + Vite

This template should help get you started developing with Vue 3 and TypeScript in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

-   [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Type Support For `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) to make the TypeScript language service aware of `.vue` types.

If the standalone TypeScript plugin doesn't feel fast enough to you, Volar has also implemented a [Take Over Mode](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669) that is more performant. You can enable it by the following steps:

1. Disable the built-in TypeScript Extension
    1. Run `Extensions: Show Built-in Extensions` from VSCode's command palette
    2. Find `TypeScript and JavaScript Language Features`, right click and select `Disable (Workspace)`
2. Reload the VSCode window by running `Developer: Reload Window` from the command palette.

</details>
