---
description: 移除 Windows 登錄反映
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: 移除 Windows 登錄反映
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9fcd31686754f9bf2d92994bec4a53b39edaf5d94b34f464e1dfdbf1179c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328977"
---
# <a name="removal-of-windows-registry-reflection"></a>移除 Windows 登錄反映

## <a name="platform"></a>平台

**客戶** 端-Windows 7  
**伺服器**-Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>描述

登錄反映程式會在兩個登錄視圖之間複製登錄機碼和值，讓它們保持同步。在舊版 Windows 的64位安裝中，此程式會反映32位和64位之間的重新導向登錄機碼子集。 但是，這種方式的執行會導致登錄的狀態不一致。  (如需登錄反映的詳細資訊，請參閱下面的 *其他資源連結* 中的對應 MSDN 文章。 ) 

從 Windows 7 開始，我們已完全移除登錄反映，併合並用來反映的金鑰：

-   HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別
-   HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ COM3
-   HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ EventSystem
-   HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Ole
-   HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Rpc
-   HKEY \_ 使用者 \\ \* \\ 軟體 \\ 類別
-   HKEY \_ USERS \\ \* \_ 類別

實際上，這會提供相同的反映行為，因為這些金鑰的變更會立即適用于32位和64位應用程式。

有條件地反映的索引鍵會保持分割：

-   HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID
-   HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ 介面
-   HKEY \_ 使用者 \\ \* \\ 軟體 \\ 類別 \\ CLSID
-   HKEY \_ 使用者 \\ \* \\ 軟體 \\ 類別 \\ 介面
-   HKEY \_ 使用者 \\ \* \_ 類別 \\ CLSID
-   HKEY \_ 使用者 \\ \* \_ 類別 \\ 介面

它們是用來保留不應在32位和64位應用程式之間共用的資料。

## <a name="manifestation"></a>表現

上述清單中的 CLSID 和介面金鑰在仍重新導向時，不會再反映出來。 雖然在大部分情況下，這是所需的行為，但應用程式可能會相依于 Vista 中反映的行為。

允許應用程式控制反映 (RegDisableReflectionKey 和 RegEnableReflectionKey) 的函式在 Windows 7 中不是 ops。

## <a name="mitigation-of-impact"></a>影響緩和措施

COM 是登錄反映的主要取用者。 已更新 COM 和其他取用者以配合此變更。 此變更不會影響使用標準 COM Api 的應用程式。

## <a name="solution"></a>解決方案

如果您要依賴登錄反映來同步處理32位和64位的視圖，請套用下列其中一個選項：

-   在安裝期間明確地在這兩個視圖中建立金鑰
-   將金鑰移出反映的索引鍵範圍
-   查詢反映的金鑰時，檢查登錄的兩個視圖

    **注意：**\_ \_ 無法合併 key wow64 32KEY 和 key \_ wow64 \_ 64KEY 旗標

如果您要依賴 RegDisableReflectionKey 函式來停用登錄反映，請套用下列其中一個選項：

-   在安裝期間明確地在這兩個視圖中建立金鑰
-   將金鑰移出反映的索引鍵範圍
-   使用平臺特定的子機碼 (例如 x86、amd64 和 ia64) 來分隔位特定的資料

## <a name="links-to-other-resources"></a>其他資源的連結

-   [登錄反映文章](../winprog64/registry-reflection.md)
-   [登錄重新導向程式文章中的重新導向金鑰清單](../winprog64/registry-redirector.md)
-   [Wow64 的最佳作法](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> 這些資源可能無法在某些語言及國家/地區中使用。

 

 

 
