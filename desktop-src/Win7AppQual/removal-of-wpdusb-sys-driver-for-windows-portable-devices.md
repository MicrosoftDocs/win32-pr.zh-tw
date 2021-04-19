---
description: .
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: 移除 Windows 可攜式裝置的 WPDUSB.SYS 驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d602c8277a5c256332b3eaec6a383997d5c63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987775"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>移除 Windows 可攜式裝置的 WPDUSB.SYS 驅動程式

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>Description

Microsoft 已將 windows Vista USB 驅動程式堆疊 (WPDUSB.SYS) 的核心模式元件取代為一般 WINUSB.SYS 驅動程式 (WPD) 。 與原始 WPDUSB.SYS 驅動程式進行通訊的方式，是透過私用 i/o 控制項 (IOCTL) 程式碼;這些服務的支援也已被移除。

這些 IOCTL 程式碼的任何取用者都必須負責適當地解讀和實行媒體傳輸通訊協定， (MTP) 。 Windows Vista 不支援協力廠商應用程式使用這些 IOCTL 程式碼。

## <a name="manifestation-of-impact"></a>影響的表現

任何相依于這些私用 IOCTL 程式碼可用性的應用程式，都將無法再存取 USB 連接的 MTP 裝置。

## <a name="mitigation"></a>降低

相依于私用 IOCTL 程式碼之應用程式的使用者，必須使用不同的應用程式 (或應用程式的更新版本) 存取 USB 連接的 MTP 裝置。

## <a name="solution"></a>解決方法

應用程式應該使用 Windows 可攜式裝置 (WPD) API 來尋找任何 WPD 裝置並與其互動。 雖然 WPD 裝置的大量百分比會實作為與電腦通訊的 MTP，但 WPD 並不只限于 MTP 裝置。 此外，透過私用 IOCTLs 直接存取裝置會限制應用程式只能與 USB 連接的裝置進行通訊，使用 WPD API 會將連線選項清單擴充到其他通訊協定 (例如，Wi-fi) 。 在罕見的情況下，當應用程式必須是 MTP 感知時，WPD API 會提供原始 MTP 命令的傳遞機制。

## <a name="leveraging-feature-capabilities"></a>運用功能功能

Windows XP (透過 windows 格式 SDK) 、Windows Vista 和 Windows 7 支援 WPD API。 Windows 7 的 WPD 執行透過藍牙新增對 MTP 的支援。

## <a name="links-to-other-resources"></a>其他資源的連結

[Windows 可攜式裝置](../windows-portable-devices.md)

 

 
