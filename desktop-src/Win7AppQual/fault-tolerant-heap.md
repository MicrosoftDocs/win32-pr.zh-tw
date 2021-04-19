---
description: .
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: 容錯堆積
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349c8c3d6d066de3d563880c169c8dde2e062370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983915"
---
# <a name="fault-tolerant-heap"></a>容錯堆積

## <a name="affected-platforms"></a>受影響的平臺

**用戶端-** Windows 7  

## <a name="feature-impact"></a>功能影響

 **嚴重性-** 中  
**頻率-** 低  


## <a name="description"></a>Description

容錯堆積 (FTH) 是 Windows 7 的子系統，負責監視應用程式損毀並自主套用緩和措施，以防止每個應用程式的未來損毀。 大部分的使用者都可以使用 FTH，而不需要介入或變更其部分。 不過，在某些情況下，應用程式開發人員和軟體測試人員可能需要覆寫此系統的預設行為。

## <a name="solution"></a>解決方法

**查看容錯堆積活動**

當服務啟動、停止或開始減輕新應用程式的問題時，容錯堆積會記錄資訊。 若要檢視此資訊，請遵循這些步驟：

1.  按一下 [開始] 功能表。
2.  在 [ **電腦** ] 上按一下滑鼠右鍵，然後按一下 [ **管理**]。
3.  按一下 [**事件檢視器**  >  **應用程式及服務記錄** 檔]，以將  >  **Microsoft**  >  **Windows > 容錯堆積**
4.  查看 FTH 事件。

服務停止和啟動事件不包含任何其他資料。 FTH Enabled 事件包含處理序識別碼 (PID) 、進程映射名稱和進程實例開始時間。

**停用容錯堆積**

**注意** 如果您使用登錄編輯程式或使用其他方法不正確地修改登錄，可能會發生嚴重的問題。 這些問題可能需要您重新安裝作業系統。 Microsoft 無法保證可以解決這些問題。 您必須自行承擔修改登錄的風險。  
 若要在系統上完全停用容錯堆積，請將 REG \_ DWORD 值 **HKLM \\ Software \\ Microsoft \\ FTH \\ Enabled** 設定為 **0**。

變更此值之後，請重新開機系統。 新的應用程式將不再啟用 FTH。

**重設 FTH 所追蹤的應用程式清單**

容錯堆積是自我管理的，而且如果在指定的應用程式中沒有有效防護措施，則會自動停止套用。 但是，如果您需要重設 FTH 可減輕問題的應用程式清單 (例如，如果您要測試應用程式，而且需要重現 FTH 正在) 緩和的損毀，您可以從提升許可權的命令提示字元執行下列命令：  **Rundll32.exe fthsvc.dll、FthSysprepSpecialize**  
**注意** 執行此命令將會清除所有 FTH 的應用程式，因此在執行此命令之後，目前正常運作的應用程式可能會開始損毀。  

 

 



