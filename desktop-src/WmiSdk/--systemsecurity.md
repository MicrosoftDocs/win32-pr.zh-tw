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
# <a name="__systemsecurity-class"></a><span data-ttu-id="13f53-103">\_\_SystemSecurity 類別</span><span class="sxs-lookup"><span data-stu-id="13f53-103">\_\_SystemSecurity class</span></span>

<span data-ttu-id="13f53-104">**\_ \_ SystemSecurity** 系統類別包含的方法可讓您存取和修改命名空間的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="13f53-104">The **\_\_SystemSecurity** system class contains methods that let you access and modify the security settings for a namespace.</span></span> <span data-ttu-id="13f53-105">**\_ \_ SystemSecurity** 類別是每個命名空間中的單一類別。</span><span class="sxs-lookup"><span data-stu-id="13f53-105">The **\_\_SystemSecurity** class is a singleton class in each namespace.</span></span>

> [!Note]  
> <span data-ttu-id="13f53-106">如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。</span><span class="sxs-lookup"><span data-stu-id="13f53-106">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

 

<span data-ttu-id="13f53-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="13f53-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="13f53-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="13f53-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f53-109">語法</span><span class="sxs-lookup"><span data-stu-id="13f53-109">Syntax</span></span>

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a><span data-ttu-id="13f53-110">成員</span><span class="sxs-lookup"><span data-stu-id="13f53-110">Members</span></span>

<span data-ttu-id="13f53-111">**\_ \_ SystemSecurity** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="13f53-111">The **\_\_SystemSecurity** class has these types of members:</span></span>

-   [<span data-ttu-id="13f53-112">方法</span><span class="sxs-lookup"><span data-stu-id="13f53-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="13f53-113">方法</span><span class="sxs-lookup"><span data-stu-id="13f53-113">Methods</span></span>

<span data-ttu-id="13f53-114">**\_ \_ SystemSecurity** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="13f53-114">The **\_\_SystemSecurity** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="13f53-115">方法</span><span class="sxs-lookup"><span data-stu-id="13f53-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="13f53-116">描述</span><span class="sxs-lookup"><span data-stu-id="13f53-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="13f53-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="13f53-117"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13f53-118">取得允許遠端存取的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="13f53-118">Gets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="13f53-119">這個方法不適用於支援的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="13f53-119">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="13f53-120">請改用 <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="13f53-120">Use <a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="13f53-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span><span class="sxs-lookup"><span data-stu-id="13f53-121"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13f53-122">傳回遮罩，其中每個位都對應至存取權限。</span><span class="sxs-lookup"><span data-stu-id="13f53-122">Returns a mask with each bit that corresponds to an access right.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="13f53-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span><span class="sxs-lookup"><span data-stu-id="13f53-123"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13f53-124">取得使用者所連接的命名空間 <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="13f53-124">Gets the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="13f53-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="13f53-125"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13f53-126">取得安全描述項，可控制與 <strong>__SystemSecurity</strong>實例相關聯之 WMI 命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="13f53-126">Gets the security descriptor that controls access to the WMI namespace associated with the instance of <strong>__SystemSecurity</strong>.</span></span> <span data-ttu-id="13f53-127">安全描述項會以<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>的實例傳回。</span><span class="sxs-lookup"><span data-stu-id="13f53-127">The security descriptor is returned as an instance of<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="13f53-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span><span class="sxs-lookup"><span data-stu-id="13f53-128"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13f53-129">設定允許遠端存取的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="13f53-129">Sets a list of users who are allowed remote access.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="13f53-130">這個方法不適用於支援的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="13f53-130">This method does not work on supported versions of Windows.</span></span> <span data-ttu-id="13f53-131">請改用 <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="13f53-131">Use <a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="13f53-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span><span class="sxs-lookup"><span data-stu-id="13f53-132"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13f53-133">為使用者所連接的命名空間設定安全描述項。</span><span class="sxs-lookup"><span data-stu-id="13f53-133">Sets the security descriptor for the namespace to which the user is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="13f53-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="13f53-134"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="13f53-135">寫入控制印表機存取權之安全描述項的更新版本。</span><span class="sxs-lookup"><span data-stu-id="13f53-135">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="13f53-136">安全描述項是由 <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>的實例表示。</span><span class="sxs-lookup"><span data-stu-id="13f53-136">The security descriptor is represented by an instance of <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="13f53-137">備註</span><span class="sxs-lookup"><span data-stu-id="13f53-137">Remarks</span></span>

<span data-ttu-id="13f53-138">您可以要求用戶端腳本和應用程式使用加密的連接來進行驗證，方法是將 **RequiresEncryption** 限定詞新增至建立命名空間的 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="13f53-138">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="13f53-139">您也可以藉由新增這個屬性來修改現有的命名空間，然後再編譯一次 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="13f53-139">You can also modify an existing namespace by adding this attribute and compile the .mof file again.</span></span> <span data-ttu-id="13f53-140">如需如何使用 **RequiresEncryption** 的詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="13f53-140">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13f53-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="13f53-141">Requirements</span></span>



| <span data-ttu-id="13f53-142">需求</span><span class="sxs-lookup"><span data-stu-id="13f53-142">Requirement</span></span> | <span data-ttu-id="13f53-143">值</span><span class="sxs-lookup"><span data-stu-id="13f53-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="13f53-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13f53-144">Minimum supported client</span></span><br/> | <span data-ttu-id="13f53-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13f53-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="13f53-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13f53-146">Minimum supported server</span></span><br/> | <span data-ttu-id="13f53-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13f53-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="13f53-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="13f53-148">Namespace</span></span><br/>                | <span data-ttu-id="13f53-149">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="13f53-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="13f53-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13f53-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f53-151">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="13f53-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="13f53-152">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="13f53-152">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="13f53-153">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="13f53-153">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="13f53-154">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="13f53-154">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="13f53-155">建立命名空間安全性的繼承</span><span class="sxs-lookup"><span data-stu-id="13f53-155">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="13f53-156"> (Acl 的存取控制清單) </span><span class="sxs-lookup"><span data-stu-id="13f53-156">Access Control Lists (ACLs)</span></span>](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[<span data-ttu-id="13f53-157">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="13f53-157">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

