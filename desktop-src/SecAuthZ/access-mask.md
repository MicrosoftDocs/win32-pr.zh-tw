---
description: 定義標準、特定和一般許可權。 這些許可權用於 (Ace 的存取控制專案) ，而且是指定要求或授與物件之存取權的主要方式。
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: 'ACCESS_MASK (Winnt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115333"
---
# <a name="access_mask"></a><span data-ttu-id="63e91-104">存取 \_ 遮罩</span><span class="sxs-lookup"><span data-stu-id="63e91-104">ACCESS\_MASK</span></span>

<span data-ttu-id="63e91-105">**存取 \_ 遮罩** 資料類型是一種 **DWORD** 值，可定義標準、特定和一般許可權。</span><span class="sxs-lookup"><span data-stu-id="63e91-105">The **ACCESS\_MASK** data type is a **DWORD** value that defines standard, specific, and generic rights.</span></span> <span data-ttu-id="63e91-106">這些許可權用於 (Ace 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)) ，而且是指定要求或授與物件之存取權的主要方式。</span><span class="sxs-lookup"><span data-stu-id="63e91-106">These rights are used in [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and are the primary means of specifying the requested or granted access to an object.</span></span>


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a><span data-ttu-id="63e91-107">備註</span><span class="sxs-lookup"><span data-stu-id="63e91-107">Remarks</span></span>

<span data-ttu-id="63e91-108">此值的位配置如下。</span><span class="sxs-lookup"><span data-stu-id="63e91-108">The bits in this value are allocated as follows.</span></span>



| <span data-ttu-id="63e91-109">Bits</span><span class="sxs-lookup"><span data-stu-id="63e91-109">Bits</span></span>             | <span data-ttu-id="63e91-110">意義</span><span class="sxs-lookup"><span data-stu-id="63e91-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e91-111">0 15</span><span class="sxs-lookup"><span data-stu-id="63e91-111">0 15</span></span><br/>  | <span data-ttu-id="63e91-112">特定權利。</span><span class="sxs-lookup"><span data-stu-id="63e91-112">Specific rights.</span></span> <span data-ttu-id="63e91-113">包含與遮罩相關聯之物件類型的特定存取遮罩。</span><span class="sxs-lookup"><span data-stu-id="63e91-113">Contains the access mask specific to the object type associated with the mask.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="63e91-114">16 23</span><span class="sxs-lookup"><span data-stu-id="63e91-114">16 23</span></span><br/> | <span data-ttu-id="63e91-115">標準權利。</span><span class="sxs-lookup"><span data-stu-id="63e91-115">Standard rights.</span></span> <span data-ttu-id="63e91-116">包含物件的標準存取權限。</span><span class="sxs-lookup"><span data-stu-id="63e91-116">Contains the object's standard access rights.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="63e91-117">24</span><span class="sxs-lookup"><span data-stu-id="63e91-117">24</span></span><br/>    | <span data-ttu-id="63e91-118">存取系統安全性 (**存取 \_ 系統 \_ 安全性**) 。</span><span class="sxs-lookup"><span data-stu-id="63e91-118">Access system security (**ACCESS\_SYSTEM\_SECURITY**).</span></span> <span data-ttu-id="63e91-119">它是用來指出 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) 存取權。</span><span class="sxs-lookup"><span data-stu-id="63e91-119">It is used to indicate access to a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="63e91-120">這種類型的存取需要呼叫進程擁有 **SE \_ 安全性 \_ 名稱** (管理審核和安全性記錄) 許可權。</span><span class="sxs-lookup"><span data-stu-id="63e91-120">This type of access requires the calling process to have the **SE\_SECURITY\_NAME** (Manage auditing and security log) privilege.</span></span> <span data-ttu-id="63e91-121">如果在 audit access ACE 的存取遮罩中設定這個旗標 (成功或失敗的存取) ，則會審核 SACL 存取。</span><span class="sxs-lookup"><span data-stu-id="63e91-121">If this flag is set in the access mask of an audit access ACE (successful or unsuccessful access), the SACL access will be audited.</span></span><br/> |
| <span data-ttu-id="63e91-122">25</span><span class="sxs-lookup"><span data-stu-id="63e91-122">25</span></span><br/>    | <span data-ttu-id="63e91-123">允許的最 **大 \_ ()** 。</span><span class="sxs-lookup"><span data-stu-id="63e91-123">Maximum allowed (**MAXIMUM\_ALLOWED**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="63e91-124">26 27</span><span class="sxs-lookup"><span data-stu-id="63e91-124">26 27</span></span><br/> | <span data-ttu-id="63e91-125">保留的。</span><span class="sxs-lookup"><span data-stu-id="63e91-125">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="63e91-126">28</span><span class="sxs-lookup"><span data-stu-id="63e91-126">28</span></span><br/>    | <span data-ttu-id="63e91-127">泛型所有 (**一般 \_ 都** 是) 。</span><span class="sxs-lookup"><span data-stu-id="63e91-127">Generic all (**GENERIC\_ALL**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="63e91-128">29</span><span class="sxs-lookup"><span data-stu-id="63e91-128">29</span></span><br/>    | <span data-ttu-id="63e91-129">一般執行 (**一般 \_ 執行**) 。</span><span class="sxs-lookup"><span data-stu-id="63e91-129">Generic execute (**GENERIC\_EXECUTE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="63e91-130">30</span><span class="sxs-lookup"><span data-stu-id="63e91-130">30</span></span><br/>    | <span data-ttu-id="63e91-131">一般寫入 (**一般 \_ 寫入**) 。</span><span class="sxs-lookup"><span data-stu-id="63e91-131">Generic write (**GENERIC\_WRITE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="63e91-132">31</span><span class="sxs-lookup"><span data-stu-id="63e91-132">31</span></span><br/>    | <span data-ttu-id="63e91-133">泛型讀取 (**一般 \_ 讀取**) 。</span><span class="sxs-lookup"><span data-stu-id="63e91-133">Generic read (**GENERIC\_READ**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="63e91-134">標準許可權位（16到23）包含物件的標準存取權限，而且可以是下列預先定義旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="63e91-134">Standard rights bits, 16 to 23, contain the object's standard access rights and can be a combination of the following predefined flags.</span></span>



| <span data-ttu-id="63e91-135">bit</span><span class="sxs-lookup"><span data-stu-id="63e91-135">Bit</span></span>           | <span data-ttu-id="63e91-136">旗標</span><span class="sxs-lookup"><span data-stu-id="63e91-136">Flag</span></span>                         | <span data-ttu-id="63e91-137">意義</span><span class="sxs-lookup"><span data-stu-id="63e91-137">Meaning</span></span>                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e91-138">16</span><span class="sxs-lookup"><span data-stu-id="63e91-138">16</span></span><br/> | <span data-ttu-id="63e91-139">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="63e91-139">**DELETE**</span></span><br/>        | <span data-ttu-id="63e91-140">刪除存取權。</span><span class="sxs-lookup"><span data-stu-id="63e91-140">Delete access.</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="63e91-141">17</span><span class="sxs-lookup"><span data-stu-id="63e91-141">17</span></span><br/> | <span data-ttu-id="63e91-142">**讀取 \_ 控制**</span><span class="sxs-lookup"><span data-stu-id="63e91-142">**READ\_CONTROL**</span></span><br/> | <span data-ttu-id="63e91-143">擁有者、群組和 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 的讀取權限 (DACL) 的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="63e91-143">Read access to the owner, group, and [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the security descriptor.</span></span><br/> |
| <span data-ttu-id="63e91-144">18</span><span class="sxs-lookup"><span data-stu-id="63e91-144">18</span></span><br/> | <span data-ttu-id="63e91-145">**寫入 \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="63e91-145">**WRITE\_DAC**</span></span><br/>    | <span data-ttu-id="63e91-146">DACL 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="63e91-146">Write access to the DACL.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="63e91-147">19</span><span class="sxs-lookup"><span data-stu-id="63e91-147">19</span></span><br/> | <span data-ttu-id="63e91-148">**寫入 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="63e91-148">**WRITE\_OWNER**</span></span><br/>  | <span data-ttu-id="63e91-149">擁有者的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="63e91-149">Write access to owner.</span></span><br/>                                                                                                                                                                                                        |
| <span data-ttu-id="63e91-150">20</span><span class="sxs-lookup"><span data-stu-id="63e91-150">20</span></span><br/> | <span data-ttu-id="63e91-151">**同步**</span><span class="sxs-lookup"><span data-stu-id="63e91-151">**SYNCHRONIZE**</span></span><br/>   | <span data-ttu-id="63e91-152">同步存取。</span><span class="sxs-lookup"><span data-stu-id="63e91-152">Synchronize access.</span></span><br/>                                                                                                                                                                                                           |



 

<span data-ttu-id="63e91-153">在 Winnt 中定義的下列常數表示特定和標準存取權限。</span><span class="sxs-lookup"><span data-stu-id="63e91-153">The following constants defined in Winnt.h represent the specific and standard access rights.</span></span>


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a><span data-ttu-id="63e91-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="63e91-154">Requirements</span></span>



| <span data-ttu-id="63e91-155">需求</span><span class="sxs-lookup"><span data-stu-id="63e91-155">Requirement</span></span> | <span data-ttu-id="63e91-156">值</span><span class="sxs-lookup"><span data-stu-id="63e91-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e91-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63e91-157">Minimum supported client</span></span><br/> | <span data-ttu-id="63e91-158">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63e91-158">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="63e91-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63e91-159">Minimum supported server</span></span><br/> | <span data-ttu-id="63e91-160">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63e91-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="63e91-161">標頭</span><span class="sxs-lookup"><span data-stu-id="63e91-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="63e91-162"><dt>Winnt (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="63e91-162"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e91-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63e91-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e91-164">存取控制</span><span class="sxs-lookup"><span data-stu-id="63e91-164">Access Control</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="63e91-165">基本存取控制結構</span><span class="sxs-lookup"><span data-stu-id="63e91-165">Basic Access Control Structures</span></span>](authorization-structures.md)
</dt> <dt>

[<span data-ttu-id="63e91-166">存取權限和存取遮罩</span><span class="sxs-lookup"><span data-stu-id="63e91-166">Access Rights and Access Masks</span></span>](access-rights-and-access-masks.md)
</dt> <dt>

[<span data-ttu-id="63e91-167">**泛型 \_ 對應**</span><span class="sxs-lookup"><span data-stu-id="63e91-167">**GENERIC\_MAPPING**</span></span>](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

