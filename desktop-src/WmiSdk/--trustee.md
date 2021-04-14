---
description: '\_ \_ 受信任的抽象系統類別代表信任者。 您可以使用 (位元組陣列的名稱或 SID) 。'
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: __Trustee 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
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
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514240"
---
# <a name="__trustee-class"></a><span data-ttu-id="ffd4d-104">\_\_信任類別</span><span class="sxs-lookup"><span data-stu-id="ffd4d-104">\_\_Trustee class</span></span>

<span data-ttu-id="ffd4d-105">[**\_ \_ 受信任**](--securitydescriptor.md)的抽象系統類別代表 [*信任者*](/windows/desktop/SecGloss/t-gly)。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-105">The [**\_\_Trustee**](--securitydescriptor.md) abstract system class represents a [*trustee*](/windows/desktop/SecGloss/t-gly).</span></span> <span data-ttu-id="ffd4d-106">您可以使用 (位元組陣列的名稱或 SID) 。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-106">Either a name or an SID (byte array) can be used.</span></span>

<span data-ttu-id="ffd4d-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ffd4d-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd4d-109">語法</span><span class="sxs-lookup"><span data-stu-id="ffd4d-109">Syntax</span></span>

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="ffd4d-110">成員</span><span class="sxs-lookup"><span data-stu-id="ffd4d-110">Members</span></span>

<span data-ttu-id="ffd4d-111">**\_ \_ 信任者** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ffd4d-111">The **\_\_Trustee** class has these types of members:</span></span>

-   [<span data-ttu-id="ffd4d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ffd4d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffd4d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ffd4d-113">Properties</span></span>

<span data-ttu-id="ffd4d-114">**\_ \_ 信任者** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-114">The **\_\_Trustee** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffd4d-115">**網域**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-115">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffd4d-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffd4d-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffd4d-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffd4d-118">帳戶的網域部分。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-118">Domain portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="ffd4d-119">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffd4d-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffd4d-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffd4d-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffd4d-122">帳戶的名稱部分。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-122">Name portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="ffd4d-123">**SID**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-123">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffd4d-124">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="ffd4d-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ffd4d-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffd4d-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffd4d-126">二進位位元組陣列形式之信任者的 SID。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-126">The SID of the trustee in the binary byte array form.</span></span>

</dd> <dt>

<span data-ttu-id="ffd4d-127">**SidLength**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-127">**SidLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffd4d-128">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffd4d-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffd4d-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffd4d-130">SID 的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-130">The length of the SID in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ffd4d-131">**SidString**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-131">**SidString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffd4d-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffd4d-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffd4d-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffd4d-134">具有字串格式之信任者的 SID，例如 "S-1-1-0"。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-134">The SID of the trustee in the string format, for example, "S-1-1-0".</span></span>

</dd> <dt>

<span data-ttu-id="ffd4d-135">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffd4d-136">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ffd4d-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ffd4d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffd4d-138">建立安全描述項時，採用 [CIM \_ DATETIME](cim-datetime.md) 格式的時間。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-138">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffd4d-139">備註</span><span class="sxs-lookup"><span data-stu-id="ffd4d-139">Remarks</span></span>

<span data-ttu-id="ffd4d-140">這個類別提供的屬性是由 [**win32 \_ 受信任**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 類別所繼承，這是 [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的成員。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-140">This class provides properties that are inherited by the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="ffd4d-141">如需詳細資訊，請參閱 [WMI 安全描述項物件](wmi-security-descriptor-objects.md) 和 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-141">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="ffd4d-142">如需 Ace 的詳細資訊，請參閱 [存取控制元件](/windows/desktop/SecAuthZ/access-control-components)。</span><span class="sxs-lookup"><span data-stu-id="ffd4d-142">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd4d-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffd4d-143">Requirements</span></span>



| <span data-ttu-id="ffd4d-144">需求</span><span class="sxs-lookup"><span data-stu-id="ffd4d-144">Requirement</span></span> | <span data-ttu-id="ffd4d-145">值</span><span class="sxs-lookup"><span data-stu-id="ffd4d-145">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ffd4d-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffd4d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd4d-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffd4d-147">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ffd4d-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffd4d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd4d-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffd4d-149">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ffd4d-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="ffd4d-150">Namespace</span></span><br/>                | <span data-ttu-id="ffd4d-151">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="ffd4d-151">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ffd4d-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffd4d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd4d-153">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="ffd4d-153">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="ffd4d-154">**Win32 \_ 信任者**</span><span class="sxs-lookup"><span data-stu-id="ffd4d-154">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[<span data-ttu-id="ffd4d-155">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="ffd4d-155">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

