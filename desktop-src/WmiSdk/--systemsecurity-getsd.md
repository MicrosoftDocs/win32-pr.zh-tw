---
description: 取得使用者所連接之命名空間的安全描述項。 這個方法會以二進位位元組陣列格式傳回安全描述項。 如果您要撰寫腳本，請使用 GetSecurityDescriptor 方法。
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 GetSD 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987573"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a>\_ \_ SystemSecurity 類別的 GetSD 方法

**GetSD** 方法會取得使用者所連接之命名空間的安全描述項。 這個方法會以二進位位元組陣列格式傳回安全描述項。 如果您要撰寫腳本，請使用 [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) 方法。 如需詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

使用者必須擁有「 **讀取 \_ 控制** 」許可權。 依預設，系統管理員擁有該許可權。 實際使用之安全描述項的唯一部分是 (DACL) 的任意存取控制清單。 DACL 可以包含繼承的和非繼承的 Ace。 拒絕和允許 Ace 都是允許的。

如果您是使用 c + + 進行程式設計，您可以使用 [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)來操作二進位安全描述項，以及 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)的轉換方法。

## <a name="syntax"></a>語法


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SD* \[擴展\]
</dt> <dd>

二進位位元組陣列格式的安全描述項。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **HRESULT** ，指出方法呼叫的狀態。 下列清單列出對 **GetSD** 而言很重要的傳回值。 針對編寫腳本和 Visual Basic 應用程式，可以從 OutParameters 取得結果 [ReturnValue](parsing-outparameters-objects.md)。 如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。

<dl> <dt>

**S \_ 確定**
</dt> <dd>

已成功執行方法。

</dd> <dt>

**WBEM \_ E \_ \_ 拒絕存取**
</dt> <dd>

呼叫端沒有足夠的許可權可以呼叫這個方法。

</dd> <dt>

**\_ \_ \_ 已停用 WBEM E 方法**
</dt> <dd>

嘗試在不支援的系統上執行這個方法。

</dd> </dl>

## <a name="remarks"></a>備註

如需以程式設計方式或手動方式修改命名空間安全性的詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md)。

## <a name="examples"></a>範例

下列腳本會示範如何使用 **GetSD** 來取得根 Cimv2 命名空間的目前安全描述項 \\ ，並將其變更為 **DisplaySD** 中顯示的位元組陣列。


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_\_SystemSecurity::SetSD**](--systemsecurity-setsd.md)
</dt> <dt>

[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[保護 WMI 命名空間](securing-wmi-namespaces.md)
</dt> </dl>

 

