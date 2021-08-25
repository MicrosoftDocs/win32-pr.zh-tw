---
title: 從 JScript 轉換成 VBScript
description: 從 JScript 轉換成 VBScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3900ba82b258e6ee19cf06edb2f97247033778da5fcabaffe4a854e66a5fef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992248"
---
# <a name="translating-to-vbscript-from-jscript"></a>從 JScript 轉換成 VBScript

在 VBScript 中，**的 ...****每個** 迴圈都會列舉集合的成員;在 JScript 中， **...****in** 迴圈會列舉 JScript 物件或陣列的成員。 若要列舉 JScript 中的集合，請使用枚舉器物件。

JScript 提供 Error 物件，可用來攔截和處理錯誤。 Error 物件類似于 VBScript Err 物件。

在 JScript 中，有數種資料類型，例如數位、字串、布林值、物件，以及 null 屬性。 VBScript 只使用一種資料類型 **Variant**，可以 subtyped 來表示字串、數位、布林值等等。

在 JScript 中，您可以藉由設定陣列 length 屬性的新值來動態展開陣列。 在 VBScript 中，陣列無法放大;您必須使用 **redim** 語句來 redimensioned 它們。

VBScript 和 JScript 支援函數。 但是 VBScript 也支援副程式。 副程式類似于函式，但不會傳回值。

JScript 會區分大小寫。 VBScript 不是。

JScript 是由各式各樣的網頁瀏覽器所支援，包括 Internet Explorer 和 Netscape Navigator。 Netscape Navigator 不支援 VBScript。

JScript 陣列不是變數類型 **VARIANT SAFEARRAY** 的陣列。 JScript 腳本必須使用 VBArray 物件來存取 **VARIANT SAFEARRAY** 變數。 VBScript 腳本可以直接存取 **VARIANT SAFEARRAY** 變數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[翻譯為 VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




