---
description: 表示存取控制項目 (ACE)。
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: __ACE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469464"
---
# <a name="__ace-class"></a><span data-ttu-id="829eb-103">\_\_ACE 類別</span><span class="sxs-lookup"><span data-stu-id="829eb-103">\_\_ACE class</span></span>

<span data-ttu-id="829eb-104">**\_ \_ Ace** 抽象系統類別代表 ([*ACE*](/windows/desktop/SecGloss/a-gly)) 的存取控制專案。</span><span class="sxs-lookup"><span data-stu-id="829eb-104">The **\_\_ACE** abstract system class represents an access control entry ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span></span>

<span data-ttu-id="829eb-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="829eb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="829eb-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="829eb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="829eb-107">語法</span><span class="sxs-lookup"><span data-stu-id="829eb-107">Syntax</span></span>

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a><span data-ttu-id="829eb-108">成員</span><span class="sxs-lookup"><span data-stu-id="829eb-108">Members</span></span>

<span data-ttu-id="829eb-109">**\_ \_ ACE** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="829eb-109">The **\_\_ACE** class has these types of members:</span></span>

-   [<span data-ttu-id="829eb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="829eb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="829eb-111">屬性</span><span class="sxs-lookup"><span data-stu-id="829eb-111">Properties</span></span>

<span data-ttu-id="829eb-112">**\_ \_ ACE** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="829eb-112">The **\_\_ACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="829eb-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="829eb-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="829eb-114">資料類型:</span><span class="sxs-lookup"><span data-stu-id="829eb-114">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="829eb-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="829eb-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="829eb-116">代表授與或拒絕信任者之許可權的位旗標。</span><span class="sxs-lookup"><span data-stu-id="829eb-116">Bit flags representing rights that are granted or denied to the trustee.</span></span> <span data-ttu-id="829eb-117">如需詳細資訊和旗標的描述，請參閱 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)類別中的 **AccessMask** 屬性。</span><span class="sxs-lookup"><span data-stu-id="829eb-117">For more information and a description of the flags, see **AccessMask** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="829eb-118">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="829eb-118">**AceFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="829eb-119">資料類型:</span><span class="sxs-lookup"><span data-stu-id="829eb-119">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="829eb-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="829eb-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="829eb-121">指定 ACE 繼承的位旗標。</span><span class="sxs-lookup"><span data-stu-id="829eb-121">Bit flags specifying the inheritance of the ACE.</span></span> <span data-ttu-id="829eb-122">如需詳細資訊和旗標的描述，請參閱 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)類別中的 **AceFlags** 屬性。</span><span class="sxs-lookup"><span data-stu-id="829eb-122">For more information and a description of the flags, see **AceFlags** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="829eb-123">**AceType**</span><span class="sxs-lookup"><span data-stu-id="829eb-123">**AceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="829eb-124">資料類型:</span><span class="sxs-lookup"><span data-stu-id="829eb-124">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="829eb-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="829eb-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="829eb-126">此實例所表示之 ACE 專案的型別。</span><span class="sxs-lookup"><span data-stu-id="829eb-126">The type of ACE entry that this instance represents.</span></span>

</dd> <dt>

<span data-ttu-id="829eb-127">**GuidInheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="829eb-127">**GuidInheritedObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="829eb-128">資料類型:</span><span class="sxs-lookup"><span data-stu-id="829eb-128">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="829eb-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="829eb-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="829eb-130">**AccessMask** 屬性中的存取權限所套用之物件父系的 GUID。</span><span class="sxs-lookup"><span data-stu-id="829eb-130">The GUID of the parent of the object to which the access rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="829eb-131">**GuidObjectType**</span><span class="sxs-lookup"><span data-stu-id="829eb-131">**GuidObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="829eb-132">資料類型:</span><span class="sxs-lookup"><span data-stu-id="829eb-132">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="829eb-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="829eb-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="829eb-134">GUID，指出 **AccessMask** 屬性中的許可權所套用的物件類型。</span><span class="sxs-lookup"><span data-stu-id="829eb-134">The GUID that indicates the type of object to which the rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="829eb-135">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="829eb-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="829eb-136">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="829eb-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="829eb-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="829eb-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="829eb-138">建立安全描述項時，採用 [CIM \_ 日期](cim-datetime.md) 時間格式的時間。</span><span class="sxs-lookup"><span data-stu-id="829eb-138">The time, in the [CIM\_DATETIME](cim-datetime.md) format, when the security descriptor was created.</span></span>

</dd> <dt>

<span data-ttu-id="829eb-139">**受託 人**</span><span class="sxs-lookup"><span data-stu-id="829eb-139">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="829eb-140">資料類型： **[ **\_ \_ 信任者**](--trustee.md)**</span><span class="sxs-lookup"><span data-stu-id="829eb-140">Data type: **[**\_\_Trustee**](--trustee.md)**</span></span>
</dt> <dt>

<span data-ttu-id="829eb-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="829eb-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="829eb-142">Ace 類別的這個實例所表示之 ace 專案的信任 **\_ \_** 者。</span><span class="sxs-lookup"><span data-stu-id="829eb-142">The trustee of the ACE entry represented by this instance of the **\_\_ACE** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="829eb-143">備註</span><span class="sxs-lookup"><span data-stu-id="829eb-143">Remarks</span></span>

<span data-ttu-id="829eb-144">這個類別會提供 [**win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 類別所繼承的屬性，該類別是 [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的成員。</span><span class="sxs-lookup"><span data-stu-id="829eb-144">This class provides the properties that are inherited by the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="829eb-145">如需詳細資訊，請參閱 [WMI 安全描述項物件](wmi-security-descriptor-objects.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="829eb-145">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="829eb-146">如需 Ace 的詳細資訊，請參閱 [存取控制元件](/windows/desktop/SecAuthZ/access-control-components)。</span><span class="sxs-lookup"><span data-stu-id="829eb-146">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="829eb-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="829eb-147">Requirements</span></span>



| <span data-ttu-id="829eb-148">需求</span><span class="sxs-lookup"><span data-stu-id="829eb-148">Requirement</span></span> | <span data-ttu-id="829eb-149">值</span><span class="sxs-lookup"><span data-stu-id="829eb-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="829eb-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="829eb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="829eb-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="829eb-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="829eb-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="829eb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="829eb-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="829eb-153">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="829eb-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="829eb-154">Namespace</span></span><br/>                | <span data-ttu-id="829eb-155">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="829eb-155">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="829eb-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="829eb-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829eb-157">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="829eb-157">**\_\_SecurityRelatedClass**</span></span>](--securityrelatedclass.md)
</dt> <dt>

[<span data-ttu-id="829eb-158">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="829eb-158">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="829eb-159">**Win32 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="829eb-159">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="829eb-160">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="829eb-160">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

