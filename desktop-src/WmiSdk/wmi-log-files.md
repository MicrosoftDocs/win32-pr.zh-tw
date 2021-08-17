---
description: WMI 使用事件追蹤 (ETW) ，而事件可以透過事件檢視器使用者介面或 Wevtutil 命令列工具取得。 如需詳細資訊，請參閱追蹤 WMI 活動。
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: WMI 記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fff9064dd82484568282f649b3380f544d9ba58a569e36583664806d47b5e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739425"
---
# <a name="wmi-log-files"></a>WMI 記錄檔

WMI 使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) ，而事件可以透過 **事件檢視器** 使用者介面或 Wevtutil 命令列工具取得。 如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。

-   [事件追蹤，而不是文字記錄](#event-tracing-instead-of-text-logs)
-   [WMI 記錄檔](#wmi-log-files)
-   [相關主題](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>事件追蹤，而不是文字記錄

WMI 服務活動會記錄在 WMITracing 檔案中。 如需啟用 WMI 事件追蹤和存取 WMITracing 的詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。 Windows (WDM) 提供者的驅動程式模型會繼續登入 Wbemprov .log 檔案。

## <a name="wmi-log-files"></a>WMI 記錄檔

WMI 服務和某些提供者會寫入文字記錄檔來記錄事件。

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[WMI 提供者記錄檔](wmi-provider-log-files.md)
</dt> <dd>

WMI 提供者也可以維護記錄。 哪些記錄檔會出現在系統上，視安裝的提供者而定。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 參考](wmi-reference.md)
</dt> <dt>

[追蹤 WMI 活動](tracing-wmi-activity.md)
</dt> <dt>

[記錄 WMI 活動](logging-wmi-activity.md)
</dt> </dl>

 

 
