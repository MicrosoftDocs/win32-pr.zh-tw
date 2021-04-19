---
title: 使用 Win32 和 c + +) 開始的滑鼠輸入 (
description: 滑鼠輸入
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a560baf110892ba1b8f277c55fc124888b62b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106966074"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>使用 Win32 和 c + +) 開始的滑鼠輸入 (

Windows 最多可支援具有五個按鈕的滑鼠：左方、中間和右邊，還有兩個額外的按鈕，稱為 XBUTTON1 和 XBUTTON2。

![顯示左 (1) 、右邊 (2) 、中間 (3) 和 xbutton1 (4) 按鈕的圖例。](images/mouse.png)

Windows 大部分的滑鼠都至少有左方和右邊的按鈕。 滑鼠左鍵用於指標、選取、拖曳等等。 滑鼠右鍵通常會顯示內容功能表。 有些滑鼠具有滾輪，位於左右按鈕之間。 視滑鼠的不同，滾輪也可以按一下，使其成為中間按鈕。

[XBUTTON1] 和 [XBUTTON2] 按鈕通常位於靠近基底之滑鼠的側邊。 這些額外的按鈕不會出現在所有滑鼠上。 如果有的話，XBUTTON1 和 XBUTTON2 按鈕通常會對應到應用程式函式，例如在網頁瀏覽器中向前和向後流覽。

左邊的使用者通常會發現，更適合用來交換左右按鈕的函式（使用右按鈕做為指標），以及使用左側按鈕顯示操作功能表。 基於這個理由，Windows 說明文件會使用 [ *主要] 按鈕* 和 *次要按鈕* 來參考邏輯函式，而不是實體放置。 在預設的 (右手) ] 設定中，左側按鈕是主要按鈕，右邊是次要按鈕。 不過，以 *滑鼠右鍵按一下* ，然後 *按一下滑鼠左鍵* ，則會參考邏輯動作。 以 *滑鼠右鍵按一下* 是指按一下主要按鈕，該按鈕是在滑鼠的右方或左邊。

不論使用者如何設定滑鼠，Windows 都會自動轉譯滑鼠訊息，使其一致。 使用者可以在使用您的程式時交換主要和次要按鈕，而不會影響您的程式列為。

MSDN 檔使用 [將詞彙 *右移* ] 按鈕和 [ *左] 按鈕* ，以表示 *主要* 和 *次要* 按鈕。 這項術語與滑鼠輸入的視窗訊息名稱一致。 請記住，實體的左和右按鈕可能會被交換。

## <a name="next"></a>下一個

[回應滑鼠點擊](mouse-clicks.md)

 

 




