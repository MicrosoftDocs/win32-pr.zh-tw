---
title: 使用 Windows 遠端管理
description: Windows 遠端管理的目的是要改善網路環境中，執行各種不同作業系統的裝置的硬體管理。
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092959"
---
# <a name="using-windows-remote-management"></a>使用 Windows 遠端管理

Windows 遠端管理的目的是要改善網路環境中，執行各種不同作業系統的裝置的硬體管理。 服務的整個設計重點在於實作可相互操作的通訊協定標準，以監看和管理遠端電腦。

由於 [Winrm 腳本 api](winrm-scripting-api.md) 和 [Winrm c + + api](winrm-c---api.md) 會執行為 WS-Management 的通訊協定所定義的作業，並將其接收 XML 資料流程以回應要求。 方法呼叫的輸入參數必須以 XML 來建立。 您可以使用 [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API 的方法來顯示或建立 XML 字串。 如需範例，請參閱 [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)。

下列清單包含說明如何使用 WinRM 腳本的主題：

-   [偵測遠端電腦是否支援 WS-Management 的通訊協定](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [從本機電腦取得資料](obtaining-data-from-the-local-computer.md)
-   [從遠端電腦取得資料](obtaining-data-from-a-remote-computer.md)
-   [列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)
-   [查詢資源的特定實例](querying-for-specific-instances-of-a-resource.md)
-   [顯示 WinRM 腳本的 XML 輸出](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a>追蹤 WinRM 活動

由於 WinRM 會透過 [Windows Management Instrumentation (wmi) ](/windows/desktop/WmiSdk/wmi-start-page)取得資料，因此您可以追蹤 WinRM 訊息所產生的 wmi 活動。 從 Windows Vista 開始，WMI 服務不再使用 [Wmi 記錄](/windows/desktop/WmiSdk/wmi-log-files)檔。 相反地，它會使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) ，而事件則是透過 **事件檢視器** UI 或 Evtutil 命令列工具提供。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 遠端管理](portal.md)
</dt> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[Windows 遠端管理參考](windows-remote-management-reference.md)
</dt> <dt>

[Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 