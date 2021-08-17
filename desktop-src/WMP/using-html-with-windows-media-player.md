---
title: 使用 HTML 搭配 Windows Media Player
description: 使用 HTML 搭配 Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player、HTML
- Windows Media Player 物件模型，HTML
- 物件模型、HTML
- Windows Media Player ActiveX 控制項、物件模型的 HTML
- ActiveX 控制項，物件模型的 HTML
- Windows Media PlayerMobile ActiveX 控制項，物件模型的 HTML
- Windows Media Player行動，HTML 物件模型
- 具有 Windows Media Player 的 HTML
- 網頁嵌入、HTML
- 內嵌、網頁
- 指令碼命令
- URL 翻轉
- 豐富的媒體串流
- 瀏覽器支援
- 顯示網頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72185dec8ae9a2119d8c3218478e7ebb5a2df4d7740b25c9f4ecc016aa392e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465918"
---
# <a name="using-html-with-windows-media-player"></a>使用 HTML 搭配 Windows Media Player

## <a name="overview"></a>概觀

使用 HTML 搭配 Windows Media Player 是結合音訊和影片與文字和圖形的絕佳方式。 當您想要補充您的靜態內容或建立具有數位媒體的 Web 應用程式時，可以在網頁中內嵌 Windows Media Player 控制項。 另一方面，如果您想要使用 HTML 來補充您的數位媒體，您可以在 Windows 的 media 中繼檔播放清單中參考網頁，以播放程式的完整模式顯示網頁。

如果您撰寫的自訂程式是以遠端模式內嵌 Windows Media Player 控制項，您也可以在使用者取消停駐控制項時，控制播放程式完整模式的各種窗格中所顯示的網頁。 這可讓您維持停駐和停駐狀態之間的持續性。

## <a name="web-embedding"></a>Web 嵌入

您可以使用 Windows Media Player 控制項做為您所建立網頁的一部分。 請參閱[將 Windows Media Player 控制項內嵌到網頁中](embedding-the-windows-media-player-control-in-a-web-page.md)。

## <a name="script-commands-and-url-flipping"></a>指令碼命令和 URL 翻轉

指令碼命令是文字/值組，您可以將它內嵌在數位媒體檔案或資料流程中。 您可以單獨使用自訂指令碼命令來觸發腳本，同時讓 Windows Media Player 自動處理其他指令碼命令。

當您有數個隨附數位媒體簡報的網頁時，[URL 腳本] 命令可以在 Windows Media Player 控制項繼續于另一個框架中播放數位媒體時，自動變更一個框架中的頁面。 這稱為 URL 翻轉，是建立多媒體投影片放映的絕佳方式。 其他自動處理的指令碼命令可讓您將播放切換至不同的媒體檔案或資料流程、顯示字幕文字，或觸發事件（例如 Windows 媒體中繼檔播放清單中定義的廣告插入）。

如需有關 URL 翻轉的詳細資訊，請參閱 [建立 Web-Based 簡報](creating-web-based-presentations.md)。

## <a name="rich-media-streaming"></a>豐富的媒體串流

URL 翻轉最適合用於快速載入的簡單頁面。 使用更複雜的頁面時，會個別傳送多個元件，因此很難將頁面顯示與數位媒體進行同步處理。 若要允許複雜的多媒體簡報，可將網頁新增至媒體資料流程，並以音訊和影片的相同方式傳送至播放機。 這可讓您更輕鬆地同步處理簡報的元件，尤其是透過低速連接。

如需豐富媒體串流處理的詳細資訊，請參閱 [建立 Web-Based 簡報](creating-web-based-presentations.md)。

## <a name="browser-support"></a>瀏覽器支援

您可以在 Microsoft Internet Explorer、Firefox 和 Netscape Navigator 中內嵌 Windows Media Player 控制項，不過每個程式的流程稍微不同。 您也可以建立設計來與這三個瀏覽器搭配使用的網頁。

使用 Internet Explorer 和 Firefox，您可以使用 HTML 物件元素內嵌控制項。 不過，導覽器需要不同的方法，因為它不會直接支援 ActiveX 控制項。 使用 [導覽器] 時，您可以使用 APPLET 元素，將特殊的 JAVA 小程式內嵌到頁面中。 此小程式可處理與玩家 ActiveX 控制項的通訊。

如需 firefox 支援的詳細資訊，請參閱搭配[firefox 使用 Windows Media Player 控制項](using-the-windows-media-player-control-with-firefox.md)。

如需 Netscape Navigator 支援的詳細資訊，請參閱[使用 Windows Media Player 搭配 Netscape 7.1](using-windows-media-player-with-netscape-7-1.md)。

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>在播放程式的完整模式中顯示網頁

您可以擴充 Windows Media Player 的功能，或在播放程式的完整模式中顯示網頁，以提供數位媒體隨附之資訊的自訂觀點。 這是 Windows 媒體中繼檔的 HTMLView 功能。 中繼檔可讓您充分掌控播放清單的內容，讓您能夠順暢地在剪輯之間轉換、插入廣告，以及在 Windows Media Player 中顯示靜止的影像。 若要在播放程式的完整模式中顯示網頁，您可以使用 PARAM 元素，將 URL 參考新增至播放清單專案或整個播放清單。

如需有關在中繼檔中使用網頁的詳細資訊，請參閱[在 Windows Media Player 中顯示網頁](displaying-web-pages-in-windows-media-player.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Player 物件模型**](about-the-player-object-model.md)
</dt> </dl>

 

 




