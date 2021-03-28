---
description: 內嵌字型是將檔和其包含的字型組合到檔案中，以傳輸到另一部電腦的技術。
ms.assetid: ded409f1-5bd9-411b-b905-fc49c484786a
title: 內嵌字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb8ab821afa5f44ded05a4a61a53439b8db9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114665"
---
# <a name="embedded-fonts"></a>內嵌字型

內嵌字型是將檔和其包含的字型組合到檔案中，以傳輸到另一部電腦的技術。 內嵌字型可保證傳送檔案中指定的字型，將會出現在接收檔案的電腦上。 不過，並非所有字型都可以從電腦移到電腦，因為大部分的字型一次只授權給一部電腦。 只有 TrueType 和 OpenType 字型可以內嵌。

應用程式應該只在使用者要求時，才將字型嵌入檔中。 應用程式無法和包含內嵌字型的檔一起散發，也不能讓應用程式本身包含內嵌字型。 只要應用程式散佈任何格式的字型，就必須確認字型擁有者的專屬許可權。

可能違反字型廠商的專利權利或使用者授權合約，以內嵌不允許內嵌的任何字型，或無法觀察下列內嵌字型的指導方針。 字型的授權可能只會提供要在目的地電腦上安裝和使用之字型的讀取/寫入權限。 或授權可能會授與唯讀許可權。 [唯讀] 許可權可讓您將檔 (查看和列印，但不能由目的地電腦) 修改;具有唯讀內嵌字型的檔本身是唯讀的。 唯讀內嵌字型可能無法從檔解除捆搭，並安裝在目的地電腦上。

應用程式可以藉由呼叫 [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)函式，並檢查 [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica)結構的 **otmfsType** 成員，來判斷授權狀態。 如果設定了 **otmfsType** 的位1，字型就不允許內嵌。 如果 bit 1 為 clear，則可以內嵌字型。 如果設定了位2，則內嵌是唯讀的。

若要內嵌 TrueType 字型，應用程式可以使用 [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata) 函式來讀取字型檔案。 將 [**GetFontData**](/windows/win32/api/wingdi/nf-wingdi-getfontdata)的 *dwTable* 和 *dwOffset* 參數設定為0L，並將 *cbData* 參數設定為1L，可確保應用程式從一開始就讀取整個字型檔案。

有幾個函式可用來根據字元寬度以及字型資料所在的位置，來內嵌 OpenType 字型。 若要內嵌位於裝置內容中的 OpenType Unicode 字型，應用程式可以使用 [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)。 若要內嵌位於裝置內容中的 OpenType UCS-4 字型，應用程式可以使用 [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)。 若要內嵌位於字型檔案中的 OpenType Unicode 字型，應用程式可以使用 [**TTEmbedFontFromFile**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)。 如需 OpenType 字型內嵌的詳細資訊，請參閱 [字體內嵌參考](font-embedding-reference.md)。

在應用程式抓取字型資料之後，可以使用任何適用的格式，將資料儲存在檔中。 大部分的應用程式會在檔中建立字型目錄、列出內嵌字型，以及內嵌是可讀寫或唯讀的。 應用程式可以使用 [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica)結構的 **otmpStyleName** 和 **otmFamilyName** 成員來識別字型。

如果已針對內嵌字型設定唯讀位，則應用程式在將字型資料儲存在檔之前，必須先將其加密。 加密方法不需要複雜;例如，使用 XOR 運算子將字型資料與應用程式定義的常數結合，是足夠且快速的。

 

 
