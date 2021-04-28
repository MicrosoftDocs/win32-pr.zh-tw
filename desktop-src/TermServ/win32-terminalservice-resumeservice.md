---
title: 'Win32_Service 類別的 ResumeService 方法 (遠端桌面服務) '
description: Win32_Service 類別的 ResumeService 方法 (遠端桌面服務) -嘗試將參考的服務放在恢復狀態。
ms.assetid: AA020A0A-E69C-44AB-B259-A73460728770
ms.tgt_platform: multiple
keywords:
- ResumeService 方法遠端桌面服務
- ResumeService 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，ResumeService 方法
topic_type:
- apiref
api_name:
- Win32_Service.ResumeService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f8e7dcfc9b9bd5b408e36d8a909aa10c84519c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090586"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a>Win32_Service 類別的 ResumeService 方法 (遠端桌面服務) 

**ResumeService** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將參考的服務放在恢復狀態。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 ResumeService();
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

雖然已停止的服務和暫停的服務之間似乎沒有任何實際的差異，但是這兩個狀態會與 SCM 以不同方式顯示。 已停止的服務是指未執行的服務，必須經過整個服務啟動程式。 不過，已暫停的服務仍在執行中，但其運作已暫止。 因此，已暫停的服務不需要經過整個服務啟動程式，但需要不同的程式來繼續運作。

您必須使用適當的方法來啟動已停止的服務，或繼續已暫停的服務。 在下列情況下，應該使用 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 方法 [**StartService**](win32-terminalservice-startservice.md) 和 **ResumeService** ：

-   如果服務目前已停止，您必須使用 [**StartService**](win32-terminalservice-startservice.md) 方法來重新開機它。 **ResumeService** 無法啟動目前已停止的服務。
-   如果服務暫停，您必須使用 **ResumeService**。 如果您在已暫停的服務上使用 [**StartService**](win32-terminalservice-startservice.md) 方法，您會收到「服務已在執行中」的訊息。 不過，在繼續服務控制程式代碼傳送給它之前，服務會保持暫停狀態。

## <a name="examples"></a>範例

已暫停 VBScript 範例的 Resume 自動啟動 [服務會](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) 重新開機已暫停的任何自動啟動服務。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
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
</dt> </dl>

 

