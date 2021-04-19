---
title: 'Win32_Service 類別的 StopService 方法 (Sdoias)  (終端機服務) '
description: 將由 Win32 TerminalService 物件表示的服務置於 \_ 已停止狀態。
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- StopService 方法遠端桌面服務
- StopService 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，StopService 方法
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106997805"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a>適用于終端機服務的 Win32_Service 類別的 StopService 方法 (Sdoias .h) 

**StopService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將服務（由 [**Win32 \_ TerminalService**](win32-terminalservice.md)物件表示）置於已停止狀態。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 StopService();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**0**
</dt> <dd>

要求已被接受。

</dd> <dt>

**1**
</dt> <dd>

不支援此要求。

</dd> <dt>

**2**
</dt> <dd>

使用者沒有必要的存取權。

</dd> <dt>

**3**
</dt> <dd>

無法停止此服務，因為與它相依的其他服務正在執行中。

</dd> <dt>

**4**
</dt> <dd>

要求的控制碼無效，或是服務不接受此控制碼。

</dd> <dt>

**5**
</dt> <dd>

因為服務的狀態 ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。

</dd> <dt>

**6**
</dt> <dd>

尚未啟動服務。

</dd> <dt>

**7**
</dt> <dd>

服務並未及時回應啟動要求。

</dd> <dt>

**8**
</dt> <dd>

啟動服務時發生未知的錯誤。

</dd> <dt>

**9**
</dt> <dd>

找不到服務可執行檔的目錄路徑。

</dd> <dt>

**10**
</dt> <dd>

服務已在執行中。

</dd> <dt>

**11**
</dt> <dd>

要加入新服務的資料庫已被鎖定。

</dd> <dt>

**12**
</dt> <dd>

這項服務所依賴的相依性已從系統中移除。

</dd> <dt>

**13**
</dt> <dd>

服務在相依的服務中找不到所需的服務。

</dd> <dt>

**14**
</dt> <dd>

已經從系統中停用服務。

</dd> <dt>

**15**
</dt> <dd>

此服務未通過驗證，無法在系統上執行。

</dd> <dt>

**16**
</dt> <dd>

這項服務正在從系統中移除。

</dd> <dt>

**17**
</dt> <dd>

服務沒有執行執行緒。

</dd> <dt>

**達**
</dt> <dd>

服務會在啟動時有迴圈相依性。

</dd> <dt>

**診斷**
</dt> <dd>

服務正在相同名稱下執行。

</dd> <dt>

**20**
</dt> <dd>

服務名稱包含不正確字元。

</dd> <dt>

**21**
</dt> <dd>

傳遞給服務的參數無效。

</dd> <dt>

**22**
</dt> <dd>

用來執行此服務的帳戶無效，或缺少執行服務的許可權。

</dd> <dt>

**23**
</dt> <dd>

服務存在於系統可使用之服務的資料庫中。

</dd> <dt>

**24**
</dt> <dd>

服務目前在系統中暫停。

</dd> </dl>

## <a name="remarks"></a>備註

確定可以停止或暫停的服務之後，您可以使用 **StopService** 和 [**PauseService**](win32-terminalservice-pauseservice.md) 方法來停止和暫停服務。 停止服務而非暫停服務（反之亦然）的決策取決於數個因素，包括下列各項：

-   服務是否能夠暫停？ 如果沒有，則您的唯一選項是停止服務。
-   您是否需要繼續處理已連線到服務的任何人的用戶端要求？ 若是如此，暫停服務通常會允許它處理現有的用戶端，同時拒絕存取新的用戶端。 相反地，當您停止服務時，所有用戶端都會立即中斷連線。
-   您是否需要重新設定服務，並讓變更立即生效？ 雖然服務屬性可以在服務暫停時變更，但大部分的服務都不會在服務實際停止並重新啟動之前生效。

停止服務所需的腳本程式碼與暫停服務所需的程式碼幾乎完全相同。

如果您嘗試停止具有相依服務的服務正在執行， **StopService** 方法會失敗，並傳回值3。 必須先停止相依的服務。

如果您停止服務，請立即檢查 [**Win32 \_ TerminalService**](win32-terminalservice.md)。**狀態** 屬性，因為值仍可能顯示服務為執行中。

## <a name="examples"></a>範例

[RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell 範例會設定遠端電腦的服務狀態。

[停止服務及其相依的](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732)VBScript 範例會停止服務和所有相依的服務。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Sdoias。h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[作業系統類別](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[WMI 工作：服務](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**PauseService**](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

