---
description: 雖然應用程式可以儲存在登錄中的資料類型和大小有幾種技術限制，但是有一些實用的方針可以提升系統效率。
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: 登錄儲存體空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00414edbd34452fd6943a4d73a2ebe85af5d38884ddd0ca77f1d8fb41ae6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885076"
---
# <a name="registry-storage-space"></a>登錄儲存體空間

雖然應用程式可以儲存在登錄中的資料類型和大小有幾種技術限制，但是有一些實用的方針可以提升系統效率。 應用程式應該將設定和初始化資料儲存在登錄中，並將其他類型的資料儲存在其他位置。

一般來說，包含一或兩個 kb (K) 的資料應儲存為檔案，並使用登錄中的機碼來參考，而不是儲存為值。 應用程式應該將資料儲存為檔案，並參考該檔案，而不是複製登錄中的大型資料片段。 可執行檔二進位程式碼絕不能儲存在登錄中。

值專案所使用的登錄空間遠少於索引鍵。 為了節省空間，應用程式應該將類似的資料以結構的形式群組在一起，並將結構儲存為值，而不是將每個結構成員儲存為個別的索引鍵。  (將資料儲存為二進位格式，可讓應用程式將資料儲存成一個值，而這些值會由數個不相容的類型組成。 ) 

登錄檔的視圖會在分頁集區記憶體中對應。

**Windows server 2008 （適用于32位）、Windows vista （含 SP1），適用于32位、Windows vista、Windows Server 2003、Windows XP：** 登錄檔的視圖會對應到電腦快取位址空間中。 因此，無論登錄資料的大小為何，都不會向 (MB) 收取超過 4 mb 的費用。

登錄 hive 的大小上限為 2 GB，但系統 hive 除外。

**Windows server 2003 SP1、Windows Server 2003 和 Windows XP：** 分頁集區記憶體和磁碟空間中的 hive 可能會耗用的總空間量沒有明確的限制，不過系統配額可能會影響實際的大小上限。 從 Windows Server 2003 Service Pack 2 (SP2) 開始，登錄區的大小上限限制為 2 GB。

系統 hive 的大小上限會受到實體記憶體的限制，如下表所示。 

| 系統                      | 系統 hive 的大小上限                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| x86 系統           | 50% 的實體記憶體，最高 400 MB。**Windows server 2003 SP2、Windows Server 2003 SP1、Windows server 2003 和 Windows XP：** 25% 的實體記憶體，最高達 200 MB。<br/>                                    |
| x64 型系統           | 50% 的實體記憶體，最高 1.5 GB。**Windows Server 2003 SP2：** 系統記憶體的25%，最多 200 MB。<br/> **Windows server 2003 （含 SP1）、Windows Server 2003 和 Windows XP 64-Bit Edition：** 32 MB。<br/> |
| Intel Itanium 型系統 | 50% 的實體記憶體，最多 1 GB。**Windows server 2008、Windows Vista、Windows server 2003 SP2、Windows server 2003 SP1、Windows server 2003 和 Windows XP 64-Bit Edition：** 32 MB。<br/>                         |



 

## <a name="windows-2000"></a>Windows 2000

登錄資料儲存在分頁集區中，這是用於系統資料的區域，可在不使用時寫入磁片。 **RegistrySizeLimit** 值會建立所有應用程式的登錄資料可取用的分頁集區數量上限。 此值位於下列登錄機碼中：

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

根據預設，登錄大小限制為分頁集區的25%。  (分頁集區的預設大小為 32 MB，因此這是 8 MB。 ) 系統可確保 **RegistrySizeLimit** 的最小值是 4 MB，而最大值大約是 **PagedPoolSize** 值的80%。 如果這個專案的值大於分頁集區大小的80%，系統會將登錄的大小上限設定為分頁集區大小的80%。 這可防止登錄使用進程所需的空間。 請注意，設定這個值並不會在分頁集區中配置空間，也無法確保在需要時可以使用該空間。

分頁集區大小是由下列登錄機碼中的 **PagedPoolSize** 值所決定：

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

如需如何判斷登錄的目前和最大大小的範例，請參閱 [判斷登錄大小](determining-the-registry-size.md)。

分頁集區的最大值約為 300470 MB，因此登錄大小限制為 240-376 MB。 但是，如果使用了/3GB 參數，則分頁集區大小上限為 192 MB，因此登錄最多可達 153.6 MB。

 

 




