---
description: 具有特殊許可權的作業需要安全性許可權，例如腳本 API 常數中的 SeLoadDriverPrivilege (wbemPrivilegeLoadDriver) ，也就是載入設備磁碟機的帳戶必須啟用的許可權。
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: 執行具有特殊許可權的作業
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce87a5783462be86d6e2e2b0565e93d811b972393319a34f84be2ab3d8e34c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050866"
---
# <a name="executing-privileged-operations"></a>執行具有特殊許可權的作業

具有特殊許可權的作業需要安全性許可權，例如 [腳本 API 常數](scripting-api-constants.md)中的 **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver**) ，也就是載入設備磁碟機的帳戶必須啟用的許可權。 您無法透過 WMI 將許可權新增至系統管理員或使用者，您只能啟用帳戶已經擁有的許可權。 如需許可權清單，請參閱 [**許可權 \_ 常數**](privilege-constants.md)。

根據預設，電腦上的本機使用者可以讀取 [*WMI 存放庫*](gloss-w.md)中的靜態資料、寫入提供者提供的實例，以及執行提供者方法，除非提供者強制執行其專屬的特殊安全性需求。 只有系統管理員可以連線 [到遠端電腦](connecting-to-wmi-on-a-remote-computer.md)、變更安全描述項，或變更靜態 wmi 儲存機制資料，例如 wmi 類別定義。 遠端連線會啟用擁有權限。 如需詳細資訊，請參閱 [保護遠端 WMI 連接](securing-a-remote-wmi-connection.md)。

C + + 的許可權常數不同于自動化語言（例如 Visual Basic）所使用的常數。 腳本必須使用常數的值，而不是名稱。 如需詳細資訊，請參閱使用 [c + + 執行特殊許可權作業](executing-privileged-operations-using-c-.md) 或 [使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)。

使用 WMI 時，拒絕存取錯誤的常見原因是缺少作業的已啟用許可權，例如取得 [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))的所有實例。 若未啟用 **SeSecurity** 許可權，就無法存取安全性記錄檔檔。

下列 VBScript 程式碼範例示範如何在標記字串中設定 **SeSecurity** 許可權。 在用於標記中時，以括弧括住的許可權名稱會卸載初始的「Se」。 如需詳細資訊，請參閱 [建立標記字串](constructing-a-moniker-string.md)。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**許可權常數**](privilege-constants.md)
</dt> </dl>

 

 
