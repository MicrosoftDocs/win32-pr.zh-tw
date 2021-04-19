---
description: 您可以使用 HRECOGNIZER 控制碼和辨識器內容（HRECOCONTEXT 控制碼）來參考筆墨辨識器。辨識器動態連結程式庫 (DLL) 可以針對多個語言執行辨識器。
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER 和 HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992001"
---
# <a name="hrecognizer-and-hrecocontext"></a>HRECOGNIZER 和 HRECOCONTEXT

您可以使用 [HRECOGNIZER](hrecognizer-handle.md) 控制碼和辨識器內容（ [HRECOCONTEXT](hrecocontext-handle.md) 控制碼）來參考筆墨辨識器。

辨識器動態連結程式庫 (DLL) 可以針對多個語言執行辨識器。 如果是的話，在應用程式中建立 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) 物件時，會使用所傳入的 CLSID 來選取每種語言。 此外，辨識器 DLL 可以在載入時建立多個辨識器控制碼，每個辨識的語言會有一或多個。

建立辨識器內容以表示辨識特定筆跡的事件。 建立內容時，會將相關聯的辨識器物件控制碼傳遞至 [**CreateCoNtext**](/windows/desktop/api/recapis/nf-recapis-createcontext) 函式。 這會使語言與辨識器內容產生關聯。

辨識器內容可能代表電子郵件內文中所有筆墨的辨識、應用程式中單一欄位的筆墨，或 Tablet PC 輸入面板中書寫的單一文字行。 單一辨識器內容中的筆跡數量可能會因單一筆劃和整個頁面的不同而不同。

辨識器內容是由的設定所定義：

-   辨識指南。
-   任何 factoids。
-   任何旗標。
-   文字內容。
-   任何單字清單。
-   字元自動完成模式。

辨識器內容的控制碼會傳遞至所有使用這些設定的函式。 變更設定會變更辨識器內容。

應用程式可能會使用數個內容來辨識螢幕不同部分的筆墨。 個別內容可以辨識多行文字。 不過，個別內容無法處理並排寫入的兩個段落，例如報紙文章中的多個資料行。

若要辨識新筆墨，請建立新的內容。 或者，您也可以使用 [**CloneCoNtext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) 函式來製作沒有筆墨和結果的內容複本，或使用 [**ResetCoNtext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) 函式來清除其筆跡和結果的內容。 使用這些方法時，筆跡應用程式可以重複使用內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**SetGuide 函式**](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[**GetGuide 函式**](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[**SetFactoid 函式**](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[**SetFlags 函式**](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[**SetEnabledUnicodeRanges 函式**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[**GetEnabledUnicodeRanges 函式**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[**SetCACMode 函式**](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[**SetTextCoNtext 函式**](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[**SetWordList 函式**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



