---
description: 腳本可以存取硬體和軟體物件的所有 WMI 類別。
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: 腳本存取 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0169da5b2d7d9d542d7fe686ae34f5bf2aeb3c4fdfff1e268dc3ca2bfdddd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992388"
---
# <a name="scripting-access-to-wmi"></a>腳本存取 WMI

腳本可以存取硬體和軟體物件的所有 WMI 類別。 Windows腳本主機 (WSH) 腳本可以對檔案系統物件執行作業、操作網路印表機，或變更環境變數。 您可以找到各種系統管理員工作，以及如何在 WMI 中完成 [腳本和應用程式之 wmi](wmi-tasks-for-scripts-and-applications.md)工作的簡單指引。 如需詳細資訊和範例，請參閱 TechNet ScriptCenter [腳本存放庫](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)。

如果您不熟悉腳本或 WMI 特定腳本，請參閱 TechNet ScriptCenter 一節 [開始使用](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx)。

透過 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)，您可以開發快速、簡單的腳本或複雜的應用程式。 腳本提供您取得資訊或在企業中設定大部分物件的相同功能，如同透過 c + + 或 c # 應用程式所做的一樣。 如需詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

您無法在腳本中寫入 [*WMI 提供者*](gloss-p.md) 。 如需詳細資訊，請參閱 [將資料提供給 WMI](providing-data-to-wmi.md)。

您可以使用任何可與 ActiveX 物件互動的指令碼語言來撰寫 WMI 腳本。

Windows PowerShell 為 WMI 管理和腳本提供簡單的環境。 如需 PowerShell 的詳細資訊，請參閱[開始使用與 Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true)。

Active Directory 服務介面 (ADSI) 腳本提供 Active Directory Domain Services (AD DS 物件的存取權。 WSH 和 ADSI 腳本都會存取物件，並允許無法透過批次檔使用的程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 WMI](about-wmi.md)
</dt> <dt>

[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)
</dt> </dl>

 

 
