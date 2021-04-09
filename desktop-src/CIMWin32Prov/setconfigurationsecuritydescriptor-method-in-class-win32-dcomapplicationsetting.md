---
description: 使用 Win32 SecurityDescriptor 類別的實例所定義的新安全描述項，更新 DCOM 應用程式的設定安全描述項 \_ 。
ms.assetid: e0fe3d2f-7641-4cae-972d-888e800548de
ms.tgt_platform: multiple
title: Win32_DCOMApplicationSetting 類別的 SetConfigurationSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8556e49d2e87e12763e3f0699bcff1f786ac1e72
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847084"
---
# <a name="setconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Win32 DCOMApplicationSetting 類別的 SetConfigurationSecurityDescriptor 方法 \_

**SetConfigurationSecurityDescriptor** 方法會使用 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)類別的實例所定義的新安全描述項，來更新 DCOM 應用程式的設定安全描述項。 此安全描述項會控制哪些人可以設定應用程式。 執行腳本或應用程式（呼叫這個方法）的帳戶必須具有 **SeSecurityPrivilege** 和 **SeRestorePrivilege** 許可權。 如需詳細資訊，請參閱 [變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)。

## <a name="syntax"></a>語法


```mof
uint32 SetConfigurationSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*描述* \[ 項在\]
</dt> <dd>

要針對 DCOM 應用程式設定的安全描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。 如需詳細資訊，請參閱 [WMI 傳回碼](/windows/desktop/WmiSdk/wmi-return-codes) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。

<dl> <dt>

「成功」
</dt> <dd>

0

成功完成

</dd> <dt>

**2**
</dt> <dd>

使用者無法存取所要求的資訊

</dd> <dt>

**8**
</dt> <dd>

未知的失敗

</dd> <dt>

**9**
</dt> <dd>

使用者沒有足夠的許可權來執行方法

</dd> <dt>

**21**
</dt> <dd>

在方法呼叫中指定的參數無效

</dd> <dt>

**其他**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>備註

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。 如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。 如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。

呼叫這個方法時，您可以同時更新 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例中的 dacl 和 SACL，但是您也可以只更新 dacl 或只更新 sacl。

[ [**安全 \_ 描述項] \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control) 中的下列值，可決定是否要更新 DACL、SACL 或兩者。

-   **\_有 SE DACL \_**

    表示 DACL 應該更新。 如果未設定此值，WMI 就會保留 DACL 的原始值。

-   **\_出現 SE SACL \_**

    指出 SACL 應該更新。 如果未設定此值，WMI 就會保留 SACL 的原始值。 若要更新 SACL，帳戶必須啟用 **SeSecurityPrivilege** 許可權。 針對腳本，許可權名稱為 **SeSecurityPrivilege**。 如需詳細資訊，請參閱 [**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)。

如果群組信任者和擁有者信任的屬性不是 **Null**，則會更新這些屬性。 否則，WMI 會保留原始值。 如需詳細資訊，請參閱 [WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)。

當新的 SACL 在呼叫這個方法時為 **Null** ，則目標安全物件上的安全描述項 SACL 會保持不變。

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

[**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

