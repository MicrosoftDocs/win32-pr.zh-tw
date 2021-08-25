---
title: 新增 Close BUTTONELEMENT
description: 新增 Close BUTTONELEMENT
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- 建立外觀，BUTTONELEMENT 元素
- Windows Media Player 的 BUTTONELEMENT 元素
- 外觀，BUTTONELEMENT 元素
- 外觀定義檔，BUTTONELEMENT 元素
- BUTTONELEMENT 元素
- 元素，BUTTONELEMENT
- 建立外觀、關閉按鈕
- Windows Media Player 的外觀、關閉按鈕
- 外觀、關閉按鈕
- 外觀定義檔，關閉按鈕
- 關閉按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5d2a85e43ae4a664504c213d182b396707ff9cfa663187e7f153fa4cc154e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765471"
---
# <a name="adding-the-close-buttonelement"></a>新增 Close BUTTONELEMENT

[關閉] 按鈕與 [播放] 按鈕的概念類似，但有不同的代碼和色彩。

將接近 **BUTTONELEMENT** 的程式碼放在播放 **BUTTONELEMENT** 的右角括弧之後。


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



下列屬性是用來定義 [關閉] 按鈕的 **BUTTONELEMENT** ：

**mappingColor**

這是您先前建立之地圖藝術檔案中區域的色彩值。 在此情況下，它是紅色的紅色色彩。 任何 **BUTTONELEMENT** 都需要這個屬性。 藉由定義此色彩，您會告訴 Windows Media Player 將此色彩區域與此按鈕的 XML 程式碼產生關聯。

**upToolTip**

這會定義當使用者將滑鼠停留在按鈕上時，將顯示的文字。 這與 [播放] 按鈕相同，不同之處在于它標示為「關閉」。

**onClick**

這會定義滑鼠按一下按鈕時所發生的事件。 這個事件屬性的值稱為「事件處理常式」（event handler），它會是 Microsoft JScript 程式碼的行，或是在 **視圖** 的 **loadScript** 屬性所載入的外部文字檔中的 JScript 函數。 在此情況下，JScript 程式碼會使用全域屬性（attribute）**視圖** 來呼叫 **view** 專案的 **close** 方法，這會關閉視圖並關閉 Windows Media Player。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立外觀定義檔**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




