---
description: '\_ForceCodepage 資料表是用來變更安裝套件字碼頁的特殊資料表。 您可以藉由匯出或匯入名為 ForceCodepage. idt 的文字保存檔案，來判斷或設定字碼頁 \_ 。'
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee252260b0aaee9713c28af5a6d810a3f6a8ed1c1b376b52bd82472cebfd0853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979598"
---
# <a name="_forcecodepage"></a>\_ForceCodepage

\_ForceCodepage 資料表是用來變更安裝套件字碼頁的特殊資料表。 您可以藉由匯出或匯入名為 ForceCodepage. idt 的 [文字保存](text-archive-files.md) 盤案，來判斷或設定字碼頁 \_ 。

ForceCodepage 資料表的格式 \_ 為2個空白行，後面接著第三行表示數值字碼頁。 例如， \_ 日文資料庫的 ForceCodepage idt 檔案看起來會如下所示。 此案例中的數值字碼頁為932。

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

如需有關如何使用 \_ ForceCodepage 來取得或設定資料庫字碼頁的詳細資訊，請參閱下列主題。

-   [程式字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)
-   [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md)
-   [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)

\_ForceCodepage 資料表是用來變更安裝套件字碼頁的特殊虛擬資料表。 使用 \_ ForceCodepage 資料表無條件地將資料庫設定為字碼頁，而不會執行任何驗證，因為目前在資料庫中的資料是否可以轉譯成新的字碼頁。 一律建議您以非語言相關資料庫開頭變更資料庫的字碼頁。

 

 



