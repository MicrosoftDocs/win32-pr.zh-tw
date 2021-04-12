---
description: 代表安全性描述元。
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: __SecurityDescriptor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193066"
---
# <a name="__securitydescriptor-class"></a><span data-ttu-id="6522b-103">\_\_SecurityDescriptor 類別</span><span class="sxs-lookup"><span data-stu-id="6522b-103">\_\_SecurityDescriptor class</span></span>

<span data-ttu-id="6522b-104">**\_ \_ SecurityDescriptor** 抽象系統類別代表 [*安全描述項*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="6522b-104">The **\_\_SecurityDescriptor** abstract system class represents a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="6522b-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6522b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6522b-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="6522b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6522b-107">語法</span><span class="sxs-lookup"><span data-stu-id="6522b-107">Syntax</span></span>

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="6522b-108">成員</span><span class="sxs-lookup"><span data-stu-id="6522b-108">Members</span></span>

<span data-ttu-id="6522b-109">**\_ \_ SecurityDescriptor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6522b-109">The **\_\_SecurityDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="6522b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6522b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6522b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6522b-111">Properties</span></span>

<span data-ttu-id="6522b-112">**\_ \_ SecurityDescriptor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6522b-112">The **\_\_SecurityDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6522b-113">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="6522b-113">**ControlFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6522b-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6522b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6522b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6522b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6522b-116">提供描述項內容和格式相關資訊的位旗標。</span><span class="sxs-lookup"><span data-stu-id="6522b-116">Bit flags that provide information about the descriptor's contents and format.</span></span> <span data-ttu-id="6522b-117">如需旗標的描述，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)類別中的 **ControlFlags** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6522b-117">See the **ControlFlags** property in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class for a description of the flags.</span></span>

</dd> <dt>

<span data-ttu-id="6522b-118">**Dacl**</span><span class="sxs-lookup"><span data-stu-id="6522b-118">**DACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6522b-119">資料類型： **[**\_ \_ ACE**](--ace.md)** 陣列</span><span class="sxs-lookup"><span data-stu-id="6522b-119">Data type: **[**\_\_ACE**](--ace.md)** array</span></span>
</dt> <dt>

<span data-ttu-id="6522b-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6522b-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6522b-121">指定物件存取權之 [**\_ \_ ACE**](--ace.md)專案的陣列。</span><span class="sxs-lookup"><span data-stu-id="6522b-121">An array of [**\_\_ACE**](--ace.md) entries that specify access to the object.</span></span>

</dd> <dt>

<span data-ttu-id="6522b-122">**群組**</span><span class="sxs-lookup"><span data-stu-id="6522b-122">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6522b-123">資料類型： **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="6522b-123">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6522b-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6522b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6522b-125">識別代表物件群組之信任者的 ACE。</span><span class="sxs-lookup"><span data-stu-id="6522b-125">ACE that identifies the trustee representing the group of the object.</span></span>

</dd> <dt>

<span data-ttu-id="6522b-126">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="6522b-126">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6522b-127">資料類型： **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="6522b-127">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6522b-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6522b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6522b-129">識別代表物件擁有者之信任者的 ACE。</span><span class="sxs-lookup"><span data-stu-id="6522b-129">ACE that identifies the trustee representing the owner of the object.</span></span>

</dd> <dt>

<span data-ttu-id="6522b-130">**SACL**</span><span class="sxs-lookup"><span data-stu-id="6522b-130">**SACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6522b-131">資料類型： **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="6522b-131">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6522b-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6522b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6522b-133">[**\_ \_ ACE**](--ace.md)專案的陣列，可識別所收集之審核資訊的使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="6522b-133">An array of [**\_\_ACE**](--ace.md) entries that identifies users and groups for which auditing information is gathered.</span></span>

</dd> <dt>

<span data-ttu-id="6522b-134">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="6522b-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6522b-135">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="6522b-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6522b-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6522b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6522b-137">建立安全描述項時，採用 [CIM \_ DATETIME](cim-datetime.md) 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="6522b-137">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6522b-138">備註</span><span class="sxs-lookup"><span data-stu-id="6522b-138">Remarks</span></span>

<span data-ttu-id="6522b-139">此類別提供 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)所繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6522b-139">This class provides properties inherited by [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="6522b-140">如需詳細資訊，請參閱 [WMI 安全描述項物件](wmi-security-descriptor-objects.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="6522b-140">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="6522b-141">如需 Ace 的詳細資訊，請參閱 [存取控制元件](/windows/desktop/SecAuthZ/access-control-components)。</span><span class="sxs-lookup"><span data-stu-id="6522b-141">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="6522b-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="6522b-142">Requirements</span></span>



| <span data-ttu-id="6522b-143">需求</span><span class="sxs-lookup"><span data-stu-id="6522b-143">Requirement</span></span> | <span data-ttu-id="6522b-144">值</span><span class="sxs-lookup"><span data-stu-id="6522b-144">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6522b-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6522b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6522b-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6522b-146">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6522b-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6522b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6522b-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6522b-148">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6522b-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="6522b-149">Namespace</span></span><br/>                | <span data-ttu-id="6522b-150">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="6522b-150">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6522b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6522b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6522b-152">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="6522b-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="6522b-153">**Win32 \_ SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="6522b-153">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="6522b-154">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="6522b-154">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

