---
title: 使用 Low-Level 監視設定函數
description: 使用 Low-Level 監視設定函數
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- 監視，函數
- 監視，低層級設定功能
- 監視器、DDC/CI
- 監視，顯示資料通道命令介面
- 監視設定、低層級設定功能
- 監視設定，函數
- 監視設定、DDC/CI
- 監視設定，顯示資料通道命令介面
- 低層級設定函數
- 顯示資料通道命令介面
- DDC/CI
- " (MCCS) 的 VESA 監視器控制命令集"
- '監視控制命令集 (MCCS) '
- 'MCCS (監視器控制命令集) '
- '虛擬主控台 (VCP) '
- 'VCP (虛擬主控台) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933183"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a>使用 Low-Level 監視設定函數

使用低層級的監視設定功能之前，您應該先熟悉這些標準：

-   顯示資料通道命令介面 (DDC/CI) 
-    (MCCS) 的 VESA 監視器控制命令集

低層級函式的運作方式是取得並設定虛擬主控台 (VCP) 代碼的值。 VCP 程式碼可以是 *連續* 或 *noncontinuous*。 連續的代碼可以假設零和廠商專屬的最大值之間的任何值。 Noncontinuous 代碼支援一組已定義的值，也就是廠商專屬的值。

若要使用低層級的監視設定函數，請執行下列步驟：

1.  藉由呼叫 [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors)或 [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)來取得 **HMONITOR** 控制碼。
2.  呼叫 [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) 以取得與 **HMONITOR** 控制碼相關聯的實體監視器數目。
3.  呼叫 [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) 以取得實體監視器的控制碼清單。
4.  呼叫 [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) 以取得監視器之 DDC/CI 功能字串的長度。 功能字串是包含監視靜態資訊的 ASCII 字串。 字串的其中一個部分會列出監視器支援的 VCP 碼。 此字串也會列出支援的 noncontinuous VCP 代碼值。
5.  配置緩衝區來保存功能字串，並呼叫 [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) 來取得字串。
6.  剖析功能字串，以判斷監視器支援哪些 VCP 碼。
7.  針對連續的 VCP 程式碼，呼叫 [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) 以取得程式碼的目前和最大值。 針對 noncontinuous VCP 程式碼，剖析功能字串以取得支援的值。
8.  呼叫 [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) 以設定 VCP 碼的新值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用監視設定**](using-monitor-configuration.md)
</dt> </dl>

 

 