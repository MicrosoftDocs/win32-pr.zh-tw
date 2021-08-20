---
title: 從 VBScript 轉換成 JScript
description: 從 VBScript 轉換成 JScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d1b07387ce36f574131cce9ca1afda262fd2bc40fdc90359c2ec3b18b60f0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917815"
---
# <a name="translating-to-jscript-from-vbscript"></a>從 VBScript 轉換成 JScript

在 VBScript 中，**的 ...****每個** 迴圈都會列舉集合的成員;在 JScript 中， **...****in** 迴圈會列舉 JScript 物件或陣列的成員。 若要列舉 JScript 中的集合，請使用枚舉器物件。

在 JScript 中，有數種資料類型，例如數位、字串、布林值、物件，以及 null 屬性。 VBScript 只使用一種資料類型 **Variant**，可以 subtyped 來表示字串、數位、布林值等等。

在 JScript 中，您可以藉由設定陣列 length 屬性的新值來動態展開陣列。 在 VBScript 中，陣列無法放大;您必須使用 **redim** 語句來 redimensioned 它們。

VBScript 和 JScript 支援函數。 但是 VBScript 也支援副程式。 副程式類似于函式，但不會傳回值。

JScript 會區分大小寫。 VBScript 不是。

JScript Internet Explorer 和 Netscape Navigator 都受到支援。 Netscape Navigator 不支援 VBScript。

JScript 提供 Error 物件，可用來攔截和處理錯誤。 Error 物件類似于 VBScript Err 物件。

JScript 陣列不是變數類型 **VARIANT SAFEARRAY** 的陣列。 如果您的腳本從 COM 物件或 VBScript 腳本接收 **VARIANT safearray** 變數，它必須使用 VBArray 物件來存取 **variant safearray** 變數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[翻譯為 JScript](translating-to-jscript.md)
</dt> </dl>

 

 




