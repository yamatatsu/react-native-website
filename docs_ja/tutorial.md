---
id: tutorial
title: Learn the Basics
---

> React Native is like React, but it uses native components instead of web components as building blocks. So to understand the basic structure of a React Native app, you need to understand some of the basic React concepts, like JSX, components, `state`, and `props`. If you already know React, you still need to learn some React-Native-specific stuff, like the native components. This tutorial is aimed at all audiences, whether you have React experience or not.

React NativeはReactと似ていますが、Webコンポーネントの代わりにネイティブコンポーネントをビルディングブロックとして使用しています。 したがって、Reactネイティブアプリの基本構造を理解するためには、JSX、コンポーネント、状態、および小道具のような基本的なReactの概念を理解する必要があります。 あなたがすでにReactを知っているなら、あなたはまだネイティブコンポーネントのようなReact-Native特有のものを学ぶ必要があります。 このチュートリアルは、あなたがリアクションの経験を持っているかどうかにかかわらず、すべての観客を対象としています。

Let's do this thing.

## Hello World

In accordance with the ancient traditions of our people, we must first build an app that does nothing except say "Hello world". Here it is:

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { AppRegistry, Text } from 'react-native';

export default class HelloWorldApp extends Component {
  render() {
    return (
      <Text>Hello world!</Text>
    );
  }
}

// skip this line if using Create React Native App
AppRegistry.registerComponent('AwesomeProject', () => HelloWorldApp);
```

If you are feeling curious, you can play around with sample code directly in the web simulators. You can also paste it into your `App.js` file to create a real app on your local machine.

## What's going on here?

Some of the things in here might not look like JavaScript to you. Don't panic. _This is the future_.

First of all, ES2015 (also known as ES6) is a set of improvements to JavaScript that is now part of the official standard, but not yet supported by all browsers, so often it isn't used yet in web development. React Native ships with ES2015 support, so you can use this stuff without worrying about compatibility. `import`, `from`, `class`, `extends`, and the `() =>` syntax in the example above are all ES2015 features. If you aren't familiar with ES2015, you can probably pick it up just by reading through sample code like this tutorial has. If you want, [this page](https://babeljs.io/learn-es2015/) has a good overview of ES2015 features.

The other unusual thing in this code example is `<Text>Hello world!</Text>`. This is JSX - a syntax for embedding XML within JavaScript. Many frameworks use a special templating language which lets you embed code inside markup language. In React, this is reversed. JSX lets you write your markup language inside code. It looks like HTML on the web, except instead of web things like `<div>` or `<span>`, you use React components. In this case, `<Text>` is a built-in component that just displays some text.

ここにあるものの中にはJavaScriptのように見えないものもあります。慌てないでください。これは未来です。

まず第一に、ES2015（ES6とも呼ばれる）は、公式規格の一部ではあるがまだすべてのブラウザでサポートされていないJavaScriptの改良セットであるため、Web開発ではまだ使用されていません。 React Native ships は ES2015をサポートしているので、互換性について心配することなくこの材料を使用できます。 import、from、class、extends、および上記の例のラムダ構文はすべてES2015の機能です。 ES2015に精通していない場合は、このチュートリアルのようなサンプルコードを読み込むだけで簡単に理解できます。必要に応じて、このページにはES2015の機能の概要があります。

このコード例の他の珍しいものは、<Text> Hello world！</ Text>です。 JSX - JavaScript内にXMLを埋め込むための構文です。多くのフレームワークでは特別なテンプレート言語を使用しています。この言語を使用すると、マークアップ言語内にコードを埋め込むことができます。リアクションでは、これは逆です。 JSXでは、コード内にマークアップ言語を記述できます。 <div>や<span>のようなWebの代わりに、Reactコンポーネントを使用する以外は、Web上のHTMLのように見えます。この場合、<Text>はテキストだけを表示するビルトインコンポーネントです。

## Components

So this code is defining `HelloWorldApp`, a new `Component`. When you're building a React Native app, you'll be making new components a lot. Anything you see on the screen is some sort of component. A component can be pretty simple - the only thing that's required is a `render` function which returns some JSX to render.

## This app doesn't do very much

Good point. To make components do more interesting things, you need to [learn about Props](props.md).
