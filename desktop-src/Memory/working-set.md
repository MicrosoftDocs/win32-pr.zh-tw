---
description: 進程的工作集是目前駐留在實體記憶體中之進程的虛擬位址空間中的一組頁面。
ms.assetid: ff05276a-1d40-4844-b649-10e32e3f1937
title: 工作集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54ed26e9809ebffd01edb30f48f36d398689e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975755"
---
# <a name="working-set"></a>工作集

進程的工作集是目前駐留在實體記憶體中之進程的虛擬位址空間中的一組頁面。 工作集只包含可分頁的記憶體配置;nonpageable 記憶體配置（例如 [位址視窗擴充](address-windowing-extensions.md) (AWE) 或 [大型分頁](large-page-support.md) 配置）不包含在工作集內。

當進程參考目前不在其工作集中的可分頁記憶體時，就會發生 *分頁錯誤* 。 系統分頁錯誤處理常式會嘗試解析分頁錯誤，如果成功，則會將頁面加入工作集。 存取 AWE 或大型頁面配置的 (永遠不會造成分頁錯誤，因為這些配置無法分頁。 ) 

若要解決 *硬分頁錯誤* ，必須從頁面的 *備份存放區* 讀取頁面內容，也就是系統分頁檔案或進程所建立的記憶體對應檔。 您可以在不存取備份存放區的情況下解析 *軟分頁錯誤* 。 當發生下列情況時，就會發生軟分頁錯誤：

-   此頁面位於一些其他進程的工作集內，因此它已經常駐在記憶體中。
-   頁面正在轉換中，因為已從所有使用頁面的處理常式的工作集移除該頁面，但尚未重設用途，或已經在執行記憶體管理員預先提取作業的結果中。
-   程式會在第一次參考配置的虛擬頁面 (有時也稱為「 *需要零的錯誤*) 。

您可以從處理常式工作集移除頁面，作為下列動作的結果：

-   此程式會藉由呼叫 [**SetProcessWorkingSetSize**](/windows/win32/api/winbase/nf-winbase-setprocessworkingsetsize)、 [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) 或 [**EmptyWorkingSet**](/windows/win32/api/psapi/nf-psapi-emptyworkingset) 函數來減少或清空工作集。
-   此處理程式會在未鎖定的記憶體範圍上呼叫 [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) 函數。
-   此程式會使用 [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) 函數 unmaps 檔案的對應視圖。
-   記憶體管理員會從工作集修剪頁面，以建立更多可用的記憶體。
-   記憶體管理員必須從工作集移除頁面，以騰出空間給新的頁面 (例如，因為工作集的大小上限為) 。

如果有數個進程共用某個頁面，從一個進程的工作集移除頁面，並不會影響其他進程。 從所有使用它的進程的工作集移除頁面之後，該頁面就會變成 *轉換頁面*。 轉換頁面會在 RAM 中保持快取狀態，直到某個進程或重新用途的 (重新參考頁面為止例如，填滿零，並將其提供給另一個進程) 。 如果轉換頁面自從上次寫入磁片後已經過修改 (也就是，如果頁面是「已變更」 ) ，則必須先將該頁面寫入至其備份存放區，才能重新建立用途。 當這類頁面可供使用時，系統就會開始將中途轉換頁面寫入其備份存放區。

每個進程都有最小和最大的工作集大小，它會影響進程的虛擬記憶體分頁行為。 若要取得指定進程之工作集的目前大小，請使用 [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) 函數。 若要取得或變更工作集大小的下限和上限，請使用 [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex) 和 [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex) 函數。

進程狀態應用程式開發介面 (PSAPI.DLL) 提供許多函數，以傳回有關處理常式工作集的詳細資訊。 如需詳細資訊，請參閱 [工作集資訊](../psapi/working-set-information.md)。

 

 
