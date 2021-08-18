---
description: 為使用者所連接的命名空間設定安全描述項。 這個方法需要二進位位元組陣列格式的安全描述項。 如果您要撰寫腳本，請使用 SetSecurityDescriptor 方法。
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: __SystemSecurity 類別的 SetSD 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 04da59b6370e2e9a381f2e3889b75ac37cb926e54c46cc0e616ec5353ed6f665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132031"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>\_ \_ SystemSecurity 類別的 SetSD 方法

**SetSD** 方法會設定使用者所連接之命名空間的安全描述項。 這個方法需要二進位位元組陣列格式的安全描述項。 如果您要撰寫腳本，請使用 [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) 方法。 如需詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。

如果您是使用 c + + 進行程式設計，您可以使用 [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)來操作二進位安全描述項，以及 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)的轉換方法。

使用者必須擁有「 **寫入 \_ DAC** 」許可權，而且根據預設，系統管理員具有該許可權。 安全描述項中唯一使用的部分是 noninherited 存取控制專案， (ACE) 在任意存取控制清單 (DACL) 中。 藉由設定 Ace 中的 **容器 \_ 繼承** 旗標，安全描述項會影響子命名空間。 允許和拒絕 Ace 都是允許的。

> [!Note]  
> 因為 DACL 中允許使用 deny 和 allow Ace，所以 Ace 的順序很重要。 如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。

 

## <a name="syntax"></a>語法


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SD* \[在\]
</dt> <dd>

組成安全描述項的位元組陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** ，指出方法呼叫的狀態。 針對編寫腳本和 Visual Basic 應用程式，可以從 OutParameters 取得結果[ReturnValue](parsing-outparameters-objects.md)。 如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。

下列清單列出對 **SetSD** 很重要的傳回值。

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

嘗試在不支援的作業系統上執行此方法。

</dd> <dt>

**WBEM \_ E \_ 不正確 \_ 物件**
</dt> <dd>

SD 不會通過基本有效性測試。

</dd> <dt>

**WBEM \_ E \_ 不正確 \_ 參數**
</dt> <dd>

SD 因為下列其中一項而無效：

-   遺漏 DACL。
-   DACL 無效。
-   ACE 已設定 **wbem \_ FULL \_ write \_ rep** 旗標，且未設定 **wbem \_ 部分 \_ 寫入 \_ 代表** 或 **wbem \_ 寫入 \_ 提供者** 旗標。
-   ACE 具有 **\_ 僅限繼承 \_ ace** 旗標的設定，而不含 **CONTAINER \_ INHERIT \_ ace** 旗標。
-   ACE 有未知的存取位集。
-   ACE 的旗標設定不在資料表中。
-   ACE 的型別不在資料表中。
-   SD 缺少擁有者和群組。

如需存取控制專案 (ACE) 旗標的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。

</dd> </dl>

## <a name="remarks"></a>備註

如需以程式設計方式或手動方式修改命名空間安全性的詳細資訊，請參閱 [保護 WMI 命名空間](securing-wmi-namespaces.md)。

## <a name="examples"></a>範例

下列腳本示範如何使用 **SetSD** 來設定根命名空間的命名空間安全描述項，並將其變更為 *strSD* 中顯示的位元組陣列。


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



下列 c # 程式碼範例會使用 AccessControl 來列舉、插入和移除 RawSecurityDescriptor. Objdescriptor.discretionaryacl 中的新 CommonAce 物件，然後再將它轉換回位元組陣列，以透過 SetSD 加以儲存。 您可以使用 NTAccount 和轉譯來取出 SecurityIdentifier。


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

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

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[保護 WMI 命名空間](securing-wmi-namespaces.md)
</dt> </dl>

 

