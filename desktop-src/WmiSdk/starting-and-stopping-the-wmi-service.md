---
description: WMI 以服務的形式執行，其顯示名稱為 &\# 0034; Windows Management Instrumentation&\# 0034; 以及服務名稱 &\# 0034; winmgmt&\# 0034;。
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: 啟動和停止 WMI 服務
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b22524d356bad5f23f4ca1cc8a3e7c68e69fd83f0dc38e64eba70bc1812436f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315006"
---
# <a name="starting-and-stopping-the-wmi-service"></a>啟動和停止 WMI 服務

WMI 會以服務的形式執行，其顯示名稱為 "Windows Management Instrumentation"，服務名稱為 "winmgmt"。 在系統啟動時，會自動在 LocalSystem 帳戶下執行 WMI。 如果 WMI 未執行，它會在第一個管理應用程式或腳本要求與 WMI 命名空間的連接時自動啟動。

根據系統執行的作業系統版本而定，有數個其他服務相依于 WMI 服務。

## <a name="starting-winmgmt-service"></a>正在啟動 Winmgmt 服務

下列程式說明如何啟動 WMI 服務。

**啟動 Winmgmt 服務**

1.  在命令提示字元中，輸入 **net** **start** **winmgmt** \[ */<switch>* \] 。

    如需可用參數的詳細資訊，請參閱 [winmgmt](winmgmt.md)。 您可以使用內建的系統管理員帳戶，或以較高的許可權執行的 Administrators 群組中的帳戶，以啟動 WMI 服務。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。

2.  其他相依于 WMI 服務的服務（例如 SMS Agent Host 或 Windows Firewall）將不會自動重新開機。

## <a name="stopping-winmgmt-service"></a>停止 Winmgmt 服務

下列程式說明如何停止 WMI 服務。

**停止 Winmgmt 服務**

1.  在命令提示字元中，輸入 **net stop winmgmt**。

2.  其他相依于 WMI 服務的服務也會停止，例如 SMS Agent Host 或 Windows 防火牆。

## <a name="examples"></a>範例

TechNet 資源庫包含 [WMI service 看門狗腳本](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282)，說明如何使用 PowerShell 以程式設計方式關閉和重新開機 winmgmt 服務。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WMI Command-Line 工具](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



