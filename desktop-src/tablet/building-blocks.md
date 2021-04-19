---
description: Tablet PC 平臺會產生數種保存格式，可作為先前所列格式的建立區塊。 以下是使用 Ink 物件的 Load 和 Save 方法產生和取用的格式。
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: 建置組塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32e6121ddfaabfc860239019ce62df65bdc36c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971979"
---
# <a name="building-blocks"></a>建置組塊

Tablet PC 平臺會產生數種保存格式，可作為先前所列格式的建立區塊。 以下是使用 [**Ink**](/previous-versions/ms583670(v=vs.100)) 物件的 [**Load**](/previous-versions/ms569609(v=vs.100)) 和 [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) 方法產生和取用的格式。

-   筆墨序列化格式 (ISF) ：筆跡序列化格式 (ISF) 是最精簡的筆墨持續性標記法。 您可以將 ISF 內嵌在二進位檔案格式中，或直接將它移到剪貼簿。 以 ISF 儲存的筆墨應該使用預設的座標系統，也就是 HIMETRIC，垂直軸反轉。
-   Base-64 編碼的 ISF：您可以使用 base-64 編碼的 ISF，直接將筆墨編碼成可延伸標記語言 (XML) 的 (XML) 或 HTML 檔案。
-   嚴加防禦圖形交換格式 (GIF) ：嚴加防禦 GIF 是一個 GIF 檔案，其中包含在檔案中內嵌的中繼資料。 以嚴加防禦 GIF 形式產生的筆墨可在無法辨識筆墨的應用程式中查看，如果筆墨傳回的應用程式可辨識筆墨，則會保留所有筆墨資料。 此格式適合用來在 HTML 檔案中傳輸筆墨內容。 無論應用程式是否辨識筆墨，任何應用程式都可以使用筆墨。
-   以64編碼的嚴加防禦 GIF：此格式適用于想要直接將筆跡編碼成 XML 或 HTML 檔案，然後稍後再將檔案轉換成影像的開發人員。 當您想要產生的 XML 檔案包含所有筆墨資訊，以及使用可延伸樣式單語言轉換 (XSLT) 來產生 HTML 時，可以使用此方法。
    > [!Note]  
    > 這項 LZW 壓縮和解壓縮技術藉由美國專利條款所涵蓋。 4558302與其相關和外國互相對應的專利 (統稱為 Unisys Corporation 所擁有的 LZW 專利) 。 Microsoft Corporation 已從 Unisys 的專利專利取得授權，以在特定 Microsoft 產品中使用 GIF 和 LZW 技術。 但是，這項授權並不會延伸到使用 Microsoft 開發產品（例如 Microsoft 工具組和語言開發產品）的協力廠商開發人員，以在自己的產品中提供 GIF 讀取/寫入或任何其他的 LZW 功能。 協力廠商開發人員必須自行決定是否需要來自 Unisys 的產品授權。

     

應用程式可以使用 [system.windows.media.visualtreehelper.hittest](/previous-versions/ms828460(v=msdn.10)) 或 [system.windows.media.visualtreehelper.hittest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) 方法來產生筆觸集合，以產生這些持續格式的其中一種，也可以：

-   使用 [AddStrokesAtRectangle](/previous-versions/ms569548(v=vs.100))方法，將這些筆觸新增至新的 [**筆墨**](/previous-versions/ms583670(v=vs.100))物件。
-   使用 [ExtractStrokes](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90))方法產生新的 [**筆墨**](/previous-versions/ms583670(v=vs.100))物件。

第一個會將選取矩形轉譯成原點，而第二個則不會。 然後，應用程式會使用 [**Ink**](/previous-versions/ms583670(v=vs.100))物件的 [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90))方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[sInk 和 tInk 物件](sink-and-tink-objects.md)
</dt> </dl>

 

 
