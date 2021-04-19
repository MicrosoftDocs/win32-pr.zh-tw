---
title: 監視設定函數
description: 監視設定函數
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- 監視，函數
- 監視，高階函數
- 監視，低層級函數
- 監視，列舉函數
- 高層級函數
- 低層級函數
- 列舉函數
- 監視設定，函數
- 監視設定、高階功能
- 監視設定、低層級功能
- 監視設定、列舉函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86925cd25912c17b8fb1bdd339888e5429de135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106980270"
---
# <a name="monitor-configuration-functions"></a>監視設定函數

下列函式是用來從監視取得資訊，以及變更監視的設定。 監視設定函數會分類為高階函式、低層級函式和列舉函數。 如需詳細資訊，請參閱 [使用監視器](using-monitor-configuration.md)設定。

## <a name="high-level-functions"></a>High-Level 函式



| 函式                                                                         | 描述                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**DegaussMonitor**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | Degausses 監視器。                                                                 |
| [**GetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | 抓取監視器的最小值、最大值和目前的亮度設定。             |
| [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | 抓取監視的設定功能。                               |
| [**GetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | 捕獲監視器目前的色溫。                                     |
| [**GetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | 抓取監視器的最小值、最大值和目前的對比設定。               |
| [**GetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | 抓取監視器的最小值、最大值和目前水準或垂直位置。 |
| [**GetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | 抓取監視器的最小值、最大值和目前的寬度或高度。                 |
| [**GetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | 抓取監視的紅色、綠色或藍色的磁片磁碟機值。                               |
| [**GetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | 捕獲監視器的紅色、綠色或藍色增益值。                                |
| [**GetMonitorTechnologyType**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | 抓取監視所使用的技術類型。                                  |
| [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | 將監視的色彩設定還原為其原廠預設值。                       |
| [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | 將監視的設定還原為其原廠預設值。                             |
| [**SaveCurrentMonitorSettings**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | 將目前的監視器設定儲存至顯示器的非動態儲存體。             |
| [**SetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | 設定監視的亮度值。                                                   |
| [**SetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | 設定監視器的色溫。                                                  |
| [**SetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | 設定監視的對比值。                                                     |
| [**SetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | 設定監視器顯示區域的水準或垂直位置。                |
| [**SetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | 設定監視器顯示區域的寬度或高度。                                |
| [**SetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | 設定監視的紅色、綠色或藍色的磁片磁碟機值。                                    |
| [**SetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | 設定監視的紅色、綠色或藍色增益值。                                     |



 

## <a name="low-level-functions"></a>Low-Level 函式



| 函式                                                                                   | 描述                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | 抓取描述監視器功能的字串。                                                        |
| [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | 捕獲監視器功能字串的長度。                                                       |
| [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | 捕獲監視器的水準和垂直同步處理頻率。                                     |
| [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | 抓取虛擬主控台的目前值、最大值和程式碼類型 (VCP) 程式碼的監視器。 |
| [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | 將目前的監視器設定儲存至顯示器的非動態儲存體。                                       |
| [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | 設定監視的虛擬主控台 (VCP) 程式碼的值。                                            |



 

## <a name="enumeration-functions"></a>列舉函數



| 函式                                                                                                   | 描述                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | 關閉實體監視器的控制碼。                                                    |
| [**DestroyPhysicalMonitors**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | 關閉實體監視器控制碼的陣列。                                              |
| [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | 捕獲與 **HMONITOR** 監視器控制碼相關聯的實體監視器數目。 |
| [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | 抓取與 Direct3D 裝置相關聯的實體監視器數目。              |
| [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | 抓取與 **HMONITOR** 監視器控制碼相關聯的實體監視器。           |
| [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | 抓取與 Direct3D 裝置相關聯的實體監視器。                        |



 

## <a name="internal-functions"></a>內部函數

監視器設定 API 會使用下列功能來存取顯示驅動程式中的功能。 應用程式不應呼叫這些函式。

-   [**DDCCIGetCapabilitiesString**](ddccigetcapabilitiesstring.md)
-   [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md)
-   [**DDCCIGetTimingReport**](ddccigettimingreport.md)
-   [**DDCCIGetVCPFeature**](ddccigetvcpfeature.md)
-   [**DDCCISaveCurrentSettings**](ddccisavecurrentsettings.md)
-   [**DDCCISetVCPFeature**](ddccisetvcpfeature.md)
-   [**DestroyPhysicalMonitorInternal**](destroyphysicalmonitorinternal.md)
-   [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md)
-   [**GetPhysicalMonitorDescription**](getphysicalmonitordescription.md)
-   [**GetPhysicalMonitors**](getphysicalmonitors.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[監視設定參考](monitor-configuration-reference.md)
</dt> </dl>

 

 




