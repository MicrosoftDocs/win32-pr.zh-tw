---
description: Windows 7 和 Windows Server 2008 R2 中的 AppInit_DLLs
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: Windows 7 AppInit_DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8741039952b0ea15d32b19bc48d4197ea13751bc492ff82fc8e67b1662d0b682
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031068"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>\_Windows 7 和 Windows Server 2008 R2 中的 AppInit dll

## <a name="platform"></a>平台

**客戶** 端-Windows 7  
**伺服器**-Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>描述

AppInit \_ dll 是一種機制，可讓您將任意 dll 清單載入系統上的每個使用者模式進程。 Microsoft 正在修改 Windows 7 和 Windows Server 2008 R2 中的 AppInit dll 設備，以加入新的程式碼簽署需求。 這將有助於改善系統的可靠性和效能，以及改善軟體來源的可見度。

## <a name="configuration"></a>組態

儲存在 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion Windows 機碼中的值會 \\ 決定 AppInit \_ dll 基礎結構的行為。 下表描述這些登錄值：



<table>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
<th>範例值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD) $ {REMOVE} $<br />
</td>
<td rowspan="2">全域啟用或停用 AppInit_DLLs。 $ {REMOVE} $<br />
</td>
<td>0x0 – AppInit_DLLs 已停用。</td>
</tr>
<tr class="even">
<td>0x1 –已啟用 AppInit_DLLs。</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ) </td>
<td>要載入之 Dll 的空格或逗號分隔清單。 DLL 的完整路徑應該使用簡短名稱來指定。</td>
<td>C：\PROGRA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD) $ {REMOVE} $<br />
</td>
<td rowspan="2">僅載入程式碼簽署的 Dll。 $ {REMOVE} $<br />
</td>
<td>0x0 –載入任何 Dll。</td>
</tr>
<tr class="odd">
<td>0x1 –僅載入程式碼簽署的 Dll。</td>


</tr>
</tbody>
</table>



 

**Windows 7**

AppInit dll 基礎結構載入的所有 Dll 都 \_ 應進行程式碼簽署。 在應用程式相容性的興趣方面，Windows 7 作業系統會載入所有 AppInit 的 dll。 不過，Microsoft 建議所有應用程式開發人員對其 dll 進行程式碼簽署，以協助改善 Windows 的可靠性，並準備好在未來的 Windows 版本中強制執行程式碼簽署。 RequireSignedAppInit \_ dll 登錄機碼會控制這個行為，而在 Windows 7 上的值預設會設定為0。

**Windows Server 2008 R2**

AppInit dll 基礎結構載入的所有 Dll 都 \_ 必須以程式碼簽署。 RequireSignedAppInit \_ dll 登錄機碼可控制這項行為，而在 Windows Server 2008 R2 上的值預設為1。

## <a name="links-to-other-resources"></a>其他資源的連結

<dl>

[Windows 7 和 Windows Server 2008 R2 中的 AppInit dll](/windows-hardware/drivers/install/)  
</dl>

 

 
