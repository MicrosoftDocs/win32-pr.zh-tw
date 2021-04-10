---
description: WMI 核心提供者會定義組成 WMI 核心功能的類別。
ms.assetid: 6EEA4284-CCFE-4206-9EAA-B4BCF988DE03
title: WMI 核心提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9927be7208d9133d65257292950913972e96483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194354"
---
# <a name="wmi-core-provider"></a>WMI 核心提供者

WMI 核心提供者會定義組成 WMI 核心功能的類別。

大部分的 WMI 核心提供者類別都包含 [WDM 提供者](wdm-provider.md)所提供的資料，並說明顯示監視器。 這些類別定義于 Wmi 中，並位於「根 \\ Wmi」命名空間中。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                           | 描述                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSMonitorClass**](msmonitorclass.md)<br/>                                             | 是抽象的 WMI 基類。 描述影片顯示監視器的類別會繼承自這個 [**MSMonitorClass**](msmonitorclass.md)。<br/>                                                                         |
| [MSMCA 類別](msmca-classes.md)<br/>                                                   | 公開機器檢查架構 (MCA) 的一組 WMI 類別。 系統抽象層 (SAL) 提供 MSMCA 類別中報告的所有事件。 Intel Corporation 開發和擁有 MCA。<br/>         |
| [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md)<br/>                         | 表示支援之頻率範圍特性的容器。<br/>                                                                                                                                          |
| [**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)<br/>     | 代表受支援的監視器顯示功能。<br/>                                                                                                                                                           |
| [**VideoModeDescriptor**](videomodedescriptor.md)<br/>                                   | 包含 [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md)類別中 **MonitorSourceModes** 陣列的模式描述項元素。<br/>                                           |
| [**>register-wmievent**](wmievent.md)<br/>                                                         | [**>register-wmievent**](wmievent.md)類別是衍生所有 WMI 事件類別的基類。<br/>                                                                                                                |
| [**WmiMonitorAnalogVideoInputParams**](wmimonitoranalogvideoinputparams.md)<br/>         | 代表電腦監視器的類比影片輸入參數。<br/>                                                                                                                                                 |
| [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)<br/>                 | 代表電腦監視器的基本顯示功能。<br/>                                                                                                                                                        |
| [**WmiMonitorBrightness**](wmimonitorbrightness.md)<br/>                                 | 代表電腦監視器的亮度參數。<br/>                                                                                                                                                         |
| [**WmiMonitorBrightnessEvent**](wmimonitorbrightnessevent.md)<br/>                       | 代表監視的亮度變更。<br/>                                                                                                                                                                 |
| [**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)<br/>                   | 包含管理監視亮度的方法。<br/>                                                                                                                                                                    |
| [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md)<br/>             | 代表 CIE 的國際委員會 (電腦監視器的) 色彩特性。<br/>                                                                                                          |
| [**WmiMonitorConnectionParams**](wmimonitorconnectionparams.md)<br/>                     | 包含監視器的連線類型。<br/>                                                                                                                                                                        |
| [**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)<br/>                   | 包含的方法可取得視頻電子產品標準關聯之影片輸入定義的原始內容 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 1.x 標準128位元組資料區塊。<br/> |
| [**WmiMonitorDigitalVideoInputParams**](wmimonitordigitalvideoinputparams.md)<br/>       | 代表數位視訊的輸入參數。<br/>                                                                                                                                                                      |
| [**WmiMonitorID**](wmimonitorid.md)<br/>                                                 | 代表影片監視器的識別資訊，例如製造商名稱、製造年份或序號。<br/>                                                                                     |
| [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md)<br/>           | 列出監視器所支援的頻率範圍。<br/>                                                                                                                                                                |
| [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md)<br/> | 列出監視器描述項中影片監視器支援的來源模式（如果有的話）。<br/>                                                                                                                       |
| [**WmiMonitorRawEEdidV1Block**](wmimonitorraweedidv1block.md)<br/>                       | 表示來自視頻電子郵件標準關聯的原始資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 結構。<br/>                                                                      |
| [**XYZinCIE**](xyzincie.md)<br/>                                                         | 包含在照明上的國際委員會 (CIE) XYZ 色彩空間顯示的座標。<br/>                                                                                                      |



 

 

 




