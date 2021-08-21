---
description: 寫入安全描述項的更新版本，以控制您所連接之 WMI 命名空間的存取權。 安全描述項會以 SecurityDescriptor 的實例來表示 \_ \_ 。
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 SetSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d44322820514fc676c1b3ad304375f5f3ce8966a73217c6505f24659914f7853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315625"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a>\_ \_ SystemSecurity 類別的 SetSecurityDescriptor 方法

[**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer)方法會寫入安全描述項的更新版本，以控制您所連接之 WMI 命名空間的存取權。 安全描述項會以 [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)的實例來表示。 如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

## <a name="syntax"></a>語法


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*描述* \[ 項在\]
</dt> <dd>

與 WMI 命名空間相關聯的安全描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。 如需詳細資訊，請參閱 [WMI 傳回碼](wmi-return-codes.md) 或 [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)。

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

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/a-gly)。 如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。 如需詳細資訊，請參閱 [**許可權常數**](privilege-constants.md) 和 [執行特殊許可權作業](executing-privileged-operations.md)。

呼叫這個方法時，您可以同時更新 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 實例中的 dacl 和 SACL，但是您也可以只更新 dacl 或只更新 sacl。

下列 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control) 中的值會決定是否要更新 DACL 或 SACL 或兩者。

-   **SE \_DACL \_ 存在**

    表示 DACL 應該更新。 如果未設定此值，WMI 就會保留 DACL 的原始值。

-   **SE \_SACL \_ 存在**

    指出 SACL 應該更新。 如果未設定此值，WMI 就會保留 SACL 的原始值。 若要更新 SACL，帳戶必須啟用 **SeSecurityPrivilege** 許可權。 針對腳本，許可權名稱為 **SeSecurityPrivilege**。 如需詳細資訊，請參閱 [**許可權常數**](privilege-constants.md)。

如果群組信任者和擁有者信任的屬性不是 **Null**，則會更新這些屬性。 否則，WMI 會保留原始值。 如需詳細資訊，請參閱 [WMI 安全描述項物件](wmi-security-descriptor-objects.md)。

當中的新 SACL 是 **Null** 時，在呼叫這個方法時，目標安全物件上的安全描述項 SACL 會保持不變。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> </dl>

 

