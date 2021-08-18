---
title: 從 JScript 轉換成 JavaScript
description: 從 JScript 轉換成 JavaScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c4adb5827952cc9bab0dac268997b5b73a52ecd1403e5431cdb3939b08c7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129580"
---
# <a name="translating-to-javascript-from-jscript"></a>從 JScript 轉換成 JavaScript

JScript 大多與 JavaScript 相容。 不過，JScript 包含一些 JavaScript 目前不支援的物件，例如 ActiveXObject、列舉值、Error、Global 和 VBArray。

JScript 版本5.0 透過 **try** 支援例外狀況處理 .。。**catch** 語句。 JavaScript 目前未提供錯誤處理機制。

使用 JScript 或 JavaScript 時，各種網頁瀏覽器所支援的物件模型執行之間有一些細微的差異。 若要撰寫在 Internet Explorer 和 Netscape Navigator 上執行的腳本，請將腳本所使用的功能限制為全球資訊網協會 (W3C) [standard for HTML 3.2 版](https://www.w3.org/tr/rec-html32.html)中指定的功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[翻譯為 JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




