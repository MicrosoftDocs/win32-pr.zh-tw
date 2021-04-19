---
description: 控制對不支援之 Windows 版本的遠端存取。
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: __NTLMUser9X 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000177"
---
# <a name="__ntlmuser9x-class"></a><span data-ttu-id="6c87f-103">\_\_NTLMUser9X 類別</span><span class="sxs-lookup"><span data-stu-id="6c87f-103">\_\_NTLMUser9X class</span></span>

<span data-ttu-id="6c87f-104">**\_ \_ NTLMUser9X** 系統類別可控制遠端存取不受支援的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="6c87f-104">The **\_\_NTLMUser9X** system class controls remote access to unsupported versions of Windows.</span></span> <span data-ttu-id="6c87f-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6c87f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6c87f-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="6c87f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c87f-107">語法</span><span class="sxs-lookup"><span data-stu-id="6c87f-107">Syntax</span></span>

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="6c87f-108">成員</span><span class="sxs-lookup"><span data-stu-id="6c87f-108">Members</span></span>

<span data-ttu-id="6c87f-109">**\_ \_ NTLMUser9X** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6c87f-109">The **\_\_NTLMUser9X** class has these types of members:</span></span>

-   [<span data-ttu-id="6c87f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6c87f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c87f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6c87f-111">Properties</span></span>

<span data-ttu-id="6c87f-112">**\_ \_ NTLMUser9X** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6c87f-112">The **\_\_NTLMUser9X** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c87f-113">**授權單位**</span><span class="sxs-lookup"><span data-stu-id="6c87f-113">**Authority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c87f-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c87f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c87f-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6c87f-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6c87f-116">要套用使用者名稱的網域。</span><span class="sxs-lookup"><span data-stu-id="6c87f-116">Domain to which a user name applies.</span></span>

</dd> <dt>

<span data-ttu-id="6c87f-117">**旗標**</span><span class="sxs-lookup"><span data-stu-id="6c87f-117">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c87f-118">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6c87f-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c87f-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6c87f-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6c87f-120">繼承旗標。</span><span class="sxs-lookup"><span data-stu-id="6c87f-120">Inheritance flags.</span></span>

<dt>

<span data-ttu-id="6c87f-121">0</span><span class="sxs-lookup"><span data-stu-id="6c87f-121">0</span></span>
</dt> <dd>

<span data-ttu-id="6c87f-122">無繼承。</span><span class="sxs-lookup"><span data-stu-id="6c87f-122">No inheritance.</span></span>

</dd> <dt>

<span data-ttu-id="6c87f-123">2</span><span class="sxs-lookup"><span data-stu-id="6c87f-123">2</span></span>
</dt> <dd>

<span data-ttu-id="6c87f-124">除了目前的命名空間之外，也會套用至子命名空間。</span><span class="sxs-lookup"><span data-stu-id="6c87f-124">Apply to child namespaces, in addition to the current one.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c87f-125">**Mask**</span><span class="sxs-lookup"><span data-stu-id="6c87f-125">**Mask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c87f-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6c87f-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c87f-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6c87f-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6c87f-128">位元遮罩，指定 Windows Management Instrumentation (WMI) 存放庫中命名空間的存取權限。</span><span class="sxs-lookup"><span data-stu-id="6c87f-128">Bitmask that specifies access rights to the namespace in the Windows Management Instrumentation (WMI) repository.</span></span> <span data-ttu-id="6c87f-129">如需位值，請參閱 [**命名空間存取權限常數**](namespace-access-rights-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="6c87f-129">For bit values, see [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c87f-130">**名稱**</span><span class="sxs-lookup"><span data-stu-id="6c87f-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c87f-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c87f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c87f-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6c87f-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6c87f-133">使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="6c87f-133">User name.</span></span>

</dd> <dt>

<span data-ttu-id="6c87f-134">**型別**</span><span class="sxs-lookup"><span data-stu-id="6c87f-134">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c87f-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="6c87f-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c87f-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6c87f-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6c87f-137">允許存取。</span><span class="sxs-lookup"><span data-stu-id="6c87f-137">Access allowed.</span></span>

<dt>

<span data-ttu-id="6c87f-138">0</span><span class="sxs-lookup"><span data-stu-id="6c87f-138">0</span></span>
</dt> <dd>

<span data-ttu-id="6c87f-139">允許存取。</span><span class="sxs-lookup"><span data-stu-id="6c87f-139">Access allowed.</span></span>

</dd> <dt>

<span data-ttu-id="6c87f-140">2</span><span class="sxs-lookup"><span data-stu-id="6c87f-140">2</span></span>
</dt> <dd>

<span data-ttu-id="6c87f-141">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="6c87f-141">Access denied.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c87f-142">備註</span><span class="sxs-lookup"><span data-stu-id="6c87f-142">Remarks</span></span>

<span data-ttu-id="6c87f-143">**\_ \_ NTLMUser9X** 類別用來做為 [**\_ \_ SystemSecurity：： Get9XUserList**](--systemsecurity-get9xuserlist.md)和 [**\_ \_ SystemSecurity：： Set9XUserList**](--systemsecurity-set9xuserlist.md)方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="6c87f-143">The **\_\_NTLMUser9X** class is used as an input parameter for the [**\_\_SystemSecurity::Get9XUserList**](--systemsecurity-get9xuserlist.md) and [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c87f-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c87f-144">Requirements</span></span>



| <span data-ttu-id="6c87f-145">需求</span><span class="sxs-lookup"><span data-stu-id="6c87f-145">Requirement</span></span> | <span data-ttu-id="6c87f-146">值</span><span class="sxs-lookup"><span data-stu-id="6c87f-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6c87f-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c87f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6c87f-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c87f-148">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6c87f-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c87f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6c87f-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c87f-150">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6c87f-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="6c87f-151">Namespace</span></span><br/>                | <span data-ttu-id="6c87f-152">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="6c87f-152">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6c87f-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c87f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c87f-154">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="6c87f-154">**\_\_SecurityRelatedClass**</span></span>](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[<span data-ttu-id="6c87f-155">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="6c87f-155">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="6c87f-156">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="6c87f-156">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

