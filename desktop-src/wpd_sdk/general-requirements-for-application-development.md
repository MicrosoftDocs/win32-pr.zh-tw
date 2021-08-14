---
description: 應用程式開發的一般需求
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: 應用程式開發 (WPD API) 的一般需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad1ed207774494102f673bd7fb4f92acbdcb4629542d238613637d9509336c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430877"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>應用程式開發 (WPD API) 的一般需求

若要建立 Windows 可攜式裝置應用程式，您必須在電腦上安裝[Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads) 。 必要的標頭和程式庫會出現在下列清單中。

-   PortableDeviceGuids .lib
-   PortableDevice。h
-   PortableDeviceTypes。h
-   PortableDeviceApi。h
-   應用程式所需的任何其他必要程式庫和標頭，以取用或轉譯媒體檔案。

如果您的應用程式支援新的裝置服務介面，它也會包含下列一或多個標頭檔。

-   AnchorSyncDeviceService。h
-   BridgeDeviceService。h
-   CalendarDeviceService。h
-   ContactDeviceService。h
-   DeviceServices。h
-   FullEnumSyncDeviceService。h
-   HintsDeviceService。h
-   MessageDeviceService。h
-   MetadataDeviceService。h
-   NotesDeviceService。h
-   RingtoneDeviceService。h
-   StatusDeviceService。h
-   SyncDeviceService。h
-   TaskDeviceService。h

在上述清單中，幾乎所有支援裝置服務的應用程式都需要 BridgeDeviceService .h 和 DeviceService。其他檔案會定義不同類型的裝置服務，並且會適當地納入。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows 可攜式裝置**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
