---
title: 從 JavaScript 轉換成 VBScript
description: 從 JavaScript 轉換成 VBScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6138a6d13710e87ae2b80c979b208d0360e28501ce5d763546a1605c49f0802a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047736"
---
# <a name="translating-to-vbscript-from-javascript"></a>從 JavaScript 轉換成 VBScript

在 JavaScript 中，有數種資料類型，例如數位、字串、布林值、物件，以及 null 屬性。 VBScript 只使用一種資料類型 **Variant**，可以 subtyped 來表示字串、數位、布林值等等。

在 JavaScript 中，您可以藉由設定陣列 length 屬性的新值來動態展開陣列。 在 VBScript 中，陣列無法放大;您必須使用 **redim** 語句來 redimensioned 它們。

VBScript 和 JavaScript 都支援函數。 但是 VBScript 也支援副程式。 副程式類似于函式，不同之處在于它們不會傳回值。

JavaScript 會區分大小寫。 VBScript 不是。

JavaScript 是由各式各樣的網頁瀏覽器所支援，包括 Internet Explorer 和 Netscape Navigator。 Netscape Navigator 不支援 VBScript。

VBScript 透過其 Err 物件支援錯誤處理。 JavaScript 目前並不提供一種方式來捕捉和處理錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[翻譯為 VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




