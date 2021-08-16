---
title: 從 JavaScript 翻譯為 JScript
description: 從 JavaScript 翻譯為 JScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c25276d569c5b461693a666d1bf8cf706b6896c0995972e1d2af0071c5760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129560"
---
# <a name="translating-to-jscript-from-javascript"></a>從 JavaScript 翻譯為 JScript

JScript 大多與 JavaScript 相容。 不過，JScript 5.0 版包含一些 JavaScript 目前不支援的物件，例如 ActiveXObject、列舉值、Error、Global 和 VBArray。

JScript 5.0 透過 **try** 支援例外狀況處理 .。。**catch** 語句。 JavaScript 目前未提供錯誤處理機制。

使用 JScript 或 JavaScript 時，各種網頁瀏覽器所支援的物件模型執行之間有一些細微的差異。 若要撰寫在 Internet Explorer 和 Netscape Navigator 上執行的腳本，請將腳本所使用的功能限制為全球資訊網協會 (W3C) standard for HTML 3.2 版中指定的功能。 如需此標準的詳細資訊，請參閱 [HTML 3.2 參考規格](https://www.w3.org/TR/REC-html32.html)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[翻譯為 JScript](translating-to-jscript.md)
</dt> </dl>

 

 




