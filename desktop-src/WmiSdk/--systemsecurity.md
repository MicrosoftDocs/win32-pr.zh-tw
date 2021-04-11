---
description: 包含方法，可讓您存取和修改命名空間的安全性設定。
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: __SystemSecurity 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115968"
---
# <a name="__systemsecurity-class"></a>\_\_SystemSecurity 類別

**\_ \_ SystemSecurity** 系統類別包含的方法可讓您存取和修改命名空間的安全性設定。 **\_ \_ SystemSecurity** 類別是每個命名空間中的單一類別。

> [!Note]  
> 如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a>成員

**\_ \_ SystemSecurity** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**\_ \_ SystemSecurity** 類別有這些方法。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">方法</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></td>
<td style="text-align: left;">取得允許遠端存取的使用者清單。<br/>
<blockquote>
[!Note]<br />
這個方法不適用於支援的 Windows 版本。 請改用 <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> 。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></td>
<td style="text-align: left;">傳回遮罩，其中每個位都對應至存取權限。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></td>
<td style="text-align: left;">取得使用者所連接的命名空間 <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> 。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></td>
<td style="text-align: left;">取得安全描述項，可控制與 <strong>__SystemSecurity</strong>實例相關聯之 WMI 命名空間的存取權。 安全描述項會以<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>的實例傳回。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></td>
<td style="text-align: left;">設定允許遠端存取的使用者清單。<br/>
<blockquote>
[!Note]<br />
這個方法不適用於支援的 Windows 版本。 請改用 <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> 。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></td>
<td style="text-align: left;">為使用者所連接的命名空間設定安全描述項。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></td>
<td style="text-align: left;">寫入控制印表機存取權之安全描述項的更新版本。 安全描述項是由 <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>的實例表示。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

您可以要求用戶端腳本和應用程式使用加密的連接來進行驗證，方法是將 **RequiresEncryption** 限定詞新增至建立命名空間的 mof 檔案。 您也可以藉由新增這個屬性來修改現有的命名空間，然後再編譯一次 mof 檔案。 如需如何使用 **RequiresEncryption** 的詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。

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

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[WMI 安全描述項物件](wmi-security-descriptor-objects.md)
</dt> <dt>

[保護 WMI 命名空間](securing-wmi-namespaces.md)
</dt> <dt>

[建立命名空間安全性的繼承](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[ (Acl 的存取控制清單) ](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

