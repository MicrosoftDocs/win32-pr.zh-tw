---
description: 寫入控制印表機存取權之安全描述項的更新版本。
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Win32_Printer 類別的 SetSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8621c1977c4553f610299695c2c68a72f5a9d6f2ecfcbe6df46b8646c379c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958956"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a>Win32 Printer 類別的 SetSecurityDescriptor 方法 \_

**SetSecurityDescriptor** 方法會寫入控制印表機存取權之安全描述項的更新版本。 安全描述項是 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例。 如需詳細資訊，請參閱 [變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

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

與印表機相關聯的安全描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**0**
</dt> <dd>

順利完成。

</dd> <dt>

**2**
</dt> <dd>

使用者無法存取所要求的資訊。

</dd> <dt>

**8**
</dt> <dd>

未知的失敗。

</dd> <dt>

**9**
</dt> <dd>

使用者沒有足夠的許可權來執行方法。

</dd> <dt>

**21**
</dt> <dd>

在方法呼叫中指定的參數無效。

</dd> </dl>

## <a name="remarks"></a>備註

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。 如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。 如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。

呼叫這個方法時，您可以同時更新 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例中的 dacl 和 SACL，但是您也可以只更新 dacl 或只更新 sacl。

下列 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control) 中的值會決定是否要更新 DACL、SACL 或兩者。

-   **SE \_DACL \_ 存在**

    表示 DACL 應該更新。 如果未設定此值，WMI 就會保留 DACL 的原始值。

-   **SE \_SACL \_ 存在**

    指出 SACL 應該更新。 如果未設定此值，WMI 就會保留 SACL 的原始值。 若要更新 SACL，帳戶必須啟用 **SeSecurityPrivilege** 許可權。 針對腳本，許可權名稱為 **SeSecurityPrivilege**。 如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)。

如果群組信任者和擁有者信任的屬性不是 **Null**，則會更新這些屬性。 否則，WMI 會保留原始值。 如需詳細資訊，請參閱 [WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)。

當新的 SACL 在呼叫這個方法時為 **Null** ，則目標安全物件上的安全描述項 SACL 會保持不變。

## <a name="examples"></a>範例

[ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) PowerShell 範例會將許可權 (ACL) 從某個印表機取代為另一個印表機。

下列 PowerShell 程式碼範例說明如何設定印表機的安全描述項。


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ 印表機。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 印表機**](win32-printer.md)
</dt> <dt>

[**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

