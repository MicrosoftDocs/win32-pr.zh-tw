---
title: 'Win32_Service 類別的 SetSecurityDescriptor 方法 (遠端桌面服務) '
description: 寫入安全描述項的更新版本，以控制服務的存取權。
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- 腳本 Windows Management Instrumentation，安全性
- 安全性 Windows Management Instrumentation，腳本
- SetSecurityDescriptor 方法遠端桌面服務
- SetSecurityDescriptor 方法遠端桌面服務，Win32_Service 類別
- Win32_Service 類別遠端桌面服務，SetSecurityDescriptor 方法
topic_type:
- apiref
api_name:
- Win32_Service.SetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a21f9730b4c1c0ab7b3ccf662ddb2d95da2ee2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686420"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a>Win32_Service 類別的 SetSecurityDescriptor 方法 (遠端桌面服務) 

**SetSecurityDescriptor** 方法會寫入控制服務存取權之安全描述項的更新版本。

## <a name="syntax"></a>語法


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*描述* \[ 項在\]
</dt> <dd>

與服務相關聯的安全描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

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

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。 如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。 如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。

呼叫這個方法時，您可以同時更新 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例中的 dacl 和 SACL，但是您也可以只更新 dacl 或只更新 sacl。

下列 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control) 中的值會決定是否要更新 DACL、SACL 或兩者。

-   **\_有 SE DACL \_**

    表示 DACL 應該更新。 如果未設定此值，WMI 就會保留 DACL 的原始值。

-   **\_出現 SE SACL \_**

    指出 SACL 應該更新。 如果未設定此值，WMI 就會保留 SACL 的原始值。 若要更新 SACL，帳戶必須啟用 **SeSecurityPrivilege** 許可權。 針對腳本，許可權名稱為 **SeSecurityPrivilege**。 如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)。

如果群組信任者和擁有者信任的屬性不是 **Null**，則會更新這些屬性。 否則，WMI 會保留原始值。 如需詳細資訊，請參閱 [WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)。

當中的新 SACL 是 **Null** 時，在呼叫這個方法時，目標安全物件上的安全描述項 SACL 會保持不變。

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

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

