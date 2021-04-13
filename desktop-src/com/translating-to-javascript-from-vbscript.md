---
title: 從 VBScript 轉換成 JavaScript
description: 從 VBScript 轉換成 JavaScript
ms.assetid: 39a712c5-f8d7-4441-a602-93cda43c24d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff950c58c87e926c8593e5c009db4efbce0a371
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300204"
---
# <a name="translating-to-javascript-from-vbscript"></a>從 VBScript 轉換成 JavaScript

在 JavaScript 中，有數種資料類型，例如數位、字串、布林值、物件，以及 null 屬性。 VBScript 只使用一種資料類型 **Variant**，可以 subtyped 來表示字串、數位、布林值等等。

在 JavaScript 中，您可以藉由設定陣列 length 屬性的新值來動態展開陣列。 在 VBScript 中，陣列無法放大;您必須使用 **redim** 語句來 redimensioned 它們。

VBScript 和 JavaScript 都支援函數。 但是 VBScript 也支援副程式。 副程式類似于函式，但不會傳回值。

JavaScript 會區分大小寫。 VBScript 不是。

JavaScript 是由各式各樣的網頁瀏覽器所支援，包括 Internet Explorer 和 Netscape Navigator。 只有 Internet Explorer 才支援 VBScript。

VBScript 透過其 Err 物件提供錯誤處理支援。 JavaScript 目前並不提供一種方式來捕捉和處理錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[翻譯為 JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




