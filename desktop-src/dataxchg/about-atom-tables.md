---
title: 關於 Atom 資料表
description: 本節討論 atom 資料表。
ms.assetid: 12114a3e-99a4-480f-9d1a-57c1942b7382
keywords:
- 原子
- atom 資料表
- atom 名稱
- 動態資料交換 (DDE) 、原子
- DDE (動態資料交換) 、原子
- 全域 atom 資料表
- 本機 atom 資料表
- 整數原子
- 字串原子
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 92a8304e1e96c7385ddb11ba6391258acbe62a26
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549603"
---
# <a name="about-atom-tables"></a>關於 Atom 資料表

*Atom 資料表* 是系統定義的資料表，可儲存字串和對應的識別碼。 應用程式會將字串放在 atom 資料表中，並接收可用於存取字串的16位整數，稱為 *atom*。 放在 atom 資料表中的字串稱為 *atom 名稱*。

系統會提供一些 atom 資料表。 每個 atom 資料表都有不同的用途。 例如，動態資料交換 (DDE) 應用程式會使用 [全域 atom 資料表](#global-atom-table) ，與其他應用程式共用專案名稱和主題名稱字串。 DDE 應用程式不會傳遞實際的字串，而是會將全域原子傳遞給其夥伴應用程式。 夥伴會使用原子來取得 atom 資料表中的字串。

應用程式可以使用本機 atom 資料表來儲存自己的專案名稱關聯。

系統使用的 atom 資料表無法直接存取應用程式。 不過，應用程式在呼叫各種函式時，會使用這些原子。 例如，已註冊的剪貼簿格式會儲存在系統所使用的內部 atom 資料表中。 應用程式會使用 [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) 函式，將原子新增至這個 atom 資料表。 此外，已註冊的類別會儲存在系統所使用的內部 atom 資料表中。 應用程式會使用 [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) 或 [**RegisterClassEx**](/windows/desktop/api/winuser/nf-winuser-registerclassexa) 函數，將原子加入這個 atom 資料表中。

本節將討論下列主題。

-   [全域 Atom 資料表](#global-atom-table)
-   [使用者 Atom 資料表](#user-atom-table)
-   [本機 Atom 資料表](#local-atom-tables)
-   [Atom 類型](#atom-types)
    -   [字串原子](#string-atoms)
    -   [整數原子](#integer-atoms)
-   [Atom 建立和使用計數](#atom-creation-and-usage-count)
-   [Atom 資料表查詢](#atom-table-queries)
-   [Atom 字串格式](#atom-string-formats)

## <a name="global-atom-table"></a>全域 Atom 資料表

全域 atom 資料表可供所有應用程式使用。 當應用程式將字串放入全域 atom 資料表時，系統會產生在整個系統中都是唯一的 atom。 任何具有 atom 的應用程式都可以藉由查詢全域 atom 資料表來取得它所識別的字串。

定義私人 DDE 資料格式以與其他應用程式共用資料的應用程式，應該將格式名稱放置在全域 atom 資料表中。 這項技術可避免與系統或其他應用程式所定義的格式名稱相衝突，並讓識別碼 (原子) ，以供其他應用程式使用的訊息或格式使用。

## <a name="user-atom-table"></a>使用者 Atom 資料表

除了全域 atom 資料表之外，使用者 atom 資料表也是另一個系統 atom 資料表，也會在所有進程間共用。 使用者 atom 資料表用於 win32k 內部的少數案例;例如，windows 模組名稱、win32k 中已知的字串、OLE 格式等等。雖然應用程式不會直接與使用者 atom 資料表互動，但是它們會呼叫數個 Api （例如 [RegisterClass](/windows/win32/api/winuser/nf-winuser-registerclassexa)、 [RegisterWindowMessage](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)和 [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata)），以將專案加入至使用者 atom 資料表。 新增的專案 `RegisterClass` 可以由刪除 `UnregisterClass` 。 不過，在 `RegisterWindowMessage` `RegisterClipboardFormat` 會話結束之前，不會刪除和所新增的專案。 如果使用者 atom 資料表已沒有空間，而且傳入的字串尚未存在於資料表中，則呼叫會失敗。 

### <a name="atom-table-size"></a>Atom 資料表大小
 
許多重要的 Api （包括 [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa)）都依賴使用者原子。 因此，使用者 atom 資料表中的空間耗盡會導致嚴重的問題;例如，所有的應用程式可能無法啟動。 以下是一些建議，以確保您的應用程式有效率地利用 atom 資料表，並保留應用程式和系統的可靠性和效能：  

1. 您應該限制應用程式使用者 atom 資料表的使用方式。 使用、或之類的 Api 來儲存唯一字串 `RegisterClass` `RegisterWindowMessage` ，會 `RegisterClipboardFormat` 佔用使用者 atom 資料表中的空間，供其他應用程式用來使用字串來註冊視窗類別。 如果有可能的話，您應該使用[AddAtom](/windows/desktop/api/Winbase/nf-winbase-addatomw) / [DeleteAtom](/windows/desktop/api/Winbase/nf-winbase-deleteatom)將字串儲存在本機 atom 資料表中， [](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) / 如果需要跨進程的原子，則使用 GlobalAddAtom[GlobalDeleteAtom](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) 。

1. 如果有關于應用程式造成使用者 atom 資料表問題的考慮，您可以連接核心偵錯工具並中斷 () 呼叫的程式，以調查根本原因 `UserAddAtomEx` `bae1 win32kbase!UserAddAtomEx /p <eprocess> "kc10;g"` 。 查看 `user32!` 呼叫堆疊以查看正在呼叫的 API。 方法類似于全域 atom 資料表問題偵測，其中說明了 [識別全域 Atom 資料表](/archive/blogs/ntdebugging/identifying-global-atom-table-leaks)流失的問題。 傾印使用者 atom 資料表內容的另一種方式，是在可能的原子範圍（從0xC000 到0xFFFF）呼叫 [GetClipboardFormatName](/windows/win32/api/winuser/nf-winuser-getclipboardformatnamea) 。 如果應用程式正在執行時，總 atom 計數會穩定出現，或在應用程式關閉時不會回到基準，就會發生問題。

## <a name="local-atom-tables"></a>本機 Atom 資料表

應用程式可以使用本機 atom 資料表，有效率地管理只在應用程式中使用的大量字串。 這些字串和相關聯的原子只適用于建立資料表的應用程式。

在許多結構中需要相同字串的應用程式，可以使用本機 atom 資料表來減少記憶體使用量。 應用程式可以將字串放在 atom 資料表中，並將產生的 atom 包含在結構中，而不是將字串複製到每一個結構中。 如此一來，字串只會在記憶體中出現一次，但可以在應用程式中使用多次。

應用程式也可以使用本機 atom 資料表來節省搜尋特定字串的時間。 若要執行搜尋，應用程式只需要將搜尋字串放在 atom 資料表中，並將產生的 atom 與相關結構中的原子進行比較。 比較原子通常比比較字串更快。

Atom 資料表會實作為雜湊表。 根據預設，本機 atom 資料表會使用37值區作為雜湊表。 不過，您可以變更呼叫 [**InitAtomTable**](/windows/desktop/api/Winbase/nf-winbase-initatomtable) 函式所使用的 bucket 數目。 但是，如果應用程式呼叫 **InitAtomTable**，則在呼叫任何其他 atom 管理函式之前，它必須先這麼做。

## <a name="atom-types"></a>Atom 類型

應用程式可以建立兩種類型的原子：字串原子和整數原子。 整數原子和字串原子的值不會重迭，因此這兩種類型的原子都可在相同的程式碼區塊中使用。

有幾個函式接受字串或原子作為參數。 將 atom 傳遞給這些函式時，應用程式可以使用 [**MAKEINTATOM**](/windows/desktop/api/Winbase/nf-winbase-makeintatom) 宏將 atom 轉換成可供函式使用的表單。

下列各節說明 atom 類型。

-   [字串原子](#string-atoms)
-   [整數原子](#integer-atoms)

### <a name="string-atoms"></a>字串原子

當應用程式將以 null 結束的字串傳遞至 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)、 [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw)、 [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)和 [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) 函式時，它們會接收 *字串原子* (16 位整數) 傳回。 字串原子具有下列屬性：

-   字串原子的值位於範圍 0xC000 (MAXINTATOM) 到0xFFFF 之間。
-   在 atom 資料表中搜尋 atom 名稱時，大小寫並不重要。 此外，搜尋作業中的整個字串必須相符;不會執行任何符合的子字串。
-   與字串 atom 相關聯的字串不能超過255個位元組大小。 這項限制適用于所有 atom 函數。
-   *參考計數* 會與每個 atom 名稱相關聯。 每次將 atom 名稱加入資料表時，計數就會遞增，並在每次從 atom 名稱中刪除 atom 名稱時減少。 這可防止相同字串 atom 的不同使用者終結彼此的 atom 名稱。 當 atom 名稱的參考計數等於零時，系統會從資料表中移除 atom 和 atom 名稱。

### <a name="integer-atoms"></a>整數原子

整數原子與字串原子的差異有下列幾種：

-   整數原子的值位於範圍0x0001 到 0xBFFF (**MAXINTATOM**– 1) 。
-   整數 atom 的字串表示是 \# *dddd*，其中以 *dddd* 表示的值是十進位數。 系統會忽略前置零。
-   沒有與整數 atom 相關聯的參考計數或儲存體額外負荷。

## <a name="atom-creation-and-usage-count"></a>Atom 建立和使用計數

應用程式會藉由呼叫 [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) 函數來建立本機 atom;它會藉由呼叫 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來建立全域 atom。 這兩個函式都需要一個指向字串的指標。 系統會在適當的 atom 資料表中搜尋字串，並將對應的 atom 傳回給應用程式。 在字串 atom 的案例中，如果字串已經存在於 atom 資料表中，系統會在此程式期間遞增字串的參考計數。

新增相同 atom 名稱的重複呼叫會傳回相同的 atom。 如果在呼叫 [**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw) 時，資料表中沒有 atom 名稱，atom 名稱就會加入至資料表，並傳回新的 atom。 如果它是字串 atom，其參考計數也會設定為1。

當應用程式不再需要使用本機 atom 時，應呼叫 [**DeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-deleteatom) 函式;它應該會在不再需要全域 atom 時呼叫 [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) 函數。 在字串 atom 的案例中，這兩個函式會將對應 atom 的參考計數減少一。 當參考計數到達零時，系統會從資料表中刪除 atom 名稱。

字串 atom 的 atom 名稱會保留在全域 atom 資料表中，前提是它的參考計數大於零，即使在將它放置在資料表中的應用程式終止之後也是如此。 當相關聯的應用程式終止時，無論資料表中原子的參考計數為何，都會終結本機 atom 資料表。

## <a name="atom-table-queries"></a>Atom-Table 查詢

應用程式可以使用 [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma) 或 [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma) 函數，判斷特定字串是否已存在於 atom 資料表中。 這些函式會在 atom 資料表中搜尋指定的字串，如果有字串，則會傳回對應的 atom。

應用程式可以使用 [**GetAtomName**](/windows/desktop/api/Winbase/nf-winbase-getatomnamea) 或 [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) 函數，從 atom 資料表中取出 atom 名稱字串，前提是應用程式具有對應至所要搜尋之字串的 atom。 這兩個函式會將指定之 atom 的 atom 名稱字串複製到緩衝區，並傳回所複製字串的長度。 **GetAtomName** 會從本機 atom 資料表抓取 atom 名稱字串，而 **GlobalGetAtomName** 會從全域 atom 資料表抓取 atom 名稱字串。

## <a name="atom-string-formats"></a>Atom 字串格式

[**AddAtom**](/windows/desktop/api/Winbase/nf-winbase-addatomw)、 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)、 [**FindAtom**](/windows/desktop/api/Winbase/nf-winbase-findatoma)和 [**GlobalFindAtom**](/windows/desktop/api/Winbase/nf-winbase-globalfindatoma)函式會採用以 null 終止之字串的指標。 應用程式可以使用下列其中一種方式來指定此指標。



|     字串格式               |    Description                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------|
| \#*dddd*           | 指定為十進位字串的整數。 用來建立或尋找整數 atom。                  |
| *字串 atom 名稱* | 字串 atom 名稱。 用來將字串 atom 名稱加入 atom 資料表中，並接收傳回的 atom。 |



 

 

 
