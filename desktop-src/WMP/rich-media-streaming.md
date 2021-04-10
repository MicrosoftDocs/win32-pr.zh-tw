---
title: 豐富的媒體串流
description: 豐富的媒體串流
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player，以網路為基礎的簡報
- Windows Media Player 物件模型，以網路為基礎的簡報
- 物件模型，以 Web 為基礎的簡報
- Windows Media Player 行動裝置、以網路為基礎的簡報
- Windows Media Player ActiveX 控制項，以 Web 為基礎的簡報
- Windows Media Player 的行動 ActiveX 控制項，以網路為基礎的簡報
- ActiveX 控制項，以網頁為基礎的簡報
- Windows Media Player，豐富的媒體串流
- Windows Media Player 物件模型，多媒體串流
- 物件模型，多媒體串流
- Windows Media Player Mobile、豐富的媒體串流
- Windows Media Player ActiveX 控制項，豐富的媒體串流
- Windows Media Player 的行動 ActiveX 控制項、豐富的媒體串流
- ActiveX 控制項，豐富的媒體串流
- 以網路為基礎的簡報，豐富的媒體串流
- 建立以網路為基礎的簡報、豐富的媒體串流
- 豐富的媒體串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674676"
---
# <a name="rich-media-streaming"></a>豐富的媒體串流

複雜的網頁包含許多通常會分開傳輸的不同元件。 在慢速連線上，這類頁面會一次顯示一段時間，而且可能需要幾分鐘的時間才能完全顯示。 這可能會讓您無法有效地將網頁與數位媒體進行同步處理。 此問題的解決方式是豐富的媒體串流，這表示將您的網頁加入數位媒體串流，以與音訊或影片資料同時提供。

豐富的媒體串流使用簡單的框架配置，其行為與一般的 URL 翻轉一樣。 如同在 URL 翻轉中，內嵌在數位媒體資料流程中的 URL 指令碼命令會用來顯示目標框架中的內容。 但是，Windows Media Player 9 系列或更新版本會使用 URL 指令碼命令來存取 Internet Explorer 快取中的檔案，而不是指向 Web 上的頁面，而是在接收到資料流程處理的 HTML 內容時，會使用 URL 指令碼命令。 如同一般的 URL 翻轉，您可以撰寫事件處理常式來回應這些 URL 指令碼命令，也可以讓 Windows Media Player 控制項自動處理所有內容。

> [!Note]  
> 透過豐富媒體串流傳遞的任何 HTML 內容都會在網際網路安全性區域中播放，並且受限於使用者的瀏覽器安全性設定。

 

如需有關建立豐富媒體簡報的詳細資訊，請參閱 Windows Media Format 9 系列或更新版本的 SDK 和 Windows Media 編碼器9系列 SDK。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Web-Based 簡報**](creating-web-based-presentations.md)
</dt> <dt>

[**使用腳本來控制 URL 翻轉**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




