---
description: 取得安全描述項，可控制您所連接之 WMI 命名空間的存取權。 安全描述項會以 SecurityDescriptor 的實例傳回 \_ \_ 。
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 GetSecurityDescriptor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 77053174878db77409c525510acb54740ac8ad5c5c0505af5bf6ff8421cdf737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050856"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a>\_ \_ SystemSecurity 類別的 GetSecurityDescriptor 方法

**GetSecurityDescriptor** 方法會取得安全描述項，以控制您所連接之 WMI 命名空間的存取權。 安全描述項會以 [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)的實例傳回。 如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

## <a name="syntax"></a>語法


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*描述* \[ 項擴展\]
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

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)實例代表 [**安全 \_ 描述項 \_ 控制項**](/windows/desktop/SecAuthZ/security-descriptor-control)資料類型，並包含 (DACL) 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly)，以及 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly)。 如需詳細資訊，請參閱 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

如果未在取得安全描述項時授與或啟用 **SeSecurityPrivilege** ，則只會傳回傳回的安全描述項中的 DACL。 如需詳細資訊，請參閱 [**許可權常數**](privilege-constants.md) 和 [執行特殊許可權作業](executing-privileged-operations.md)。

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

 

