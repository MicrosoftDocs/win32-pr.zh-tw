---
description: 傳回控制服務存取的安全描述項。
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者的 Win32_Service 類別的 GetSecurityDescriptor 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf8dee49893a5a1d3b628e72b0b0746a6215fb0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025883"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a> (CIMWin32 WMI 提供者的 Win32_Service 類別的 GetSecurityDescriptor 方法) 

**GetSecurityDescriptor** 方法會傳回控制服務存取權的安全描述項。 描述項會以 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的實例傳回。

## <a name="syntax"></a>語法


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*描述* \[ 項擴展\]
</dt> <dd>

與服務相關聯的安全描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

「成功」
</dt> <dd>

0

要求已被接受。

</dd> <dt>


</dt> <dd>

1

不支援此要求。

</dd> <dt>

**拒絕存取**
</dt> <dd>

2

使用者沒有必要的存取權。

</dd> <dt>


</dt> <dd>

3

無法停止此服務，因為與它相依的其他服務正在執行中。

</dd> <dt>


</dt> <dd>

4

要求的控制碼無效，或是服務不接受此控制碼。

</dd> <dt>


</dt> <dd>

5

因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。

</dd> <dt>


</dt> <dd>

6

尚未啟動服務。

</dd> <dt>


</dt> <dd>

7

服務並未及時回應啟動要求。

</dd> <dt>

**未知的失敗**
</dt> <dd>

8

啟動服務時發生未知的錯誤。

</dd> <dt>

**缺少許可權**
</dt> <dd>

9

找不到服務可執行檔的目錄路徑。

</dd> <dt>


</dt> <dd>

10

服務已在執行中。

</dd> <dt>


</dt> <dd>

11

要加入新服務的資料庫已被鎖定。

</dd> <dt>


</dt> <dd>

12

這項服務所依賴的相依性已從系統中移除。

</dd> <dt>


</dt> <dd>

13

服務在相依的服務中找不到所需的服務。

</dd> <dt>


</dt> <dd>

14

已經從系統中停用服務。

</dd> <dt>


</dt> <dd>

15

此服務未通過驗證，無法在系統上執行。

</dd> <dt>


</dt> <dd>

16

這項服務正在從系統中移除。

</dd> <dt>


</dt> <dd>

17

服務沒有執行執行緒。

</dd> <dt>


</dt> <dd>

18

服務會在啟動時有迴圈相依性。

</dd> <dt>


</dt> <dd>

19

服務正在相同名稱下執行。

</dd> <dt>


</dt> <dd>

20

服務名稱包含不正確字元。

</dd> <dt>

**參數不正確**
</dt> <dd>

21

傳遞給服務的參數無效。

</dd> <dt>


</dt> <dd>

22

用來執行此服務的帳戶無效，或缺少執行服務的許可權。

</dd> <dt>


</dt> <dd>

23

服務存在於系統可使用之服務的資料庫中。

</dd> <dt>


</dt> <dd>

24

服務目前在系統中暫停。

</dd> <dt>

**其他**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="remarks"></a>備註

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。 如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。 如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。

## <a name="examples"></a>範例

在 VBScript 中取出安全描述項時，請務必以系統管理員身分執行，並以系統管理員身分執行，如下列程式碼片段所示。 否則，您的程式碼可能會擲回許可權錯誤。


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



同樣地，在 VB.NET 中，請務必設定 "EnablePrivileges = True"，並以系統管理員身分執行應用程式。


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 服務**](win32-service.md)
</dt> <dt>

[**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

