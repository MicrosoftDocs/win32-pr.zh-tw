---
description: 深入瞭解：建立資料庫
title: 建立資料庫
TOCTitle: Creating Databases
ms:assetid: d221144d-f777-4f8a-80ca-2ebdb77108dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294100(v=EXCHG.10)
ms:contentKeyID: 32765715
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eac708b64837fc79fa8a5060df7deb93ec552e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973894"
---
# <a name="creating-databases"></a>建立資料庫


_**適用于：** Windows |Windows Server_

## <a name="creating-databases"></a>建立資料庫

ESE 資料庫包含一個或多個資料表，這些資料表會依資料行和資料列來組織資料。 ESE 資料庫是以名稱和資料庫識別碼來識別。 ESE 資料庫看起來像是 Microsoft Windows 作業系統的單一檔案;不過，在內部，資料庫會儲存為頁面的集合。 這些頁面包含的中繼資料會描述資料庫中的資料、資料本身，以及儲存不同資料順序的一或多個索引。 資料庫最多可以包含 2 ^ 31 個頁面，或包含 8 KB 頁面之資料庫的 16 Tb 資料。

應用程式會建立資料庫引擎的實例，然後建立資料庫並將它附加至實例。 最多可同時將6個資料庫附加至具有 [JetCreateDatabase](./jetcreatedatabase-function.md) 或 [JetAttachDatabase](./jetattachdatabase-function.md)的實例。 一個或多個會話應該在資料庫中啟動，因為所有後續的 ESE 作業都是在會話的內容中執行。 您應該針對每個使用 ESE 的執行緒開啟個別的會話。

此程式會初始化 ESE 並建立資料庫。

### <a name="to-initialize-ese-and-create-a-database"></a>初始化 ESE 並建立資料庫

1.  [JetCreateInstance](./jetcreateinstance-function.md)：建立 database engine 的實例。
    
    **WINDOWS XP 和更新版本：** 這項功能可在 Windows XP 及更新版本中使用。 在 Windows 2000 上，只支援一個實例，而該實例會以隱含方式建立

2.  [JetSetSystemParameter](./jetsetsystemparameter-function.md)：在使用 [JetInit](./jetinit-function.md)初始化實例之前，必須先設定影響實體配置的系統參數，例如 JET_paramLogFilePath 和 JET_paramSystemPath。 在這個階段設定的參數會針對實例中建立的所有資料庫進行設定。 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 是唯一可以使用實例的函式，它會使用 [JetInit](./jetinit-function.md)來初始化。

3.  [JetInit](./jetinit-function.md)：初始化實例。 實例必須使用 [JetInit](./jetinit-function.md) 初始化，才能搭配任何其他函式使用。

4.  [JetBeginSession](./jetbeginsession-function.md)：建立所有後續交易的會話。 所有資料庫交易都會發生在會話的內容中 ([JET_SESID](./jet-sesid.md)) 。

5.  [JetCreateDatabase](./jetcreatedatabase-function.md)：建立資料庫，並將控制碼傳回 ([JET_DBID](./jet-dbid.md)) 的資料庫識別碼。
    
    如果資料庫已經存在，則會以下列兩個步驟取代上述的步驟5：
    
    1.  [JetAttachDatabase](./jetattachdatabase-function.md)：依名稱將資料庫附加至會話
    
    2.  [JetOpenDatabase](./jetopendatabase-function.md)：傳回後續資料庫作業中所使用的資料庫識別碼。

您可以使用 [JetDetachDatabase](./jetdetachdatabase-function.md) ，並在稍後附加至具有 [JetAttachDatabase](./jetattachdatabase-function.md)的另一個實例，將資料庫從一個 ESE 實例卸離。 卸離資料庫後，就可以使用標準的 Windows 公用程式，將它複製成單一檔案。 不過，當資料庫附加至 ESE 實例時，無法複製它，因為 ESE 會以獨佔方式開啟資料庫檔案。 此外，如果實例損毀，則無法單獨複製資料庫檔案，因為它需要與其相關聯的交易記錄檔，才能從該損毀中復原。
