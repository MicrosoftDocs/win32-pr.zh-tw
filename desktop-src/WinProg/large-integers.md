---
title: 大型整數
description: 大型整數函式和結構最初提供32位 Windows 上64位值的支援。
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- 大型整數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106984942"
---
# <a name="large-integers"></a>大型整數

大型整數函式和結構最初提供32位 Windows 上64位值的支援。 現在，您的 C 編譯器可能會以原生方式支援64位的整數。 例如，Microsoft Visual C++ 支援 [**\_ \_ int64**](/windows/desktop/Midl/--int64)大小的整數類型。 如需詳細資訊，請參閱 C 編譯器隨附的檔。

如需64位 Windows 上64位整數的詳細資訊，請參閱 [新的資料類型](/windows/desktop/WinProg64/the-new-data-types)。

## <a name="large-integer-operations"></a>大型整數運算

應用程式可以使用 [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) 和 [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) 函數，將帶正負號或不帶正負號的32位整數（產生64位結果）相乘。 應用程式可以使用 [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)、 [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)和 [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) 函式，將64位值中的位轉換成左方或右方。 這些函式提供邏輯和算術移位。

應用程式也可以使用 [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) 函數，在單一作業中將32位值相乘和相除。 雖然作業的結果是32位的值，但函數會將中繼結果儲存為64位值，如此一來，當將大型32位值相乘和相除時，資訊就不會遺失。

## <a name="large-integer-reference"></a>大型整數參考

-   [大型整數函數](large-integer-functions.md)
-   [大型整數結構](large-integer-structures.md)

 

 