---
description: WMI Windows PowerShell 命令類別的受控參考
ms.assetid: 30e77956-8428-4259-9218-b93f143fd987
ms.tgt_platform: multiple
title: WMI Windows PowerShell 命令類別的受控參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb309a9ca421a3966f84ba1ae825bd0c81eee8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997562"
---
# <a name="managed-reference-for-wmi-windows-powershell-command-classes"></a>WMI Windows PowerShell 命令類別的受控參考

Windows PowerShell 透過一組 Cmdlet 來執行 Windows Management Instrumentation (WMI) 功能。 您可以使用這些 Cmdlet 來完成管理本機和遠端電腦所需的端對端工作。

如需詳細資訊，請參閱 [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) 。

## <a name="wmi-powershell-classes"></a>WMI PowerShell 類別

**命名空間**： Microsoft. 命令

**元件**： Microsoft. 命令. 管理

**DLL**： Microsoft.PowerShell.Commands.Management.dll

這些 WMI 命令類別是由 Windows PowerShell 所執行。 這些類別包含在此軟體發展工具組中， (SDK) 僅供完整性之用。 這些類別的成員不能直接使用，也不能用來衍生其他類別。



| 類別                   | 描述                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GetWmiObjectCommand     | 取得 WMI 類別的實例或可用類別的相關資訊。<br/> 如需有關參數的範例和詳細資訊，請參閱 [>get-wmiobject](/previous-versions//dd315295(v=technet.10)) Cmdlet。<br/> |
| InvokeWmiMethod         | 呼叫 WMI 方法。<br/> 如需有關參數的範例和詳細資訊，請參閱 [>invoke-wmimethod](/previous-versions//dd315300(v=technet.10)) Cmdlet。<br/>                                                     |
| RegisterWmiEventCommand | 訂閱 WMI 事件。<br/> 如需有關參數的範例和詳細資訊，請參閱 [>register-wmievent](/previous-versions//dd315242(v=technet.10)) Cmdlet。<br/>                                            |
| RemoveWmiObject         | 刪除現有 WMI 類別的實例。<br/> 如需有關參數的範例和詳細資訊，請參閱 [>get-wmiobject](/previous-versions//dd347605(v=technet.10)) Cmdlet。<br/>                          |
| SetWmiInstance          | 建立或更新現有 WMI 類別的實例。<br/> 如需有關參數的範例和詳細資訊，請參閱 [set-wmiinstance](/previous-versions//dd315391(v=technet.10)) Cmdlet。<br/>                |



 

 

