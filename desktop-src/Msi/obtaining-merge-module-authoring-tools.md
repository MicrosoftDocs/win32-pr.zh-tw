---
description: 若要產生合併模組，您需要取得用來編輯 .msm 檔案的軟體工具。
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: 取得合併模組撰寫工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a85fb75c0317a6737393e67f12a7a03cd8b76c68a8261c9d26d10d06cbe484c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327878"
---
# <a name="obtaining-merge-module-authoring-tools"></a>取得合併模組撰寫工具

若要產生合併模組，您需要取得用來編輯 .msm 檔案的軟體工具。 因為 .msm 檔案基本上是簡化的 .msi 檔案，所以您可以使用用來建立安裝資料庫的相同工具。 例如，Orca.exe Windows Installer SDK 提供的應用程式。

另一種方式是購買可從獨立軟體廠商取得的其中一個安裝程式封裝工具。 開發中有數個協力廠商工具，可用來產生合併模組。 如果您選擇使用協力廠商工具，您應該確認它會產生與本檔中所述標準一致的合併模組。 尤其是，您應該判斷編輯工具尚未對合併模組執行下列任何一項動作。

-   已將多餘的資料表新增至 [ModuleIgnoreTable 資料表](moduleignoretable-table.md)中未參考的合併模組。

    刪除這些資料表，或將它們加入至 ModuleIgnoreTable 資料表。

-   將不必要的 [樣式表單](textstyle-table.md) 加入至合併模組。

    如果您的合併模組沒有 UI (而且通常不應該) 您可以安全地刪除此資料表。

-   已將不必要的專案新增至 [目錄資料表](directory-table.md)。

    從目錄資料表中移除不必要的專案。

-   從合併模組的驗證資料表中取出資訊 \_ 。

    這可防止合併模組驗證。 加入完整的 \_ 驗證資料表。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在合併模組中撰寫使用者介面](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[撰寫合併模組目錄資料表](authoring-merge-module-directory-tables.md)
</dt> <dt>

[驗證合併模組](validating-merge-modules.md)
</dt> </dl>

 

 



