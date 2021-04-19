---
description: CPU 集會提供 Api，以「軟」方式宣告與作業系統電源管理相容的應用程式親和性。
ms.assetid: FF8BE790-19D9-473F-B184-C54FB392D61A
title: CPU 集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801474591751f04a5bffe570d6b8caff4974203f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974275"
---
# <a name="cpu-sets"></a>CPU 集

CPU 集會提供 Api，以「軟」方式宣告與作業系統電源管理相容的應用程式親和性。 此外，API 還可讓應用程式使用 **進程預設** 機制，將進程中的所有背景執行緒 reaffinitize 到處理器的子集，以避免進程內的作業系統執行緒干擾。 某些版本的 Windows 支援核心保留原則，其中系統的 CPU 組子集可專門用於個別應用程式和工作負載的專屬用途。

CPU 集 API 適用于與虛擬處理器親和性相關聯的 CPU 集識別碼。 在大部分的系統上，以及大部分的情況下，每個 CPU 集合識別碼都會直接對應到單一的 **主** 邏輯處理器。 相似化為至指定 CPU 集的執行緒通常會在其選取的 CPU 組識別碼清單中的其中一個處理器上執行。

您可以檢查系統 CPU 集資訊中配置 **的旗標，以** 判斷保留的 CPU 集 \_ \_ \_ 。 系統會控制對保留的 CPU 集的存取權，而且可以使用系統 \_ CPU \_ 集資訊結構的 AllocatedToTargetProcess 旗標來查詢指派 \_ 。 如果處理常式嘗試使用專門配置給其他進程的 CPU 集合指派，則會忽略其要求，並在其他地方排定指派給不允許的 CPU 集的執行緒。 可以在兩個層級指派 CPU 集。 進程預設 CPU 集會指派給進程中的所有線程，且該進程中的執行緒沒有在選取的層級上指派。 如果執行緒或進程已設定嚴格的相似性遮罩，則會在任何衝突的 CPU 集合指派上方遵守相似性遮罩。 在多群組系統上，如果 CPU 指派所在的群組與執行緒的親和性遮罩中的群組不相符，則會予以忽略。 如果執行緒指派給多個有效的 CPU 集合，它會根據其優先順序以及這些處理器上爭用執行緒的優先順序，在其中一個對應的處理器上執行。

**CPU 集函數/列舉/結構**

-   [**GetProcessDefaultCpuSets**](getprocessdefaultcpusets.md) 函式
-   [**GetSystemCpuSetInformation**](getsystemcpusetinformation.md) 函式
-   [**GetThreadSelectedCpuSets**](getthreadselectedcpusets.md) 函式
-   [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md) 函式
-   [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) 函式
-   [**CPU \_設定 \_ 資訊 \_ 類型**](cpu-set-information-type.md) 列舉
-   [**系統 \_CPU \_ 集 \_ 資訊**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) 結構

 

 



