---
description: 描述 Winerror.h .h 標頭檔中定義的錯誤碼8200-8999，適用于開發人員。
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: '系統錯誤碼 (8200-8999)  (Winerror.h. h) '
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187727"
---
# <a name="system-error-codes-8200-8999"></a><span data-ttu-id="790c2-103">系統錯誤碼 (8200-8999) </span><span class="sxs-lookup"><span data-stu-id="790c2-103">System Error Codes (8200-8999)</span></span>

> [!NOTE]
> <span data-ttu-id="790c2-104">這項資訊適用于程式設計人員偵測系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="790c2-105">針對其他錯誤（例如 Windows Update 的問題），[ [錯誤碼](system-error-codes.md) ] 頁面上有資源清單。</span><span class="sxs-lookup"><span data-stu-id="790c2-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="790c2-106">下列清單描述錯誤8200到8999的 [系統錯誤碼](system-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="790c2-106">The following list describes [system error codes](system-error-codes.md) for errors 8200 to 8999.</span></span> <span data-ttu-id="790c2-107">當有許多函式失敗時， [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回這些函數。</span><span class="sxs-lookup"><span data-stu-id="790c2-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="790c2-108">若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式，並搭配系統旗標的 **格式 \_ 訊息 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="790c2-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="790c2-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**\_ \_ 未安裝錯誤 \_ DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR\_DS\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-110">8200 (0x2008) </span><span class="sxs-lookup"><span data-stu-id="790c2-110">8200 (0x2008)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-111">安裝目錄服務時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-111">An error occurred while installing the directory service.</span></span> <span data-ttu-id="790c2-112">如需詳細資訊，請參閱事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="790c2-112">For more information, see the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**在 \_ \_ 本機評估 DS 成員資格的 \_ 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR\_DS\_MEMBERSHIP\_EVALUATED\_LOCALLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-114">8201 (0x2009) </span><span class="sxs-lookup"><span data-stu-id="790c2-114">8201 (0x2009)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-115">目錄服務會在本機評估群組成員資格。</span><span class="sxs-lookup"><span data-stu-id="790c2-115">The directory service evaluated group memberships locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**錯誤 \_ DS \_ 沒有 \_ 屬性 \_ 或 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="790c2-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR\_DS\_NO\_ATTRIBUTE\_OR\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-117">8202 (0x200A) </span><span class="sxs-lookup"><span data-stu-id="790c2-117">8202 (0x200A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-118">指定的目錄服務屬性或值不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-118">The specified directory service attribute or value does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**錯誤 \_ DS \_ 不正確 \_ 屬性 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="790c2-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR\_DS\_INVALID\_ATTRIBUTE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-120">8203 (0x200B) </span><span class="sxs-lookup"><span data-stu-id="790c2-120">8203 (0x200B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-121">指定給目錄服務的屬性語法無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-121">The attribute syntax specified to the directory service is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**錯誤 \_ DS \_ 屬性 \_ 類型 \_ 未定義**</span><span class="sxs-lookup"><span data-stu-id="790c2-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR\_DS\_ATTRIBUTE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-123">8204 (0x200C) </span><span class="sxs-lookup"><span data-stu-id="790c2-123">8204 (0x200C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-124">未定義指定給目錄服務的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="790c2-124">The attribute type specified to the directory service is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**\_DS \_ 屬性 \_ 或 \_ 值 \_ 存在時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR\_DS\_ATTRIBUTE\_OR\_VALUE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-126">8205 (0x200D) </span><span class="sxs-lookup"><span data-stu-id="790c2-126">8205 (0x200D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-127">指定的目錄服務屬性或值已經存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-127">The specified directory service attribute or value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**\_DS \_ 忙碌時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR\_DS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-129">8206 (0x200E) </span><span class="sxs-lookup"><span data-stu-id="790c2-129">8206 (0x200E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-130">目錄服務忙碌中。</span><span class="sxs-lookup"><span data-stu-id="790c2-130">The directory service is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**\_ \_ 無法使用錯誤 DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-132">8207 (0x200F) </span><span class="sxs-lookup"><span data-stu-id="790c2-132">8207 (0x200F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-133">目錄服務無法使用。</span><span class="sxs-lookup"><span data-stu-id="790c2-133">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**錯誤 \_ DS \_ 未配置 \_ RID \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR\_DS\_NO\_RIDS\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-135">8208 (0x2010) </span><span class="sxs-lookup"><span data-stu-id="790c2-135">8208 (0x2010)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-136">目錄服務無法配置相關的識別碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-136">The directory service was unable to allocate a relative identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**錯誤 \_ DS \_ 不再 \_ 有 \_ RID**</span><span class="sxs-lookup"><span data-stu-id="790c2-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR\_DS\_NO\_MORE\_RIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-138">8209 (0x2011) </span><span class="sxs-lookup"><span data-stu-id="790c2-138">8209 (0x2011)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-139">目錄服務已用盡相對識別碼的集區。</span><span class="sxs-lookup"><span data-stu-id="790c2-139">The directory service has exhausted the pool of relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**錯誤 \_ DS 錯誤的 \_ \_ 角色 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="790c2-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR\_DS\_INCORRECT\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-141">8210 (0x2012) </span><span class="sxs-lookup"><span data-stu-id="790c2-141">8210 (0x2012)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-142">無法執行要求的作業，因為目錄服務不是該類型作業的主要。</span><span class="sxs-lookup"><span data-stu-id="790c2-142">The requested operation could not be performed because the directory service is not the master for that type of operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**錯誤 \_ DS \_ RIDMGR \_ 初始化 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERROR\_DS\_RIDMGR\_INIT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-144">8211 (0x2013) </span><span class="sxs-lookup"><span data-stu-id="790c2-144">8211 (0x2013)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-145">目錄服務無法初始化配置相對識別碼的子系統。</span><span class="sxs-lookup"><span data-stu-id="790c2-145">The directory service was unable to initialize the subsystem that allocates relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**\_DS \_ OBJ \_ 類別 \_ 違規錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR\_DS\_OBJ\_CLASS\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-147">8212 (0x2014) </span><span class="sxs-lookup"><span data-stu-id="790c2-147">8212 (0x2014)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-148">要求的作業無法滿足一或多個與物件類別相關聯的條件約束。</span><span class="sxs-lookup"><span data-stu-id="790c2-148">The requested operation did not satisfy one or more constraints associated with the class of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**\_ \_ \_ 無法在非分 \_ \_ 葉上進行錯誤 DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR\_DS\_CANT\_ON\_NON\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-150">8213 (0x2015) </span><span class="sxs-lookup"><span data-stu-id="790c2-150">8213 (0x2015)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-151">目錄服務只能對分葉物件執行要求的操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-151">The directory service can perform the requested operation only on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**錯誤 \_ DS \_ 無法 \_ 在 \_ RDN 上進行**</span><span class="sxs-lookup"><span data-stu-id="790c2-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR\_DS\_CANT\_ON\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-153">8214 (0x2016) </span><span class="sxs-lookup"><span data-stu-id="790c2-153">8214 (0x2016)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-154">目錄服務無法在物件的 RDN 屬性上執行要求的作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-154">The directory service cannot perform the requested operation on the RDN attribute of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**錯誤 \_ DS \_ 無法 \_ MOD \_ OBJ \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="790c2-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR\_DS\_CANT\_MOD\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-156">8215 (0x2017) </span><span class="sxs-lookup"><span data-stu-id="790c2-156">8215 (0x2017)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-157">目錄服務偵測到嘗試修改物件的物件類別。</span><span class="sxs-lookup"><span data-stu-id="790c2-157">The directory service detected an attempt to modify the object class of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**錯誤 \_ DS \_ 跨 \_ DOM \_ 移動 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**ERROR\_DS\_CROSS\_DOM\_MOVE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-159">8216 (0x2018) </span><span class="sxs-lookup"><span data-stu-id="790c2-159">8216 (0x2018)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-160">無法執行要求的跨網域移動操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-160">The requested cross-domain move operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**錯誤 \_ DS \_ GC \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="790c2-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR\_DS\_GC\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-162">8217 (0x2019) </span><span class="sxs-lookup"><span data-stu-id="790c2-162">8217 (0x2019)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-163">無法連絡通用類別目錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="790c2-163">Unable to contact the global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**錯誤 \_ 共用 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="790c2-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERROR\_SHARED\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-165">8218 (0x201A) </span><span class="sxs-lookup"><span data-stu-id="790c2-165">8218 (0x201A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-166">原則物件是共用的，只能在根修改。</span><span class="sxs-lookup"><span data-stu-id="790c2-166">The policy object is shared and can only be modified at the root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**\_ \_ \_ \_ 找不到錯誤原則物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**ERROR\_POLICY\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-168">8219 (0x201B) </span><span class="sxs-lookup"><span data-stu-id="790c2-168">8219 (0x201B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-169">原則物件不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-169">The policy object does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_ \_ 只有 \_ DS 中的錯誤原則 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**ERROR\_POLICY\_ONLY\_IN\_DS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-171">8220 (0x201C) </span><span class="sxs-lookup"><span data-stu-id="790c2-171">8220 (0x201C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-172">要求的原則資訊只會在目錄服務中。</span><span class="sxs-lookup"><span data-stu-id="790c2-172">The requested policy information is only in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**使用中的錯誤 \_ 提升 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**ERROR\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-174">8221 (0x201D) </span><span class="sxs-lookup"><span data-stu-id="790c2-174">8221 (0x201D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-175">網域控制站升級目前為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="790c2-175">A domain controller promotion is currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**錯誤 \_ 沒有任何 \_ 促銷 \_ 活動**</span><span class="sxs-lookup"><span data-stu-id="790c2-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR\_NO\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-177">8222 (0x201E) </span><span class="sxs-lookup"><span data-stu-id="790c2-177">8222 (0x201E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-178">網域控制站升級目前未啟用。</span><span class="sxs-lookup"><span data-stu-id="790c2-178">A domain controller promotion is not currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**錯誤 \_ DS \_ 作業 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**ERROR\_DS\_OPERATIONS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-180">8224 (0x2020) </span><span class="sxs-lookup"><span data-stu-id="790c2-180">8224 (0x2020)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-181">發生作業錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-181">An operations error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**錯誤 \_ DS \_ 通訊協定 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**ERROR\_DS\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-183">8225 (0x2021) </span><span class="sxs-lookup"><span data-stu-id="790c2-183">8225 (0x2021)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-184">發生了通訊協定錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-184">A protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**\_超過錯誤 DS \_ TIMELIMIT \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR\_DS\_TIMELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-186">8226 (0x2022) </span><span class="sxs-lookup"><span data-stu-id="790c2-186">8226 (0x2022)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-187">超過此要求的時間限制。</span><span class="sxs-lookup"><span data-stu-id="790c2-187">The time limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**\_超過錯誤 DS \_ SIZELIMIT \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR\_DS\_SIZELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-189">8227 (0x2023) </span><span class="sxs-lookup"><span data-stu-id="790c2-189">8227 (0x2023)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-190">超過此要求的大小限制。</span><span class="sxs-lookup"><span data-stu-id="790c2-190">The size limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**\_超過 DS 系統 \_ 管理員 \_ 限制 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERROR\_DS\_ADMIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-192">8228 (0x2024) </span><span class="sxs-lookup"><span data-stu-id="790c2-192">8228 (0x2024)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-193">超過此要求的管理限制。</span><span class="sxs-lookup"><span data-stu-id="790c2-193">The administrative limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**錯誤 \_ DS \_ 比較 \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="790c2-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR\_DS\_COMPARE\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-195">8229 (0x2025) </span><span class="sxs-lookup"><span data-stu-id="790c2-195">8229 (0x2025)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-196">比較回應為 false。</span><span class="sxs-lookup"><span data-stu-id="790c2-196">The compare response was false.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**錯誤 \_ DS \_ 比較 \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="790c2-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR\_DS\_COMPARE\_TRUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-198">8230 (0x2026) </span><span class="sxs-lookup"><span data-stu-id="790c2-198">8230 (0x2026)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-199">比較回應為 true。</span><span class="sxs-lookup"><span data-stu-id="790c2-199">The compare response was true.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**\_ \_ \_ \_ 不支援錯誤 DS 驗證 \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="790c2-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERROR\_DS\_AUTH\_METHOD\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-201">8231 (0x2027) </span><span class="sxs-lookup"><span data-stu-id="790c2-201">8231 (0x2027)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-202">伺服器不支援要求的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="790c2-202">The requested authentication method is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**\_需要 DS \_ 強 \_ 身份驗證 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR\_DS\_STRONG\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-204">8232 (0x2028) </span><span class="sxs-lookup"><span data-stu-id="790c2-204">8232 (0x2028)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-205">此伺服器需要更安全的驗證方法。</span><span class="sxs-lookup"><span data-stu-id="790c2-205">A more secure authentication method is required for this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**錯誤 \_ DS \_ 不當 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="790c2-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR\_DS\_INAPPROPRIATE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-207">8233 (0x2029) </span><span class="sxs-lookup"><span data-stu-id="790c2-207">8233 (0x2029)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-208">不適當的驗證。</span><span class="sxs-lookup"><span data-stu-id="790c2-208">Inappropriate authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**錯誤 \_ DS \_ 驗證 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="790c2-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR\_DS\_AUTH\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-210">8234 (0x202A) </span><span class="sxs-lookup"><span data-stu-id="790c2-210">8234 (0x202A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-211">驗證機制未知。</span><span class="sxs-lookup"><span data-stu-id="790c2-211">The authentication mechanism is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**錯誤 \_ DS \_ 參考**</span><span class="sxs-lookup"><span data-stu-id="790c2-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**ERROR\_DS\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-213">8235 (0x202B) </span><span class="sxs-lookup"><span data-stu-id="790c2-213">8235 (0x202B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-214">已從伺服器傳回轉介。</span><span class="sxs-lookup"><span data-stu-id="790c2-214">A referral was returned from the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**錯誤 \_ DS \_ 無法使用 \_ 臨界 \_ 延伸模組**</span><span class="sxs-lookup"><span data-stu-id="790c2-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR\_DS\_UNAVAILABLE\_CRIT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-216">8236 (0x202C) </span><span class="sxs-lookup"><span data-stu-id="790c2-216">8236 (0x202C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-217">伺服器不支援要求的重要延伸模組。</span><span class="sxs-lookup"><span data-stu-id="790c2-217">The server does not support the requested critical extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**\_需要 DS \_ 機密性 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR\_DS\_CONFIDENTIALITY\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-219">8237 (0x202D) </span><span class="sxs-lookup"><span data-stu-id="790c2-219">8237 (0x202D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-220">此要求需要安全連線。</span><span class="sxs-lookup"><span data-stu-id="790c2-220">This request requires a secure connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**錯誤 \_ DS 不 \_ 適當的 \_ 相符**</span><span class="sxs-lookup"><span data-stu-id="790c2-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR\_DS\_INAPPROPRIATE\_MATCHING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-222">8238 (0x202E) </span><span class="sxs-lookup"><span data-stu-id="790c2-222">8238 (0x202E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-223">不適當的相符。</span><span class="sxs-lookup"><span data-stu-id="790c2-223">Inappropriate matching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**錯誤 \_ DS \_ 條件約束 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="790c2-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR\_DS\_CONSTRAINT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-225">8239 (0x202F) </span><span class="sxs-lookup"><span data-stu-id="790c2-225">8239 (0x202F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-226">發生條件約束違規。</span><span class="sxs-lookup"><span data-stu-id="790c2-226">A constraint violation occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**錯誤 \_ DS \_ 沒有 \_ 這類 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR\_DS\_NO\_SUCH\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-228">8240 (0x2030) </span><span class="sxs-lookup"><span data-stu-id="790c2-228">8240 (0x2030)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-229">伺服器上沒有此類物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-229">There is no such object on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**錯誤 \_ DS \_ 別名 \_ 問題**</span><span class="sxs-lookup"><span data-stu-id="790c2-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERROR\_DS\_ALIAS\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-231">8241 (0x2031) </span><span class="sxs-lookup"><span data-stu-id="790c2-231">8241 (0x2031)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-232">有別名問題。</span><span class="sxs-lookup"><span data-stu-id="790c2-232">There is an alias problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**錯誤 \_ DS \_ 不正確 \_ DN \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="790c2-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR\_DS\_INVALID\_DN\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-234">8242 (0x2032) </span><span class="sxs-lookup"><span data-stu-id="790c2-234">8242 (0x2032)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-235">指定了不正確 dn 語法。</span><span class="sxs-lookup"><span data-stu-id="790c2-235">An invalid dn syntax has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**錯誤 \_ DS \_ 是分 \_ 葉**</span><span class="sxs-lookup"><span data-stu-id="790c2-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERROR\_DS\_IS\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-237">8243 (0x2033) </span><span class="sxs-lookup"><span data-stu-id="790c2-237">8243 (0x2033)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-238">物件是分葉物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-238">The object is a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**錯誤 \_ DS \_ 別名 \_ DEREF \_ 問題**</span><span class="sxs-lookup"><span data-stu-id="790c2-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERROR\_DS\_ALIAS\_DEREF\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-240">8244 (0x2034) </span><span class="sxs-lookup"><span data-stu-id="790c2-240">8244 (0x2034)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-241">有一個別名參考問題。</span><span class="sxs-lookup"><span data-stu-id="790c2-241">There is an alias dereferencing problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**\_DS 不 \_ 願意 \_ \_ 執行的錯誤 DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR\_DS\_UNWILLING\_TO\_PERFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-243">8245 (0x2035) </span><span class="sxs-lookup"><span data-stu-id="790c2-243">8245 (0x2035)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-244">伺服器不願意處理要求。</span><span class="sxs-lookup"><span data-stu-id="790c2-244">The server is unwilling to process the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**\_DS \_ 迴圈偵測 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR\_DS\_LOOP\_DETECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-246">8246 (0x2036) </span><span class="sxs-lookup"><span data-stu-id="790c2-246">8246 (0x2036)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-247">偵測到迴圈。</span><span class="sxs-lookup"><span data-stu-id="790c2-247">A loop has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**\_DS \_ 命名 \_ 違規時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR\_DS\_NAMING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-249">8247 (0x2037) </span><span class="sxs-lookup"><span data-stu-id="790c2-249">8247 (0x2037)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-250">發生命名違規。</span><span class="sxs-lookup"><span data-stu-id="790c2-250">There is a naming violation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**錯誤 \_ DS \_ 物件 \_ 結果 \_ 太 \_ 大**</span><span class="sxs-lookup"><span data-stu-id="790c2-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERROR\_DS\_OBJECT\_RESULTS\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-252">8248 (0x2038) </span><span class="sxs-lookup"><span data-stu-id="790c2-252">8248 (0x2038)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-253">結果集太大。</span><span class="sxs-lookup"><span data-stu-id="790c2-253">The result set is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**錯誤 \_ DS \_ 會影響 \_ 多個 \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="790c2-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERROR\_DS\_AFFECTS\_MULTIPLE\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-255">8249 (0x2039) </span><span class="sxs-lookup"><span data-stu-id="790c2-255">8249 (0x2039)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-256">作業會影響多個 Dsa。</span><span class="sxs-lookup"><span data-stu-id="790c2-256">The operation affects multiple DSAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**錯誤 \_ DS \_ 伺服器 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="790c2-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR\_DS\_SERVER\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-258">8250 (0x203A) </span><span class="sxs-lookup"><span data-stu-id="790c2-258">8250 (0x203A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-259">無法操作伺服器。</span><span class="sxs-lookup"><span data-stu-id="790c2-259">The server is not operational.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**錯誤 \_ DS \_ 本機 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**ERROR\_DS\_LOCAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-261">8251 (0x203B) </span><span class="sxs-lookup"><span data-stu-id="790c2-261">8251 (0x203B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-262">發生本機錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-262">A local error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**錯誤 \_ DS \_ 編碼 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**ERROR\_DS\_ENCODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-264">8252 (0x203C) </span><span class="sxs-lookup"><span data-stu-id="790c2-264">8252 (0x203C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-265">發生了編碼錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-265">An encoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**錯誤 \_ DS \_ 解碼 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**ERROR\_DS\_DECODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-267">8253 (0x203D) </span><span class="sxs-lookup"><span data-stu-id="790c2-267">8253 (0x203D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-268">發生解碼錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-268">A decoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**錯誤 \_ DS \_ 篩選器 \_ 未知**</span><span class="sxs-lookup"><span data-stu-id="790c2-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR\_DS\_FILTER\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-270">8254 (0x203E) </span><span class="sxs-lookup"><span data-stu-id="790c2-270">8254 (0x203E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-271">無法辨認搜尋篩選準則。</span><span class="sxs-lookup"><span data-stu-id="790c2-271">The search filter cannot be recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**錯誤 \_ DS \_ 參數 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**ERROR\_DS\_PARAM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-273">8255 (0x203F) </span><span class="sxs-lookup"><span data-stu-id="790c2-273">8255 (0x203F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-274">一或多個參數不合法。</span><span class="sxs-lookup"><span data-stu-id="790c2-274">One or more parameters are illegal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**\_ \_ 不支援錯誤 \_ DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR\_DS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-276">8256 (0x2040) </span><span class="sxs-lookup"><span data-stu-id="790c2-276">8256 (0x2040)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-277">不支援指定的方法。</span><span class="sxs-lookup"><span data-stu-id="790c2-277">The specified method is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**錯誤 \_ DS \_ 沒有 \_ 傳回任何結果 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR\_DS\_NO\_RESULTS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-279">8257 (0x2041) </span><span class="sxs-lookup"><span data-stu-id="790c2-279">8257 (0x2041)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-280">未傳回任何結果。</span><span class="sxs-lookup"><span data-stu-id="790c2-280">No results were returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**\_ \_ \_ 找不到 DS \_ 控制項錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERROR\_DS\_CONTROL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-282">8258 (0x2042) </span><span class="sxs-lookup"><span data-stu-id="790c2-282">8258 (0x2042)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-283">伺服器不支援指定的控制項。</span><span class="sxs-lookup"><span data-stu-id="790c2-283">The specified control is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**錯誤 \_ DS \_ 用戶端 \_ 迴圈**</span><span class="sxs-lookup"><span data-stu-id="790c2-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR\_DS\_CLIENT\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-285">8259 (0x2043) </span><span class="sxs-lookup"><span data-stu-id="790c2-285">8259 (0x2043)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-286">用戶端偵測到參考迴圈。</span><span class="sxs-lookup"><span data-stu-id="790c2-286">A referral loop was detected by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**\_超過錯誤 DS \_ 參考 \_ 限制 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERROR\_DS\_REFERRAL\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-288">8260 (0x2044) </span><span class="sxs-lookup"><span data-stu-id="790c2-288">8260 (0x2044)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-289">超過預設的參考限制。</span><span class="sxs-lookup"><span data-stu-id="790c2-289">The preset referral limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**\_缺少 DS \_ 排序 \_ 控制項 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR\_DS\_SORT\_CONTROL\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-291">8261 (0x2045) </span><span class="sxs-lookup"><span data-stu-id="790c2-291">8261 (0x2045)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-292">搜尋需要 SORT 控制項。</span><span class="sxs-lookup"><span data-stu-id="790c2-292">The search requires a SORT control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**錯誤 \_ DS \_ 位移 \_ 範圍 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**ERROR\_DS\_OFFSET\_RANGE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-294">8262 (0x2046) </span><span class="sxs-lookup"><span data-stu-id="790c2-294">8262 (0x2046)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-295">搜尋結果超過指定的位移範圍。</span><span class="sxs-lookup"><span data-stu-id="790c2-295">The search results exceed the offset range specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**錯誤 \_ DS \_ RIDMGR \_ 已停用**</span><span class="sxs-lookup"><span data-stu-id="790c2-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR\_DS\_RIDMGR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-297">8263 (0x2047) </span><span class="sxs-lookup"><span data-stu-id="790c2-297">8263 (0x2047)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-298">目錄服務偵測到配置相對識別碼的子系統已停用。</span><span class="sxs-lookup"><span data-stu-id="790c2-298">The directory service detected the subsystem that allocates relative identifiers is disabled.</span></span> <span data-ttu-id="790c2-299">當系統判斷 (Rid) 已用盡之相對識別碼的重要部分時，就會發生這種保護機制。</span><span class="sxs-lookup"><span data-stu-id="790c2-299">This can occur as a protective mechanism when the system determines a significant portion of relative identifiers (RIDs) have been exhausted.</span></span> <span data-ttu-id="790c2-300">如需 <https://go.microsoft.com/fwlink/p/?linkid=228610> 建議的診斷步驟和重新啟用帳戶建立的程式，請參閱。</span><span class="sxs-lookup"><span data-stu-id="790c2-300">Please see <https://go.microsoft.com/fwlink/p/?linkid=228610> for recommended diagnostic steps and the procedure to re-enable account creation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**錯誤 \_ DS \_ 根 \_ 必須 \_ 是 \_ NC**</span><span class="sxs-lookup"><span data-stu-id="790c2-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERROR\_DS\_ROOT\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-302">8301 (0x206D) </span><span class="sxs-lookup"><span data-stu-id="790c2-302">8301 (0x206D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-303">根物件必須是命名內容的標頭。</span><span class="sxs-lookup"><span data-stu-id="790c2-303">The root object must be the head of a naming context.</span></span> <span data-ttu-id="790c2-304">根物件不能有具現化的父系。</span><span class="sxs-lookup"><span data-stu-id="790c2-304">The root object cannot have an instantiated parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**禁止 \_ DS \_ 新增 \_ 複本 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR\_DS\_ADD\_REPLICA\_INHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-306">8302 (0x206E) </span><span class="sxs-lookup"><span data-stu-id="790c2-306">8302 (0x206E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-307">無法執行新增複本作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-307">The add replica operation cannot be performed.</span></span> <span data-ttu-id="790c2-308">命名內容必須是可寫入的，才能建立複本。</span><span class="sxs-lookup"><span data-stu-id="790c2-308">The naming context must be writeable in order to create the replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**\_ \_ \_ \_ \_ 架構中的錯誤 DS ATT 不是 DEF \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-310">8303 (0x206F) </span><span class="sxs-lookup"><span data-stu-id="790c2-310">8303 (0x206F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-311">未在架構中定義之屬性的參考發生。</span><span class="sxs-lookup"><span data-stu-id="790c2-311">A reference to an attribute that is not defined in the schema occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**\_超過錯誤 DS 的 \_ 最大 \_ OBJ \_ 大小 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERROR\_DS\_MAX\_OBJ\_SIZE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-313">8304 (0x2070) </span><span class="sxs-lookup"><span data-stu-id="790c2-313">8304 (0x2070)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-314">已超過物件的大小上限。</span><span class="sxs-lookup"><span data-stu-id="790c2-314">The maximum size of an object has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**錯誤 \_ DS \_ OBJ \_ 字串 \_ 名稱 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="790c2-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR\_DS\_OBJ\_STRING\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-316">8305 (0x2071) </span><span class="sxs-lookup"><span data-stu-id="790c2-316">8305 (0x2071)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-317">嘗試使用已在使用中的名稱，將物件新增至目錄。</span><span class="sxs-lookup"><span data-stu-id="790c2-317">An attempt was made to add an object to the directory with a name that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**錯誤 \_ DS \_ \_ \_ \_ 在架構中未定義 RDN \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR\_DS\_NO\_RDN\_DEFINED\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-319">8306 (0x2072) </span><span class="sxs-lookup"><span data-stu-id="790c2-319">8306 (0x2072)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-320">嘗試加入類別的物件，而該類別沒有定義在架構中的 RDN。</span><span class="sxs-lookup"><span data-stu-id="790c2-320">An attempt was made to add an object of a class that does not have an RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**錯誤 \_ DS \_ RDN \_ 不 \_ 符合 \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="790c2-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERROR\_DS\_RDN\_DOESNT\_MATCH\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-322">8307 (0x2073) </span><span class="sxs-lookup"><span data-stu-id="790c2-322">8307 (0x2073)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-323">嘗試使用不是在架構中定義之 RDN 的 RDN 來新增物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-323">An attempt was made to add an object using an RDN that is not the RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**錯誤 \_ DS \_ \_ 找不到要求的 \_ ATTS \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR\_DS\_NO\_REQUESTED\_ATTS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-325">8308 (0x2074) </span><span class="sxs-lookup"><span data-stu-id="790c2-325">8308 (0x2074)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-326">在物件上找不到任何要求的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-326">None of the requested attributes were found on the objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**錯誤 \_ DS \_ 使用者 \_ 緩衝區 \_ 至 \_ 小型**</span><span class="sxs-lookup"><span data-stu-id="790c2-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR\_DS\_USER\_BUFFER\_TO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-328">8309 (0x2075) </span><span class="sxs-lookup"><span data-stu-id="790c2-328">8309 (0x2075)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-329">使用者緩衝區太小。</span><span class="sxs-lookup"><span data-stu-id="790c2-329">The user buffer is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**錯誤 \_ DS \_ ATT \_ \_ 不 \_ 在 \_ OBJ 上**</span><span class="sxs-lookup"><span data-stu-id="790c2-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR\_DS\_ATT\_IS\_NOT\_ON\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-331">8310 (0x2076) </span><span class="sxs-lookup"><span data-stu-id="790c2-331">8310 (0x2076)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-332">在作業中指定的屬性不存在於物件中。</span><span class="sxs-lookup"><span data-stu-id="790c2-332">The attribute specified in the operation is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**錯誤 \_ DS 不 \_ 合法的 \_ MOD \_ 運算**</span><span class="sxs-lookup"><span data-stu-id="790c2-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR\_DS\_ILLEGAL\_MOD\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-334">8311 (0x2077) </span><span class="sxs-lookup"><span data-stu-id="790c2-334">8311 (0x2077)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-335">不合法的修改作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-335">Illegal modify operation.</span></span> <span data-ttu-id="790c2-336">不允許修改的某些層面。</span><span class="sxs-lookup"><span data-stu-id="790c2-336">Some aspect of the modification is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**錯誤 \_ DS \_ OBJ \_ 太 \_ 大**</span><span class="sxs-lookup"><span data-stu-id="790c2-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERROR\_DS\_OBJ\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-338">8312 (0x2078) </span><span class="sxs-lookup"><span data-stu-id="790c2-338">8312 (0x2078)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-339">指定的物件太大。</span><span class="sxs-lookup"><span data-stu-id="790c2-339">The specified object is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**錯誤 \_ DS 錯誤的 \_ \_ 實例 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="790c2-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERROR\_DS\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-341">8313 (0x2079) </span><span class="sxs-lookup"><span data-stu-id="790c2-341">8313 (0x2079)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-342">指定的實例類型無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-342">The specified instance type is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**\_需要錯誤 DS \_ MASTERDSA \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR\_DS\_MASTERDSA\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-344">8314 (0x207A) </span><span class="sxs-lookup"><span data-stu-id="790c2-344">8314 (0x207A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-345">此操作必須在主要 DSA 上執行。</span><span class="sxs-lookup"><span data-stu-id="790c2-345">The operation must be performed at a master DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**\_需要 ERROR DS \_ 物件 \_ 類別 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**ERROR\_DS\_OBJECT\_CLASS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-347">8315 (0x207B) </span><span class="sxs-lookup"><span data-stu-id="790c2-347">8315 (0x207B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-348">必須指定物件類別屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-348">The object class attribute must be specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**錯誤 \_ DS \_ 遺失 \_ 必要的 \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="790c2-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR\_DS\_MISSING\_REQUIRED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-350">8316 (0x207C) </span><span class="sxs-lookup"><span data-stu-id="790c2-350">8316 (0x207C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-351">遺漏必要的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-351">A required attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**錯誤 \_ DS \_ ATT \_ NOT \_ \_ 類別的 \_ DEF**</span><span class="sxs-lookup"><span data-stu-id="790c2-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_FOR\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-353">8317 (0x207D) </span><span class="sxs-lookup"><span data-stu-id="790c2-353">8317 (0x207D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-354">嘗試修改物件以包含對其類別而言不合法的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-354">An attempt was made to modify an object to include an attribute that is not legal for its class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**錯誤 \_ DS \_ ATT \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="790c2-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERROR\_DS\_ATT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-356">8318 (0x207E) </span><span class="sxs-lookup"><span data-stu-id="790c2-356">8318 (0x207E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-357">物件上已經有指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-357">The specified attribute is already present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**錯誤 \_ DS \_ 無法 \_ 新增 \_ ATT \_ 值**</span><span class="sxs-lookup"><span data-stu-id="790c2-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR\_DS\_CANT\_ADD\_ATT\_VALUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-359">8320 (0x2080) </span><span class="sxs-lookup"><span data-stu-id="790c2-359">8320 (0x2080)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-360">指定的屬性不存在，或沒有任何值。</span><span class="sxs-lookup"><span data-stu-id="790c2-360">The specified attribute is not present, or has no values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR \_ DS \_ 單一 \_ 值 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="790c2-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR\_DS\_SINGLE\_VALUE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-362">8321 (0x2081) </span><span class="sxs-lookup"><span data-stu-id="790c2-362">8321 (0x2081)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-363">針對只能有一個值的屬性，指定了多個值。</span><span class="sxs-lookup"><span data-stu-id="790c2-363">Multiple values were specified for an attribute that can have only one value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**錯誤 \_ DS \_ 範圍 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="790c2-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERROR\_DS\_RANGE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-365">8322 (0x2082) </span><span class="sxs-lookup"><span data-stu-id="790c2-365">8322 (0x2082)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-366">屬性的值不在可接受的值範圍內。</span><span class="sxs-lookup"><span data-stu-id="790c2-366">A value for the attribute was not in the acceptable range of values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**錯誤 \_ DS \_ ATT \_ VAL \_ 已經 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="790c2-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERROR\_DS\_ATT\_VAL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-368">8323 (0x2083) </span><span class="sxs-lookup"><span data-stu-id="790c2-368">8323 (0x2083)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-369">指定的值已存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-369">The specified value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**錯誤 \_ DS \_ 無法 \_ REM \_ 遺失 \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="790c2-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-371">8324 (0x2084) </span><span class="sxs-lookup"><span data-stu-id="790c2-371">8324 (0x2084)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-372">無法移除屬性，因為該屬性不存在於物件上。</span><span class="sxs-lookup"><span data-stu-id="790c2-372">The attribute cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**錯誤 \_ DS \_ 無法 \_ REM \_ 遺漏 \_ ATT \_ VAL**</span><span class="sxs-lookup"><span data-stu-id="790c2-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT\_VAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-374">8325 (0x2085) </span><span class="sxs-lookup"><span data-stu-id="790c2-374">8325 (0x2085)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-375">無法移除屬性值，因為它不存在於物件上。</span><span class="sxs-lookup"><span data-stu-id="790c2-375">The attribute value cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**\_ \_ \_ \_ 無法 \_ SUBREF 錯誤 DS 根目錄**</span><span class="sxs-lookup"><span data-stu-id="790c2-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR\_DS\_ROOT\_CANT\_BE\_SUBREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-377">8326 (0x2086) </span><span class="sxs-lookup"><span data-stu-id="790c2-377">8326 (0x2086)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-378">指定的根物件不可以是 subref。</span><span class="sxs-lookup"><span data-stu-id="790c2-378">The specified root object cannot be a subref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**錯誤 \_ DS \_ 沒有 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="790c2-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR\_DS\_NO\_CHAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-380">8327 (0x2087) </span><span class="sxs-lookup"><span data-stu-id="790c2-380">8327 (0x2087)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-381">不允許使用連結。</span><span class="sxs-lookup"><span data-stu-id="790c2-381">Chaining is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**錯誤 \_ DS \_ 沒有 \_ 連結的 \_ 評估**</span><span class="sxs-lookup"><span data-stu-id="790c2-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR\_DS\_NO\_CHAINED\_EVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-383">8328 (0x2088) </span><span class="sxs-lookup"><span data-stu-id="790c2-383">8328 (0x2088)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-384">不允許連鎖的評估。</span><span class="sxs-lookup"><span data-stu-id="790c2-384">Chained evaluation is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**錯誤 \_ DS \_ 沒有 \_ 父 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR\_DS\_NO\_PARENT\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-386">8329 (0x2089) </span><span class="sxs-lookup"><span data-stu-id="790c2-386">8329 (0x2089)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-387">無法執行操作，因為物件的父系可能無法建立例項或已被刪除。</span><span class="sxs-lookup"><span data-stu-id="790c2-387">The operation could not be performed because the object's parent is either uninstantiated or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**錯誤 \_ DS \_ 父系 \_ 是 \_ \_ 別名**</span><span class="sxs-lookup"><span data-stu-id="790c2-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERROR\_DS\_PARENT\_IS\_AN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-389">8330 (0x208A) </span><span class="sxs-lookup"><span data-stu-id="790c2-389">8330 (0x208A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-390">不允許擁有別名的父系。</span><span class="sxs-lookup"><span data-stu-id="790c2-390">Having a parent that is an alias is not permitted.</span></span> <span data-ttu-id="790c2-391">別名是分葉物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-391">Aliases are leaf objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**錯誤 \_ DS \_ 無法 \_ 混合 \_ 主機 \_ 和 \_ 代表**</span><span class="sxs-lookup"><span data-stu-id="790c2-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR\_DS\_CANT\_MIX\_MASTER\_AND\_REPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-393">8331 (0x208B) </span><span class="sxs-lookup"><span data-stu-id="790c2-393">8331 (0x208B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-394">物件和父系必須屬於相同類型，不論是 master 或兩個複本。</span><span class="sxs-lookup"><span data-stu-id="790c2-394">The object and parent must be of the same type, either both masters or both replicas.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**\_DS \_ 子系 \_ 存在錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR\_DS\_CHILDREN\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-396">8332 (0x208C) </span><span class="sxs-lookup"><span data-stu-id="790c2-396">8332 (0x208C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-397">無法執行操作，因為子物件存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-397">The operation cannot be performed because child objects exist.</span></span> <span data-ttu-id="790c2-398">此作業只能在分葉物件上執行。</span><span class="sxs-lookup"><span data-stu-id="790c2-398">This operation can only be performed on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**\_ \_ \_ 找不到 DS \_ OBJ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERROR\_DS\_OBJ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-400">8333 (0x208D) </span><span class="sxs-lookup"><span data-stu-id="790c2-400">8333 (0x208D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-401">找不到目錄物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-401">Directory object not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**\_缺少錯誤 DS \_ 別名的 \_ OBJ \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERROR\_DS\_ALIASED\_OBJ\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-403">8334 (0x208E) </span><span class="sxs-lookup"><span data-stu-id="790c2-403">8334 (0x208E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-404">遺漏了別名的物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-404">The aliased object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**錯誤 \_ DS \_ 錯誤 \_ 名稱 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="790c2-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR\_DS\_BAD\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-406">8335 (0x208F) </span><span class="sxs-lookup"><span data-stu-id="790c2-406">8335 (0x208F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-407">物件名稱的語法不正確。</span><span class="sxs-lookup"><span data-stu-id="790c2-407">The object name has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**錯誤 \_ DS \_ 別名 \_ 指向 \_ \_ 別名**</span><span class="sxs-lookup"><span data-stu-id="790c2-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERROR\_DS\_ALIAS\_POINTS\_TO\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-409">8336 (0x2090) </span><span class="sxs-lookup"><span data-stu-id="790c2-409">8336 (0x2090)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-410">別名不允許參考另一個別名。</span><span class="sxs-lookup"><span data-stu-id="790c2-410">It is not permitted for an alias to refer to another alias.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**錯誤 \_ DS 無法進行 \_ \_ DEREF \_ 別名**</span><span class="sxs-lookup"><span data-stu-id="790c2-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR\_DS\_CANT\_DEREF\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-412">8337 (0x2091) </span><span class="sxs-lookup"><span data-stu-id="790c2-412">8337 (0x2091)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-413">別名無法取值。</span><span class="sxs-lookup"><span data-stu-id="790c2-413">The alias cannot be dereferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**錯誤 \_ DS \_ 超出 \_ \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="790c2-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR\_DS\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-415">8338 (0x2092) </span><span class="sxs-lookup"><span data-stu-id="790c2-415">8338 (0x2092)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-416">作業超出範圍。</span><span class="sxs-lookup"><span data-stu-id="790c2-416">The operation is out of scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**\_ \_ \_ 移除的 DS 物件 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR\_DS\_OBJECT\_BEING\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-418">8339 (0x2093) </span><span class="sxs-lookup"><span data-stu-id="790c2-418">8339 (0x2093)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-419">無法繼續操作，因為物件正在移除中。</span><span class="sxs-lookup"><span data-stu-id="790c2-419">The operation cannot continue because the object is in the process of being removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**錯誤 \_ DS \_ 無法 \_ 刪除 \_ DSA \_ OBJ**</span><span class="sxs-lookup"><span data-stu-id="790c2-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR\_DS\_CANT\_DELETE\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-421">8340 (0x2094) </span><span class="sxs-lookup"><span data-stu-id="790c2-421">8340 (0x2094)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-422">無法刪除 DSA 物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-422">The DSA object cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**錯誤 \_ DS \_ 一般 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**ERROR\_DS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-424">8341 (0x2095) </span><span class="sxs-lookup"><span data-stu-id="790c2-424">8341 (0x2095)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-425">發生目錄服務錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-425">A directory service error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**錯誤 \_ DS \_ DSA \_ 必須 \_ 是 \_ INT \_ 主機**</span><span class="sxs-lookup"><span data-stu-id="790c2-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR\_DS\_DSA\_MUST\_BE\_INT\_MASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-427">8342 (0x2096) </span><span class="sxs-lookup"><span data-stu-id="790c2-427">8342 (0x2096)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-428">此操作只能在內部主要 DSA 物件上執行。</span><span class="sxs-lookup"><span data-stu-id="790c2-428">The operation can only be performed on an internal master DSA object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**錯誤 \_ DS \_ 類別 \_ 不是 \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="790c2-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR\_DS\_CLASS\_NOT\_DSA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-430">8343 (0x2097) </span><span class="sxs-lookup"><span data-stu-id="790c2-430">8343 (0x2097)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-431">物件必須是類別 DSA。</span><span class="sxs-lookup"><span data-stu-id="790c2-431">The object must be of class DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**錯誤 \_ DS \_ INSUFF \_ 訪問 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="790c2-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERROR\_DS\_INSUFF\_ACCESS\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-433">8344 (0x2098) </span><span class="sxs-lookup"><span data-stu-id="790c2-433">8344 (0x2098)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-434">許可權不足，無法執行此作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-434">Insufficient access rights to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**錯誤 \_ DS 不 \_ 合法的 \_ 高階**</span><span class="sxs-lookup"><span data-stu-id="790c2-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR\_DS\_ILLEGAL\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-436">8345 (0x2099) </span><span class="sxs-lookup"><span data-stu-id="790c2-436">8345 (0x2099)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-437">無法加入物件，因為父系不在可能的 superiors 清單中。</span><span class="sxs-lookup"><span data-stu-id="790c2-437">The object cannot be added because the parent is not on the list of possible superiors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**\_ \_ \_ SAM 所擁有 \_ 的 \_ 錯誤 DS 屬性**</span><span class="sxs-lookup"><span data-stu-id="790c2-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERROR\_DS\_ATTRIBUTE\_OWNED\_BY\_SAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-439">8346 (0x209A) </span><span class="sxs-lookup"><span data-stu-id="790c2-439">8346 (0x209A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-440">因為屬性是由安全性帳戶管理員 (SAM) 所擁有，所以不允許存取屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-440">Access to the attribute is not permitted because the attribute is owned by the Security Accounts Manager (SAM).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**錯誤 \_ DS \_ 名稱 \_ 太 \_ 多 \_ 部分**</span><span class="sxs-lookup"><span data-stu-id="790c2-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR\_DS\_NAME\_TOO\_MANY\_PARTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-442">8347 (0x209B) </span><span class="sxs-lookup"><span data-stu-id="790c2-442">8347 (0x209B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-443">名稱具有太多部分。</span><span class="sxs-lookup"><span data-stu-id="790c2-443">The name has too many parts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**錯誤 \_ DS \_ 名稱 \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="790c2-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR\_DS\_NAME\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-445">8348 (0x209C) </span><span class="sxs-lookup"><span data-stu-id="790c2-445">8348 (0x209C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-446">名稱太長。</span><span class="sxs-lookup"><span data-stu-id="790c2-446">The name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**錯誤 \_ DS \_ 名稱 \_ 值 \_ 太 \_ 長**</span><span class="sxs-lookup"><span data-stu-id="790c2-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERROR\_DS\_NAME\_VALUE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-448">8349 (0x209D) </span><span class="sxs-lookup"><span data-stu-id="790c2-448">8349 (0x209D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-449">名稱值太長。</span><span class="sxs-lookup"><span data-stu-id="790c2-449">The name value is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**錯誤 \_ DS \_ 名稱無法 \_ 分析**</span><span class="sxs-lookup"><span data-stu-id="790c2-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR\_DS\_NAME\_UNPARSEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-451">8350 (0x209E) </span><span class="sxs-lookup"><span data-stu-id="790c2-451">8350 (0x209E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-452">目錄服務剖析名稱時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-452">The directory service encountered an error parsing a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**錯誤 \_ DS \_ 名稱 \_ 類型 \_ 未知**</span><span class="sxs-lookup"><span data-stu-id="790c2-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR\_DS\_NAME\_TYPE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-454">8351 (0x209F) </span><span class="sxs-lookup"><span data-stu-id="790c2-454">8351 (0x209F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-455">目錄服務無法取得名稱的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="790c2-455">The directory service cannot get the attribute type for a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**錯誤 \_ DS \_ 不 \_ 是 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR\_DS\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-457">8352 (0x20A0) </span><span class="sxs-lookup"><span data-stu-id="790c2-457">8352 (0x20A0)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-458">名稱不會識別物件;名稱會識別虛設專案。</span><span class="sxs-lookup"><span data-stu-id="790c2-458">The name does not identify an object; the name identifies a phantom.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR \_ DS \_ SEC \_ DESC \_ 太 \_ 短**</span><span class="sxs-lookup"><span data-stu-id="790c2-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR\_DS\_SEC\_DESC\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-460">8353 (0x20A1) </span><span class="sxs-lookup"><span data-stu-id="790c2-460">8353 (0x20A1)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-461">安全描述項太短。</span><span class="sxs-lookup"><span data-stu-id="790c2-461">The security descriptor is too short.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR \_ DS \_ SEC \_ DESC \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="790c2-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR\_DS\_SEC\_DESC\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-463">8354 (0x20A2) </span><span class="sxs-lookup"><span data-stu-id="790c2-463">8354 (0x20A2)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-464">安全描述項無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-464">The security descriptor is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**錯誤 \_ DS \_ 未 \_ 刪除 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="790c2-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR\_DS\_NO\_DELETED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-466">8355 (0x20A3) </span><span class="sxs-lookup"><span data-stu-id="790c2-466">8355 (0x20A3)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-467">無法建立已刪除之物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="790c2-467">Failed to create name for deleted object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**錯誤 \_ DS \_ SUBREF \_ 必須 \_ 有 \_ 父系**</span><span class="sxs-lookup"><span data-stu-id="790c2-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERROR\_DS\_SUBREF\_MUST\_HAVE\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-469">8356 (0x20A4) </span><span class="sxs-lookup"><span data-stu-id="790c2-469">8356 (0x20A4)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-470">新 subref 的父系必須存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-470">The parent of a new subref must exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**錯誤 \_ DS \_ NCNAME \_ 必須 \_ 是 \_ NC**</span><span class="sxs-lookup"><span data-stu-id="790c2-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR\_DS\_NCNAME\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-472">8357 (0x20A5) </span><span class="sxs-lookup"><span data-stu-id="790c2-472">8357 (0x20A5)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-473">物件必須是命名內容。</span><span class="sxs-lookup"><span data-stu-id="790c2-473">The object must be a naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**錯誤 \_ DS \_ 無法 \_ 新增 \_ 系統 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR\_DS\_CANT\_ADD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-475">8358 (0x20A6) </span><span class="sxs-lookup"><span data-stu-id="790c2-475">8358 (0x20A6)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-476">不允許新增系統所擁有的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-476">It is not permitted to add an attribute which is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**ERROR \_ DS \_ 類別 \_ 必須 \_ 是 \_ 具體的**</span><span class="sxs-lookup"><span data-stu-id="790c2-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**ERROR\_DS\_CLASS\_MUST\_BE\_CONCRETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-478">8359 (0x20A7) </span><span class="sxs-lookup"><span data-stu-id="790c2-478">8359 (0x20A7)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-479">物件的類別必須是結構化的。您無法具現化抽象類別。</span><span class="sxs-lookup"><span data-stu-id="790c2-479">The class of the object must be structural; you cannot instantiate an abstract class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**錯誤 \_ DS \_ 不正確 \_ DMD**</span><span class="sxs-lookup"><span data-stu-id="790c2-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR\_DS\_INVALID\_DMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-481">8360 (0x20A8) </span><span class="sxs-lookup"><span data-stu-id="790c2-481">8360 (0x20A8)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-482">找不到架構物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-482">The schema object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**錯誤 \_ DS \_ OBJ \_ GUID \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="790c2-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERROR\_DS\_OBJ\_GUID\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-484">8361 (0x20A9) </span><span class="sxs-lookup"><span data-stu-id="790c2-484">8361 (0x20A9)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-485">具有這個 GUID)  (的本機物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-485">A local object with this GUID (dead or alive) already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**錯誤 \_ DS \_ 不 \_ 在 \_ BACKLINK 上**</span><span class="sxs-lookup"><span data-stu-id="790c2-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR\_DS\_NOT\_ON\_BACKLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-487">8362 (0x20AA) </span><span class="sxs-lookup"><span data-stu-id="790c2-487">8362 (0x20AA)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-488">無法在後置連結上執行此操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-488">The operation cannot be performed on a back link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**錯誤 \_ DS \_ 沒有 \_ \_ NC 的交叉引用 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR\_DS\_NO\_CROSSREF\_FOR\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-490">8363 (0x20AB) </span><span class="sxs-lookup"><span data-stu-id="790c2-490">8363 (0x20AB)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-491">找不到指定之命名內容的交互參考。</span><span class="sxs-lookup"><span data-stu-id="790c2-491">The cross reference for the specified naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**錯誤 \_ DS \_ 關機 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR\_DS\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-493">8364 (0x20AC) </span><span class="sxs-lookup"><span data-stu-id="790c2-493">8364 (0x20AC)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-494">無法執行操作，因為目錄服務正在關閉。</span><span class="sxs-lookup"><span data-stu-id="790c2-494">The operation could not be performed because the directory service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**錯誤 \_ DS \_ 不明 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="790c2-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR\_DS\_UNKNOWN\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-496">8365 (0x20AD) </span><span class="sxs-lookup"><span data-stu-id="790c2-496">8365 (0x20AD)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-497">目錄服務要求無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-497">The directory service request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**錯誤 \_ DS \_ 不正確 \_ 角色 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="790c2-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR\_DS\_INVALID\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-499">8366 (0x20AE) </span><span class="sxs-lookup"><span data-stu-id="790c2-499">8366 (0x20AE)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-500">無法讀取角色擁有者屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-500">The role owner attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**錯誤 \_ DS \_ 無法 \_ 聯絡 \_ FSMO**</span><span class="sxs-lookup"><span data-stu-id="790c2-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR\_DS\_COULDNT\_CONTACT\_FSMO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-502">8367 (0x20AF) </span><span class="sxs-lookup"><span data-stu-id="790c2-502">8367 (0x20AF)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-503">要求的 FSMO 作業失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-503">The requested FSMO operation failed.</span></span> <span data-ttu-id="790c2-504">無法連絡目前的 FSMO 持有人。</span><span class="sxs-lookup"><span data-stu-id="790c2-504">The current FSMO holder could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**錯誤 \_ DS \_ 跨 \_ NC \_ DN \_ 重新命名**</span><span class="sxs-lookup"><span data-stu-id="790c2-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR\_DS\_CROSS\_NC\_DN\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-506">8368 (0x20B0) </span><span class="sxs-lookup"><span data-stu-id="790c2-506">8368 (0x20B0)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-507">不允許在命名內容中修改 DN。</span><span class="sxs-lookup"><span data-stu-id="790c2-507">Modification of a DN across a naming context is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**錯誤 \_ DS \_ 無法 \_ MOD \_ 系統 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR\_DS\_CANT\_MOD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-509">8369 (0x20B1) </span><span class="sxs-lookup"><span data-stu-id="790c2-509">8369 (0x20B1)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-510">因為屬性是由系統所擁有，所以無法修改。</span><span class="sxs-lookup"><span data-stu-id="790c2-510">The attribute cannot be modified because it is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**\_ \_ 僅限錯誤 DS 複寫器 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR\_DS\_REPLICATOR\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-512">8370 (0x20B2) </span><span class="sxs-lookup"><span data-stu-id="790c2-512">8370 (0x20B2)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-513">只有複寫器可以執行此功能。</span><span class="sxs-lookup"><span data-stu-id="790c2-513">Only the replicator can perform this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**\_ \_ \_ \_ 未定義錯誤 DS OBJ \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="790c2-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-515">8371 (0x20B3) </span><span class="sxs-lookup"><span data-stu-id="790c2-515">8371 (0x20B3)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-516">未定義指定的類別。</span><span class="sxs-lookup"><span data-stu-id="790c2-516">The specified class is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR \_ DS \_ OBJ \_ 類別 \_ 不 \_ 是子類別**</span><span class="sxs-lookup"><span data-stu-id="790c2-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_SUBCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-518">8372 (0x20B4) </span><span class="sxs-lookup"><span data-stu-id="790c2-518">8372 (0x20B4)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-519">指定的類別不是子類別。</span><span class="sxs-lookup"><span data-stu-id="790c2-519">The specified class is not a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**錯誤 \_ DS \_ 名稱 \_ 參考 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="790c2-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR\_DS\_NAME\_REFERENCE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-521">8373 (0x20B5) </span><span class="sxs-lookup"><span data-stu-id="790c2-521">8373 (0x20B5)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-522">名稱參考無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-522">The name reference is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**錯誤 \_ DS \_ 交互 \_ 參照 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="790c2-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERROR\_DS\_CROSS\_REF\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-524">8374 (0x20B6) </span><span class="sxs-lookup"><span data-stu-id="790c2-524">8374 (0x20B6)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-525">交叉參考已存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-525">A cross reference already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**錯誤 \_ DS \_ 無法 \_ DEL \_ 主機 \_ 交叉引用**</span><span class="sxs-lookup"><span data-stu-id="790c2-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR\_DS\_CANT\_DEL\_MASTER\_CROSSREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-527">8375 (0x20B7) </span><span class="sxs-lookup"><span data-stu-id="790c2-527">8375 (0x20B7)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-528">不允許刪除主要交互參考。</span><span class="sxs-lookup"><span data-stu-id="790c2-528">It is not permitted to delete a master cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**錯誤 \_ DS \_ 子樹 \_ 通知 \_ NOT \_ NC \_ HEAD**</span><span class="sxs-lookup"><span data-stu-id="790c2-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR\_DS\_SUBTREE\_NOTIFY\_NOT\_NC\_HEAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-530">8376 (0x20B8) </span><span class="sxs-lookup"><span data-stu-id="790c2-530">8376 (0x20B8)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-531">只有 NC 標頭才支援子樹通知。</span><span class="sxs-lookup"><span data-stu-id="790c2-531">Subtree notifications are only supported on NC heads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**錯誤 \_ DS \_ 通知 \_ 篩選 \_ 太 \_ 複雜**</span><span class="sxs-lookup"><span data-stu-id="790c2-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR\_DS\_NOTIFY\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-533">8377 (0x20B9) </span><span class="sxs-lookup"><span data-stu-id="790c2-533">8377 (0x20B9)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-534">通知篩選太複雜。</span><span class="sxs-lookup"><span data-stu-id="790c2-534">Notification filter is too complex.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR \_ DS \_ DUP \_ RDN**</span><span class="sxs-lookup"><span data-stu-id="790c2-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR\_DS\_DUP\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-536">8378 (0x20BA) </span><span class="sxs-lookup"><span data-stu-id="790c2-536">8378 (0x20BA)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-537">架構更新失敗：重複的 RDN。</span><span class="sxs-lookup"><span data-stu-id="790c2-537">Schema update failed: duplicate RDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR \_ DS \_ DUP \_ OID**</span><span class="sxs-lookup"><span data-stu-id="790c2-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR\_DS\_DUP\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-539">8379 (0x20BB) </span><span class="sxs-lookup"><span data-stu-id="790c2-539">8379 (0x20BB)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-540">架構更新失敗：重複的 OID。</span><span class="sxs-lookup"><span data-stu-id="790c2-540">Schema update failed: duplicate OID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**錯誤 \_ DS \_ DUP \_ MAPI \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="790c2-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERROR\_DS\_DUP\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-542">8380 (0x20BC) </span><span class="sxs-lookup"><span data-stu-id="790c2-542">8380 (0x20BC)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-543">架構更新失敗：重複的 MAPI 識別碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-543">Schema update failed: duplicate MAPI identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR \_ DS \_ DUP \_ 架構 \_ 識別碼 \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="790c2-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR\_DS\_DUP\_SCHEMA\_ID\_GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-545">8381 (0x20BD) </span><span class="sxs-lookup"><span data-stu-id="790c2-545">8381 (0x20BD)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-546">架構更新失敗：重複的架構識別碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="790c2-546">Schema update failed: duplicate schema-id GUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR \_ DS \_ DUP \_ LDAP \_ 顯示 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="790c2-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR\_DS\_DUP\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-548">8382 (0x20BE) </span><span class="sxs-lookup"><span data-stu-id="790c2-548">8382 (0x20BE)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-549">架構更新失敗：重複的 LDAP 顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="790c2-549">Schema update failed: duplicate LDAP display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**錯誤 \_ DS \_ 語義 \_ ATT \_ 測試**</span><span class="sxs-lookup"><span data-stu-id="790c2-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR\_DS\_SEMANTIC\_ATT\_TEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-551">8383 (0x20BF) </span><span class="sxs-lookup"><span data-stu-id="790c2-551">8383 (0x20BF)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-552">架構更新失敗：範圍-低於範圍上限。</span><span class="sxs-lookup"><span data-stu-id="790c2-552">Schema update failed: range-lower less than range upper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**錯誤 \_ DS \_ 語法 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="790c2-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR\_DS\_SYNTAX\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-554">8384 (0x20C0) </span><span class="sxs-lookup"><span data-stu-id="790c2-554">8384 (0x20C0)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-555">架構更新失敗：語法不相符。</span><span class="sxs-lookup"><span data-stu-id="790c2-555">Schema update failed: syntax mismatch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**錯誤 \_ DS \_ 存在 \_ 于 \_ 必須 \_ 有**</span><span class="sxs-lookup"><span data-stu-id="790c2-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**ERROR\_DS\_EXISTS\_IN\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-557">8385 (0x20C1) </span><span class="sxs-lookup"><span data-stu-id="790c2-557">8385 (0x20C1)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-558">架構刪除失敗：屬性在必須包含的中使用。</span><span class="sxs-lookup"><span data-stu-id="790c2-558">Schema deletion failed: attribute is used in must-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**錯誤 \_ DS \_ 存在 \_ 于 \_ 可能 \_ 的**</span><span class="sxs-lookup"><span data-stu-id="790c2-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**ERROR\_DS\_EXISTS\_IN\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-560">8386 (0x20C2) </span><span class="sxs-lookup"><span data-stu-id="790c2-560">8386 (0x20C2)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-561">架構刪除失敗：在可能包含的屬性中使用屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-561">Schema deletion failed: attribute is used in may-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**\_ \_ 不存在的 DS 錯誤 \_ 可能 \_ 有**</span><span class="sxs-lookup"><span data-stu-id="790c2-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERROR\_DS\_NONEXISTENT\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-563">8387 (0x20C3) </span><span class="sxs-lookup"><span data-stu-id="790c2-563">8387 (0x20C3)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-564">架構更新失敗：可能包含的屬性不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-564">Schema update failed: attribute in may-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**\_ \_ 不存在的錯誤 DS \_ 必須 \_ 有**</span><span class="sxs-lookup"><span data-stu-id="790c2-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERROR\_DS\_NONEXISTENT\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-566">8388 (0x20C4) </span><span class="sxs-lookup"><span data-stu-id="790c2-566">8388 (0x20C4)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-567">架構更新失敗： in 必須包含的屬性不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-567">Schema update failed: attribute in must-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**錯誤 \_ DS \_ AUX \_ CLS \_ 測試 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR\_DS\_AUX\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-569">8389 (0x20C5) </span><span class="sxs-lookup"><span data-stu-id="790c2-569">8389 (0x20C5)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-570">架構更新失敗： aux 類別清單中的類別不存在或不是輔助類別。</span><span class="sxs-lookup"><span data-stu-id="790c2-570">Schema update failed: class in aux-class list does not exist or is not an auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**錯誤 \_ DS 不 \_ 存在 \_ POSS \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="790c2-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR\_DS\_NONEXISTENT\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-572">8390 (0x20C6) </span><span class="sxs-lookup"><span data-stu-id="790c2-572">8390 (0x20C6)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-573">架構更新失敗： poss-superiors 中的類別不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-573">Schema update failed: class in poss-superiors does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**錯誤 \_ DS \_ 子 \_ CLS \_ 測試 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR\_DS\_SUB\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-575">8391 (0x20C7) </span><span class="sxs-lookup"><span data-stu-id="790c2-575">8391 (0x20C7)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-576">架構更新失敗： subclassof 清單中的類別不存在或無法滿足階層規則。</span><span class="sxs-lookup"><span data-stu-id="790c2-576">Schema update failed: class in subclassof list does not exist or does not satisfy hierarchy rules.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**錯誤 \_ DS 錯誤的 \_ \_ RDN \_ ATT \_ 識別碼 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="790c2-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR\_DS\_BAD\_RDN\_ATT\_ID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-578">8392 (0x20C8) </span><span class="sxs-lookup"><span data-stu-id="790c2-578">8392 (0x20C8)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-579">架構更新失敗： Rdn-Att 識別碼的語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-579">Schema update failed: Rdn-Att-Id has wrong syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**\_ \_ \_ \_ AUX \_ CLS 中存在錯誤 DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERROR\_DS\_EXISTS\_IN\_AUX\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-581">8393 (0x20C9) </span><span class="sxs-lookup"><span data-stu-id="790c2-581">8393 (0x20C9)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-582">架構刪除失敗：類別會當做輔助類別使用。</span><span class="sxs-lookup"><span data-stu-id="790c2-582">Schema deletion failed: class is used as auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**錯誤 \_ DS \_ 存在 \_ 于 \_ SUB \_ CLS 中**</span><span class="sxs-lookup"><span data-stu-id="790c2-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERROR\_DS\_EXISTS\_IN\_SUB\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-584">8394 (0x20CA) </span><span class="sxs-lookup"><span data-stu-id="790c2-584">8394 (0x20CA)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-585">架構刪除失敗：類別用做為子類別。</span><span class="sxs-lookup"><span data-stu-id="790c2-585">Schema deletion failed: class is used as sub class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**\_ \_ \_ \_ POSS \_ SUP 中有錯誤 DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERROR\_DS\_EXISTS\_IN\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-587">8395 (0x20CB) </span><span class="sxs-lookup"><span data-stu-id="790c2-587">8395 (0x20CB)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-588">架構刪除失敗：類別用來做為 poss 高階。</span><span class="sxs-lookup"><span data-stu-id="790c2-588">Schema deletion failed: class is used as poss superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**錯誤 \_ DS \_ RECALCSCHEMA \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR\_DS\_RECALCSCHEMA\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-590">8396 (0x20CC) </span><span class="sxs-lookup"><span data-stu-id="790c2-590">8396 (0x20CC)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-591">重新計算驗證快取時架構更新失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-591">Schema update failed in recalculating validation cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**錯誤 \_ DS \_ 樹 \_ 刪除 \_ 未 \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="790c2-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR\_DS\_TREE\_DELETE\_NOT\_FINISHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-593">8397 (0x20CD) </span><span class="sxs-lookup"><span data-stu-id="790c2-593">8397 (0x20CD)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-594">未完成刪除樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="790c2-594">The tree deletion is not finished.</span></span> <span data-ttu-id="790c2-595">您必須重新建立要求，才能繼續刪除樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="790c2-595">The request must be made again to continue deleting the tree.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**錯誤 \_ DS \_ 無法 \_ 刪除**</span><span class="sxs-lookup"><span data-stu-id="790c2-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR\_DS\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-597">8398 (0x20CE) </span><span class="sxs-lookup"><span data-stu-id="790c2-597">8398 (0x20CE)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-598">無法執行要求的刪除操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-598">The requested delete operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**錯誤 \_ DS \_ ATT \_ 架構 \_ 要求 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="790c2-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-600">8399 (0x20CF) </span><span class="sxs-lookup"><span data-stu-id="790c2-600">8399 (0x20CF)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-601">無法讀取架構記錄的管理類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-601">Cannot read the governs class identifier for the schema record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**錯誤 \_ DS \_ 錯誤 \_ ATT \_ 架構 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="790c2-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR\_DS\_BAD\_ATT\_SCHEMA\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-603">8400 (0x20D0) </span><span class="sxs-lookup"><span data-stu-id="790c2-603">8400 (0x20D0)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-604">屬性架構的語法不正確。</span><span class="sxs-lookup"><span data-stu-id="790c2-604">The attribute schema has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**錯誤 DS 無法快取 \_ \_ \_ \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="790c2-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR\_DS\_CANT\_CACHE\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-606">8401 (0x20D1) </span><span class="sxs-lookup"><span data-stu-id="790c2-606">8401 (0x20D1)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-607">無法快取屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-607">The attribute could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**錯誤 DS 無法快取 \_ \_ \_ \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="790c2-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR\_DS\_CANT\_CACHE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-609">8402 (0x20D2) </span><span class="sxs-lookup"><span data-stu-id="790c2-609">8402 (0x20D2)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-610">無法快取類別。</span><span class="sxs-lookup"><span data-stu-id="790c2-610">The class could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**錯誤 \_ DS \_ 無法 \_ 移除 \_ ATT 快取 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_ATT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-612">8403 (0x20D3) </span><span class="sxs-lookup"><span data-stu-id="790c2-612">8403 (0x20D3)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-613">無法從快取中移除屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-613">The attribute could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**錯誤 \_ DS \_ 無法 \_ 移除 \_ 類別快取 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_CLASS\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-615">8404 (0x20D4) </span><span class="sxs-lookup"><span data-stu-id="790c2-615">8404 (0x20D4)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-616">無法從快取中移除類別。</span><span class="sxs-lookup"><span data-stu-id="790c2-616">The class could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ DN**</span><span class="sxs-lookup"><span data-stu-id="790c2-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR\_DS\_CANT\_RETRIEVE\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-618">8405 (0x20D5) </span><span class="sxs-lookup"><span data-stu-id="790c2-618">8405 (0x20D5)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-619">無法讀取分辨名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-619">The distinguished name attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**錯誤 \_ DS \_ 遺失 \_ SUPREF**</span><span class="sxs-lookup"><span data-stu-id="790c2-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR\_DS\_MISSING\_SUPREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-621">8406 (0x20D6) </span><span class="sxs-lookup"><span data-stu-id="790c2-621">8406 (0x20D6)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-622">尚未為目錄服務設定上層參照。</span><span class="sxs-lookup"><span data-stu-id="790c2-622">No superior reference has been configured for the directory service.</span></span> <span data-ttu-id="790c2-623">因此，目錄服務無法對這個樹系外的物件發出參考。</span><span class="sxs-lookup"><span data-stu-id="790c2-623">The directory service is therefore unable to issue referrals to objects outside this forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ 實例**</span><span class="sxs-lookup"><span data-stu-id="790c2-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR\_DS\_CANT\_RETRIEVE\_INSTANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-625">8407 (0x20D7) </span><span class="sxs-lookup"><span data-stu-id="790c2-625">8407 (0x20D7)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-626">無法取出實例型別屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-626">The instance type attribute could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**錯誤 \_ DS 程式 \_ 代碼不 \_ 一致**</span><span class="sxs-lookup"><span data-stu-id="790c2-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERROR\_DS\_CODE\_INCONSISTENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-628">8408 (0x20D8) </span><span class="sxs-lookup"><span data-stu-id="790c2-628">8408 (0x20D8)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-629">發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-629">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**錯誤 \_ DS \_ 資料庫 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**ERROR\_DS\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-631">8409 (0x20D9) </span><span class="sxs-lookup"><span data-stu-id="790c2-631">8409 (0x20D9)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-632">發生資料庫錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-632">A database error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**錯誤 \_ DS \_ GOVERNSID \_ 遺失**</span><span class="sxs-lookup"><span data-stu-id="790c2-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR\_DS\_GOVERNSID\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-634">8410 (0x20DA) </span><span class="sxs-lookup"><span data-stu-id="790c2-634">8410 (0x20DA)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-635">遺漏屬性 GOVERNSID。</span><span class="sxs-lookup"><span data-stu-id="790c2-635">The attribute GOVERNSID is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**錯誤 \_ DS \_ 遺失 \_ 預期的 \_ ATT**</span><span class="sxs-lookup"><span data-stu-id="790c2-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR\_DS\_MISSING\_EXPECTED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-637">8411 (0x20DB) </span><span class="sxs-lookup"><span data-stu-id="790c2-637">8411 (0x20DB)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-638">遺漏預期的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-638">An expected attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**\_DS \_ NCNAME \_ 缺少 \_ CR \_ REF 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR\_DS\_NCNAME\_MISSING\_CR\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-640">8412 (0x20DC) </span><span class="sxs-lookup"><span data-stu-id="790c2-640">8412 (0x20DC)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-641">指定的命名內容缺少交互參考。</span><span class="sxs-lookup"><span data-stu-id="790c2-641">The specified naming context is missing a cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**錯誤 \_ DS \_ 安全性 \_ 檢查 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**ERROR\_DS\_SECURITY\_CHECKING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-643">8413 (0x20DD) </span><span class="sxs-lookup"><span data-stu-id="790c2-643">8413 (0x20DD)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-644">發生安全性檢查錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-644">A security checking error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**\_ \_ \_ 未載入錯誤 DS \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="790c2-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERROR\_DS\_SCHEMA\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-646">8414 (0x20DE) </span><span class="sxs-lookup"><span data-stu-id="790c2-646">8414 (0x20DE)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-647">未載入架構。</span><span class="sxs-lookup"><span data-stu-id="790c2-647">The schema is not loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**錯誤 \_ DS \_ 架構 \_ 配置 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR\_DS\_SCHEMA\_ALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-649">8415 (0x20DF) </span><span class="sxs-lookup"><span data-stu-id="790c2-649">8415 (0x20DF)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-650">架構配置失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-650">Schema allocation failed.</span></span> <span data-ttu-id="790c2-651">請檢查電腦是否記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="790c2-651">Please check if the machine is running low on memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**錯誤 \_ DS \_ ATT \_ 架構 \_ 要求 \_ 語法**</span><span class="sxs-lookup"><span data-stu-id="790c2-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-653">8416 (0x20E0) </span><span class="sxs-lookup"><span data-stu-id="790c2-653">8416 (0x20E0)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-654">無法取得屬性架構的必要語法。</span><span class="sxs-lookup"><span data-stu-id="790c2-654">Failed to obtain the required syntax for the attribute schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**錯誤 \_ DS \_ GCVERIFY \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**ERROR\_DS\_GCVERIFY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-656">8417 (0x20E1) </span><span class="sxs-lookup"><span data-stu-id="790c2-656">8417 (0x20E1)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-657">通用類別目錄驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-657">The global catalog verification failed.</span></span> <span data-ttu-id="790c2-658">通用類別目錄無法使用，或不支援此操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-658">The global catalog is not available or does not support the operation.</span></span> <span data-ttu-id="790c2-659">目錄的某些部分目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="790c2-659">Some part of the directory is currently not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**\_DS \_ DRA 架構 \_ 錯誤 \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="790c2-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR\_DS\_DRA\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-661">8418 (0x20E2) </span><span class="sxs-lookup"><span data-stu-id="790c2-661">8418 (0x20E2)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-662">複寫作業失敗，因為相關伺服器之間的架構不相符。</span><span class="sxs-lookup"><span data-stu-id="790c2-662">The replication operation failed because of a schema mismatch between the servers involved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**錯誤 \_ DS \_ \_ 找不到 \_ DSA \_ OBJ**</span><span class="sxs-lookup"><span data-stu-id="790c2-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR\_DS\_CANT\_FIND\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-664">8419 (0x20E3) </span><span class="sxs-lookup"><span data-stu-id="790c2-664">8419 (0x20E3)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-665">找不到 DSA 物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-665">The DSA object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**錯誤 \_ DS \_ \_ 找不到 \_ 預期的 \_ NC**</span><span class="sxs-lookup"><span data-stu-id="790c2-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR\_DS\_CANT\_FIND\_EXPECTED\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-667">8420 (0x20E4) </span><span class="sxs-lookup"><span data-stu-id="790c2-667">8420 (0x20E4)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-668">找不到命名內容。</span><span class="sxs-lookup"><span data-stu-id="790c2-668">The naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**錯誤 \_ DS \_ 在快取 \_ 中找不到 \_ NC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR\_DS\_CANT\_FIND\_NC\_IN\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-670">8421 (0x20E5) </span><span class="sxs-lookup"><span data-stu-id="790c2-670">8421 (0x20E5)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-671">在快取中找不到命名內容。</span><span class="sxs-lookup"><span data-stu-id="790c2-671">The naming context could not be found in the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ 子系**</span><span class="sxs-lookup"><span data-stu-id="790c2-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR\_DS\_CANT\_RETRIEVE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-673">8422 (0x20E6) </span><span class="sxs-lookup"><span data-stu-id="790c2-673">8422 (0x20E6)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-674">無法取出子物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-674">The child object could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**錯誤 \_ DS \_ 安全性不 \_ 合法的 \_ 修改**</span><span class="sxs-lookup"><span data-stu-id="790c2-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR\_DS\_SECURITY\_ILLEGAL\_MODIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-676">8423 (0x20E7) </span><span class="sxs-lookup"><span data-stu-id="790c2-676">8423 (0x20E7)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-677">基於安全性考慮，不允許進行修改。</span><span class="sxs-lookup"><span data-stu-id="790c2-677">The modification was not permitted for security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**錯誤 \_ DS \_ 無法 \_ 取代 \_ 隱藏的 \_ REC**</span><span class="sxs-lookup"><span data-stu-id="790c2-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR\_DS\_CANT\_REPLACE\_HIDDEN\_REC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-679">8424 (0x20E8) </span><span class="sxs-lookup"><span data-stu-id="790c2-679">8424 (0x20E8)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-680">作業無法取代隱藏的記錄。</span><span class="sxs-lookup"><span data-stu-id="790c2-680">The operation cannot replace the hidden record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**錯誤 DS 錯誤的階層 \_ \_ \_ \_ 檔**</span><span class="sxs-lookup"><span data-stu-id="790c2-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERROR\_DS\_BAD\_HIERARCHY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-682">8425 (0x20E9) </span><span class="sxs-lookup"><span data-stu-id="790c2-682">8425 (0x20E9)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-683">階層檔案無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-683">The hierarchy file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**錯誤 \_ DS \_ 組建 \_ 階層 \_ 資料表 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR\_DS\_BUILD\_HIERARCHY\_TABLE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-685">8426 (0x20EA) </span><span class="sxs-lookup"><span data-stu-id="790c2-685">8426 (0x20EA)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-686">嘗試建立階層資料表失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-686">The attempt to build the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**\_缺少 DS \_ 設定 \_ 參數 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR\_DS\_CONFIG\_PARAM\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-688">8427 (0x20EB) </span><span class="sxs-lookup"><span data-stu-id="790c2-688">8427 (0x20EB)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-689">登錄中遺漏目錄設定參數。</span><span class="sxs-lookup"><span data-stu-id="790c2-689">The directory configuration parameter is missing from the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**錯誤 \_ DS \_ 計數 \_ AB \_ 索引 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR\_DS\_COUNTING\_AB\_INDICES\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-691">8428 (0x20EC) </span><span class="sxs-lookup"><span data-stu-id="790c2-691">8428 (0x20EC)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-692">嘗試計算通訊錄索引失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-692">The attempt to count the address book indices failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**錯誤 \_ DS \_ 階層 \_ 表 \_ MALLOC \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_MALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-694">8429 (0x20ED) </span><span class="sxs-lookup"><span data-stu-id="790c2-694">8429 (0x20ED)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-695">階層資料表的配置失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-695">The allocation of the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**錯誤 \_ DS \_ 內部 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR\_DS\_INTERNAL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-697">8430 (0x20EE) </span><span class="sxs-lookup"><span data-stu-id="790c2-697">8430 (0x20EE)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-698">目錄服務發生內部失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-698">The directory service encountered an internal failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**錯誤 \_ DS \_ 不明 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**ERROR\_DS\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-700">8431 (0x20EF) </span><span class="sxs-lookup"><span data-stu-id="790c2-700">8431 (0x20EF)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-701">目錄服務發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-701">The directory service encountered an unknown failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**錯誤 \_ DS \_ 根目錄 \_ 需要 \_ 類別 \_ TOP**</span><span class="sxs-lookup"><span data-stu-id="790c2-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERROR\_DS\_ROOT\_REQUIRES\_CLASS\_TOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-703">8432 (0x20F0) </span><span class="sxs-lookup"><span data-stu-id="790c2-703">8432 (0x20F0)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-704">根物件需要 ' top ' 的類別。</span><span class="sxs-lookup"><span data-stu-id="790c2-704">A root object requires a class of 'top'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**\_DS \_ 拒絕 \_ FSMO \_ 角色錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR\_DS\_REFUSING\_FSMO\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-706">8433 (0x20F1) </span><span class="sxs-lookup"><span data-stu-id="790c2-706">8433 (0x20F1)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-707">此目錄伺服器正在關機，無法取得新浮動單一主機操作角色的擁有權。</span><span class="sxs-lookup"><span data-stu-id="790c2-707">This directory server is shutting down, and cannot take ownership of new floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**錯誤 \_ DS \_ 遺失 \_ FSMO \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="790c2-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR\_DS\_MISSING\_FSMO\_SETTINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-709">8434 (0x20F2) </span><span class="sxs-lookup"><span data-stu-id="790c2-709">8434 (0x20F2)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-710">目錄服務遺失必要的設定資訊，而且無法判斷浮動單一主機作業角色的擁有權。</span><span class="sxs-lookup"><span data-stu-id="790c2-710">The directory service is missing mandatory configuration information, and is unable to determine the ownership of floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**錯誤 \_ DS \_ 無法 \_ \_ 時須交回 \_ 角色**</span><span class="sxs-lookup"><span data-stu-id="790c2-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR\_DS\_UNABLE\_TO\_SURRENDER\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-712">8435 (0x20F3) </span><span class="sxs-lookup"><span data-stu-id="790c2-712">8435 (0x20F3)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-713">目錄服務無法將一或多個浮動單一主機作業角色的擁有權轉移給其他伺服器。</span><span class="sxs-lookup"><span data-stu-id="790c2-713">The directory service was unable to transfer ownership of one or more floating single-master operation roles to other servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**錯誤 \_ DS \_ DRA \_ 泛型**</span><span class="sxs-lookup"><span data-stu-id="790c2-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR\_DS\_DRA\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-715">8436 (0x20F4) </span><span class="sxs-lookup"><span data-stu-id="790c2-715">8436 (0x20F4)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-716">複寫操作失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-716">The replication operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**\_DS \_ DRA 錯誤 \_ \_ 參數無效**</span><span class="sxs-lookup"><span data-stu-id="790c2-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR\_DS\_DRA\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-718">8437 (0x20F5) </span><span class="sxs-lookup"><span data-stu-id="790c2-718">8437 (0x20F5)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-719">為此複寫作業指定了不正確參數。</span><span class="sxs-lookup"><span data-stu-id="790c2-719">An invalid parameter was specified for this replication operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**\_DS \_ DRA \_ 忙碌時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR\_DS\_DRA\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-721">8438 (0x20F6) </span><span class="sxs-lookup"><span data-stu-id="790c2-721">8438 (0x20F6)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-722">目錄服務太忙碌，無法完成複寫作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-722">The directory service is too busy to complete the replication operation at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**\_DS \_ DRA DRA \_ 錯誤 \_ DN**</span><span class="sxs-lookup"><span data-stu-id="790c2-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR\_DS\_DRA\_BAD\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-724">8439 (0x20F7) </span><span class="sxs-lookup"><span data-stu-id="790c2-724">8439 (0x20F7)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-725">為此複寫作業指定的辨別名稱無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-725">The distinguished name specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**\_DS \_ DRA DRA \_ 錯誤 \_ NC**</span><span class="sxs-lookup"><span data-stu-id="790c2-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR\_DS\_DRA\_BAD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-727">8440 (0x20F8) </span><span class="sxs-lookup"><span data-stu-id="790c2-727">8440 (0x20F8)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-728">為此複寫作業指定的命名內容無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-728">The naming context specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**錯誤 \_ DS \_ DRA \_ DN \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="790c2-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR\_DS\_DRA\_DN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-730">8441 (0x20F9) </span><span class="sxs-lookup"><span data-stu-id="790c2-730">8441 (0x20F9)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-731">為此複寫作業指定的辨別名稱已存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-731">The distinguished name specified for this replication operation already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**錯誤 \_ DS \_ DRA \_ 內部 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**ERROR\_DS\_DRA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-733">8442 (0x20FA) </span><span class="sxs-lookup"><span data-stu-id="790c2-733">8442 (0x20FA)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-734">複寫系統發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-734">The replication system encountered an internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**\_DS \_ DRA DRA \_ 不一致的 \_ DIT**</span><span class="sxs-lookup"><span data-stu-id="790c2-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR\_DS\_DRA\_INCONSISTENT\_DIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-736">8443 (0x20FB) </span><span class="sxs-lookup"><span data-stu-id="790c2-736">8443 (0x20FB)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-737">複寫作業發生資料庫不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="790c2-737">The replication operation encountered a database inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**錯誤 \_ DS \_ DRA \_ 連接 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR\_DS\_DRA\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-739">8444 (0x20FC) </span><span class="sxs-lookup"><span data-stu-id="790c2-739">8444 (0x20FC)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-740">無法連絡為此複寫作業指定的伺服器。</span><span class="sxs-lookup"><span data-stu-id="790c2-740">The server specified for this replication operation could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**\_DS \_ DRA DRA 錯誤的 \_ \_ 實例 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="790c2-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR\_DS\_DRA\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-742">8445 (0x20FD) </span><span class="sxs-lookup"><span data-stu-id="790c2-742">8445 (0x20FD)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-743">複寫作業遇到具有無效實例類型的物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-743">The replication operation encountered an object with an invalid instance type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**\_ \_ \_ \_ 記憶體中的 DS DRA \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR\_DS\_DRA\_OUT\_OF\_MEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-745">8446 (0x20FE) </span><span class="sxs-lookup"><span data-stu-id="790c2-745">8446 (0x20FE)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-746">複寫操作無法配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="790c2-746">The replication operation failed to allocate memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**錯誤 \_ DS \_ DRA \_ 郵件 \_ 問題**</span><span class="sxs-lookup"><span data-stu-id="790c2-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR\_DS\_DRA\_MAIL\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-748">8447 (0x20FF) </span><span class="sxs-lookup"><span data-stu-id="790c2-748">8447 (0x20FF)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-749">複寫作業在郵件系統發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-749">The replication operation encountered an error with the mail system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**錯誤 \_ DS \_ DRA \_ 參考 \_ 已 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="790c2-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERROR\_DS\_DRA\_REF\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-751">8448 (0x2100) </span><span class="sxs-lookup"><span data-stu-id="790c2-751">8448 (0x2100)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-752">目標伺服器的複寫參考資訊已存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-752">The replication reference information for the target server already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**\_ \_ \_ \_ \_ 找不到 DS DRA 參考錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR\_DS\_DRA\_REF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-754">8449 (0x2101) </span><span class="sxs-lookup"><span data-stu-id="790c2-754">8449 (0x2101)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-755">目標伺服器的複寫參考資訊不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-755">The replication reference information for the target server does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR \_ DS \_ DRA \_ OBJ \_ 是 \_ REP \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="790c2-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR\_DS\_DRA\_OBJ\_IS\_REP\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-757">8450 (0x2102) </span><span class="sxs-lookup"><span data-stu-id="790c2-757">8450 (0x2102)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-758">因為命名內容已複寫到另一部伺服器，所以無法移除。</span><span class="sxs-lookup"><span data-stu-id="790c2-758">The naming context cannot be removed because it is replicated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**錯誤 \_ DS \_ DRA \_ 資料庫 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**ERROR\_DS\_DRA\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-760">8451 (0x2103) </span><span class="sxs-lookup"><span data-stu-id="790c2-760">8451 (0x2103)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-761">複寫作業發生資料庫錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-761">The replication operation encountered a database error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**錯誤 \_ DS \_ DRA \_ 沒有 \_ 複本**</span><span class="sxs-lookup"><span data-stu-id="790c2-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR\_DS\_DRA\_NO\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-763">8452 (0x2104) </span><span class="sxs-lookup"><span data-stu-id="790c2-763">8452 (0x2104)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-764">命名內容正在移除，或未從指定的伺服器複寫。</span><span class="sxs-lookup"><span data-stu-id="790c2-764">The naming context is in the process of being removed or is not replicated from the specified server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**\_拒絕 DS \_ DRA \_ 存取 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR\_DS\_DRA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-766">8453 (0x2105) </span><span class="sxs-lookup"><span data-stu-id="790c2-766">8453 (0x2105)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-767">複寫存取被拒。</span><span class="sxs-lookup"><span data-stu-id="790c2-767">Replication access was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**\_ \_ \_ 不支援的 DS DRA 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR\_DS\_DRA\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-769">8454 (0x2106) </span><span class="sxs-lookup"><span data-stu-id="790c2-769">8454 (0x2106)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-770">此版本的目錄服務不支援要求的操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-770">The requested operation is not supported by this version of the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**錯誤 \_ DS \_ DRA \_ RPC 已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="790c2-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR\_DS\_DRA\_RPC\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-772">8455 (0x2107) </span><span class="sxs-lookup"><span data-stu-id="790c2-772">8455 (0x2107)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-773">複寫遠端程序呼叫已取消。</span><span class="sxs-lookup"><span data-stu-id="790c2-773">The replication remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**\_ \_ \_ 停用 DS DRA 來源 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERROR\_DS\_DRA\_SOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-775">8456 (0x2108) </span><span class="sxs-lookup"><span data-stu-id="790c2-775">8456 (0x2108)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-776">來源伺服器目前拒絕複寫要求。</span><span class="sxs-lookup"><span data-stu-id="790c2-776">The source server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**\_ \_ \_ 停用 DS DRA 接收 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR\_DS\_DRA\_SINK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-778">8457 (0x2109) </span><span class="sxs-lookup"><span data-stu-id="790c2-778">8457 (0x2109)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-779">目的地伺服器目前拒絕複寫要求。</span><span class="sxs-lookup"><span data-stu-id="790c2-779">The destination server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**\_DS \_ DRA \_ 名稱 \_ 衝突錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERROR\_DS\_DRA\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-781">8458 (0x210A) </span><span class="sxs-lookup"><span data-stu-id="790c2-781">8458 (0x210A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-782">複寫作業失敗，因為物件名稱發生衝突。</span><span class="sxs-lookup"><span data-stu-id="790c2-782">The replication operation failed due to a collision of object names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**\_ \_ \_ 重新安裝 DS DRA 來源 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR\_DS\_DRA\_SOURCE\_REINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-784">8459 (0x210B) </span><span class="sxs-lookup"><span data-stu-id="790c2-784">8459 (0x210B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-785">已重新安裝複寫來源。</span><span class="sxs-lookup"><span data-stu-id="790c2-785">The replication source has been reinstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**錯誤 \_ DS \_ DRA \_ 遺失 \_ 父系**</span><span class="sxs-lookup"><span data-stu-id="790c2-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR\_DS\_DRA\_MISSING\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-787">8460 (0x210C) </span><span class="sxs-lookup"><span data-stu-id="790c2-787">8460 (0x210C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-788">複寫作業失敗，因為遺漏必要的父物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-788">The replication operation failed because a required parent object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**\_DS \_ DRA DRA \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR\_DS\_DRA\_PREEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-790">8461 (0x210D) </span><span class="sxs-lookup"><span data-stu-id="790c2-790">8461 (0x210D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-791">複寫作業已被佔用。</span><span class="sxs-lookup"><span data-stu-id="790c2-791">The replication operation was preempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**\_DS \_ DRA \_ 放棄 \_ 同步錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR\_DS\_DRA\_ABANDON\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-793">8462 (0x210E) </span><span class="sxs-lookup"><span data-stu-id="790c2-793">8462 (0x210E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-794">因為缺少更新，所以已放棄複寫同步處理嘗試。</span><span class="sxs-lookup"><span data-stu-id="790c2-794">The replication synchronization attempt was abandoned because of a lack of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**\_DS \_ DRA \_ 關機錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR\_DS\_DRA\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-796">8463 (0x210F) </span><span class="sxs-lookup"><span data-stu-id="790c2-796">8463 (0x210F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-797">複寫作業已終止，因為系統正在關閉。</span><span class="sxs-lookup"><span data-stu-id="790c2-797">The replication operation was terminated because the system is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**\_DS \_ DRA \_ 不相容的 \_ 部分 \_ 集合錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR\_DS\_DRA\_INCOMPATIBLE\_PARTIAL\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-799">8464 (0x2110) </span><span class="sxs-lookup"><span data-stu-id="790c2-799">8464 (0x2110)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-800">因為目的地 DC 目前正在等候從來源同步處理新的部分屬性，所以同步處理嘗試失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-800">Synchronization attempt failed because the destination DC is currently waiting to synchronize new partial attributes from source.</span></span> <span data-ttu-id="790c2-801">如果最近的架構變更修改了部分屬性集，這就是正常情況。</span><span class="sxs-lookup"><span data-stu-id="790c2-801">This condition is normal if a recent schema change modified the partial attribute set.</span></span> <span data-ttu-id="790c2-802">目的地部分屬性集不是來源部分屬性集的子集。</span><span class="sxs-lookup"><span data-stu-id="790c2-802">The destination partial attribute set is not a subset of source partial attribute set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**錯誤 \_ DS \_ DRA \_ 來源 \_ 為 \_ 部分 \_ 複本**</span><span class="sxs-lookup"><span data-stu-id="790c2-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERROR\_DS\_DRA\_SOURCE\_IS\_PARTIAL\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-804">8465 (0x2111) </span><span class="sxs-lookup"><span data-stu-id="790c2-804">8465 (0x2111)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-805">複寫同步處理嘗試失敗，因為主要複本嘗試從部分複本進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="790c2-805">The replication synchronization attempt failed because a master replica attempted to sync from a partial replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**錯誤 \_ DS \_ DRA \_ EXTN \_ 連接 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR\_DS\_DRA\_EXTN\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-807">8466 (0x2112) </span><span class="sxs-lookup"><span data-stu-id="790c2-807">8466 (0x2112)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-808">已連線到為此複寫作業指定的伺服器，但該伺服器無法連線到完成此作業所需的其他伺服器。</span><span class="sxs-lookup"><span data-stu-id="790c2-808">The server specified for this replication operation was contacted, but that server was unable to contact an additional server needed to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**錯誤 \_ DS \_ 安裝 \_ 架構 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="790c2-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR\_DS\_INSTALL\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-810">8467 (0x2113) </span><span class="sxs-lookup"><span data-stu-id="790c2-810">8467 (0x2113)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-811">來源樹系的目錄服務架構版本與這部電腦上的目錄服務版本不相容。</span><span class="sxs-lookup"><span data-stu-id="790c2-811">The version of the directory service schema of the source forest is not compatible with the version of directory service on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**\_DS \_ DUP \_ 連結 \_ 識別碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERROR\_DS\_DUP\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-813">8468 (0x2114) </span><span class="sxs-lookup"><span data-stu-id="790c2-813">8468 (0x2114)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-814">架構更新失敗：已有具有相同連結識別碼的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-814">Schema update failed: An attribute with the same link identifier already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**錯誤 \_ 的 \_ DS \_ 名稱 \_ 解析錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR\_DS\_NAME\_ERROR\_RESOLVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-816">8469 (0x2115) </span><span class="sxs-lookup"><span data-stu-id="790c2-816">8469 (0x2115)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-817">名稱轉譯：一般處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-817">Name translation: Generic processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**\_ \_ \_ \_ \_ 找不到 DS 名稱錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-819">8470 (0x2116) </span><span class="sxs-lookup"><span data-stu-id="790c2-819">8470 (0x2116)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-820">名稱轉譯：找不到名稱或許可權不足，無法查看名稱。</span><span class="sxs-lookup"><span data-stu-id="790c2-820">Name translation: Could not find the name or insufficient right to see name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 不是 \_ 唯一的**</span><span class="sxs-lookup"><span data-stu-id="790c2-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-822">8471 (0x2117) </span><span class="sxs-lookup"><span data-stu-id="790c2-822">8471 (0x2117)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-823">名稱轉譯：輸入名稱對應至一個以上的輸出名稱。</span><span class="sxs-lookup"><span data-stu-id="790c2-823">Name translation: Input name mapped to more than one output name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 沒有 \_ 對應**</span><span class="sxs-lookup"><span data-stu-id="790c2-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-825">8472 (0x2118) </span><span class="sxs-lookup"><span data-stu-id="790c2-825">8472 (0x2118)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-826">名稱轉譯：找到輸入名稱，但沒有相關聯的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="790c2-826">Name translation: Input name found, but not the associated output format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 網域 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERROR\_DS\_NAME\_ERROR\_DOMAIN\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-828">8473 (0x2119) </span><span class="sxs-lookup"><span data-stu-id="790c2-828">8473 (0x2119)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-829">名稱轉譯：無法完全解析，只找到網域。</span><span class="sxs-lookup"><span data-stu-id="790c2-829">Name translation: Unable to resolve completely, only the domain was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 沒有 \_ 語法 \_ 對應**</span><span class="sxs-lookup"><span data-stu-id="790c2-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_SYNTACTICAL\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-831">8474 (0x211A) </span><span class="sxs-lookup"><span data-stu-id="790c2-831">8474 (0x211A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-832">名稱轉譯：無法在用戶端上執行純粹的語法對應，而不需要連線到網路。</span><span class="sxs-lookup"><span data-stu-id="790c2-832">Name translation: Unable to perform purely syntactical mapping at the client without going out to the wire.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**錯誤 \_ DS \_ 結構 \_ ATT \_ MOD**</span><span class="sxs-lookup"><span data-stu-id="790c2-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR\_DS\_CONSTRUCTED\_ATT\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-834">8475 (0x211B) </span><span class="sxs-lookup"><span data-stu-id="790c2-834">8475 (0x211B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-835">不允許修改已建立的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-835">Modification of a constructed attribute is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**錯誤 \_ DS 錯誤的 \_ \_ OM \_ OBJ \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="790c2-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR\_DS\_WRONG\_OM\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-837">8476 (0x211C) </span><span class="sxs-lookup"><span data-stu-id="790c2-837">8476 (0x211C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-838">針對具有指定語法的屬性，指定的 OM 物件類別不正確。</span><span class="sxs-lookup"><span data-stu-id="790c2-838">The OM-Object-Class specified is incorrect for an attribute with the specified syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**錯誤 \_ DS \_ DRA \_ 複寫 \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="790c2-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR\_DS\_DRA\_REPL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-840">8477 (0x211D) </span><span class="sxs-lookup"><span data-stu-id="790c2-840">8477 (0x211D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-841">複寫要求已公佈;正在等候回復。</span><span class="sxs-lookup"><span data-stu-id="790c2-841">The replication request has been posted; waiting for reply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**\_需要 ERROR DS \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR\_DS\_DS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-843">8478 (0x211E) </span><span class="sxs-lookup"><span data-stu-id="790c2-843">8478 (0x211E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-844">要求的作業需要目錄服務，而且沒有可用的。</span><span class="sxs-lookup"><span data-stu-id="790c2-844">The requested operation requires a directory service, and none was available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**錯誤 \_ DS \_ 不正確 \_ LDAP \_ 顯示 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="790c2-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR\_DS\_INVALID\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-846">8479 (0x211F) </span><span class="sxs-lookup"><span data-stu-id="790c2-846">8479 (0x211F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-847">類別或屬性的 LDAP 顯示名稱包含非 ASCII 字元。</span><span class="sxs-lookup"><span data-stu-id="790c2-847">The LDAP display name of the class or attribute contains non-ASCII characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**錯誤 \_ DS \_ 非 \_ 基底 \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="790c2-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR\_DS\_NON\_BASE\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-849">8480 (0x2120) </span><span class="sxs-lookup"><span data-stu-id="790c2-849">8480 (0x2120)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-850">只有基底搜尋支援要求的搜尋作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-850">The requested search operation is only supported for base searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ ATTS**</span><span class="sxs-lookup"><span data-stu-id="790c2-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR\_DS\_CANT\_RETRIEVE\_ATTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-852">8481 (0x2121) </span><span class="sxs-lookup"><span data-stu-id="790c2-852">8481 (0x2121)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-853">搜尋無法從資料庫取出屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-853">The search failed to retrieve attributes from the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**\_ \_ \_ 沒有連結的 DS BACKLINK 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR\_DS\_BACKLINK\_WITHOUT\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-855">8482 (0x2122) </span><span class="sxs-lookup"><span data-stu-id="790c2-855">8482 (0x2122)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-856">架構更新作業嘗試加入沒有對應轉寄連結的反向連結屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-856">The schema update operation tried to add a backward link attribute that has no corresponding forward link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**\_DS \_ EPOCH 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR\_DS\_EPOCH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-858">8483 (0x2123) </span><span class="sxs-lookup"><span data-stu-id="790c2-858">8483 (0x2123)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-859">跨網域移動的來源和目的地不同意物件的 epoch 號碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-859">Source and destination of a cross-domain move do not agree on the object's epoch number.</span></span> <span data-ttu-id="790c2-860">來源或目的地都沒有最新版本的物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-860">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**\_DS \_ SRC \_ 名稱 \_ 不符錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR\_DS\_SRC\_NAME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-862">8484 (0x2124) </span><span class="sxs-lookup"><span data-stu-id="790c2-862">8484 (0x2124)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-863">跨網域移動的來源和目的地不同意物件的目前名稱。</span><span class="sxs-lookup"><span data-stu-id="790c2-863">Source and destination of a cross-domain move do not agree on the object's current name.</span></span> <span data-ttu-id="790c2-864">來源或目的地都沒有最新版本的物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-864">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**錯誤 \_ DS \_ SRC \_ 和 \_ DST \_ NC \_ 相同**</span><span class="sxs-lookup"><span data-stu-id="790c2-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR\_DS\_SRC\_AND\_DST\_NC\_IDENTICAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-866">8485 (0x2125) </span><span class="sxs-lookup"><span data-stu-id="790c2-866">8485 (0x2125)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-867">跨網域移動作業的來源和目的地相同。</span><span class="sxs-lookup"><span data-stu-id="790c2-867">Source and destination for the cross-domain move operation are identical.</span></span> <span data-ttu-id="790c2-868">呼叫端應該使用本機移動作業，而不是跨網域的移動操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-868">Caller should use local move operation instead of cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**錯誤 \_ DS \_ DST \_ NC \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="790c2-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR\_DS\_DST\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-870">8486 (0x2126) </span><span class="sxs-lookup"><span data-stu-id="790c2-870">8486 (0x2126)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-871">樹系中的命名內容不會有跨網域移動的來源和目的地。</span><span class="sxs-lookup"><span data-stu-id="790c2-871">Source and destination for a cross-domain move are not in agreement on the naming contexts in the forest.</span></span> <span data-ttu-id="790c2-872">來源或目的地都沒有最新版本的分割區容器。</span><span class="sxs-lookup"><span data-stu-id="790c2-872">Either source or destination does not have the latest version of the Partitions container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**\_ \_ \_ \_ 適用于 \_ DST \_ NC 的錯誤 DS 未 AUTHORITIVE**</span><span class="sxs-lookup"><span data-stu-id="790c2-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR\_DS\_NOT\_AUTHORITIVE\_FOR\_DST\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-874">8487 (0x2127) </span><span class="sxs-lookup"><span data-stu-id="790c2-874">8487 (0x2127)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-875">跨網域移動的目的地不是目的地命名內容的授權。</span><span class="sxs-lookup"><span data-stu-id="790c2-875">Destination of a cross-domain move is not authoritative for the destination naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**錯誤 \_ DS \_ SRC \_ GUID \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="790c2-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR\_DS\_SRC\_GUID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-877">8488 (0x2128) </span><span class="sxs-lookup"><span data-stu-id="790c2-877">8488 (0x2128)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-878">跨網域移動的來源和目的地不同意來源物件的身分識別。</span><span class="sxs-lookup"><span data-stu-id="790c2-878">Source and destination of a cross-domain move do not agree on the identity of the source object.</span></span> <span data-ttu-id="790c2-879">來源或目的地都沒有最新版本的來源物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-879">Either source or destination does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 已刪除的 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR\_DS\_CANT\_MOVE\_DELETED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-881">8489 (0x2129) </span><span class="sxs-lookup"><span data-stu-id="790c2-881">8489 (0x2129)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-882">目的地伺服器已知道要將跨網域移動的物件刪除。</span><span class="sxs-lookup"><span data-stu-id="790c2-882">Object being moved across-domains is already known to be deleted by the destination server.</span></span> <span data-ttu-id="790c2-883">來源伺服器沒有最新版本的來源物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-883">The source server does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**\_ \_ \_ \_ 進行中的 DS PDC 操作時發生錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR\_DS\_PDC\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-885">8490 (0x212A) </span><span class="sxs-lookup"><span data-stu-id="790c2-885">8490 (0x212A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-886">另一項需要獨佔存取 PDC FSMO 的作業已在進行中。</span><span class="sxs-lookup"><span data-stu-id="790c2-886">Another operation which requires exclusive access to the PDC FSMO is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**錯誤 \_ DS \_ 跨 \_ 網域 \_ 清除 \_ REQD**</span><span class="sxs-lookup"><span data-stu-id="790c2-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR\_DS\_CROSS\_DOMAIN\_CLEANUP\_REQD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-888">8491 (0x212B) </span><span class="sxs-lookup"><span data-stu-id="790c2-888">8491 (0x212B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-889">跨網域移動作業失敗，因此移動物件的兩個版本都存在，也就是來源和目的地網域中的每一個。</span><span class="sxs-lookup"><span data-stu-id="790c2-889">A cross-domain move operation failed such that two versions of the moved object exist - one each in the source and destination domains.</span></span> <span data-ttu-id="790c2-890">必須移除目的地物件，才能將系統還原成一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="790c2-890">The destination object needs to be removed to restore the system to a consistent state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**錯誤 \_ DS 不 \_ 合法的 \_ XDOM \_ 移動 \_ 操作**</span><span class="sxs-lookup"><span data-stu-id="790c2-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR\_DS\_ILLEGAL\_XDOM\_MOVE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-892">8492 (0x212C) </span><span class="sxs-lookup"><span data-stu-id="790c2-892">8492 (0x212C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-893">因為不允許此類別的跨網域移動，或物件具有某些特殊特性，例如： trust 帳戶或限制 RID （防止其移動），所以這個物件可能不會跨網域界限移動。</span><span class="sxs-lookup"><span data-stu-id="790c2-893">This object may not be moved across domain boundaries either because cross-domain moves for this class are disallowed, or the object has some special characteristics, e.g.: trust account or restricted RID, which prevent its move.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**\_ \_ \_ 使用 \_ 帳戶 \_ 群組 \_ MEMBERSHPS 時發生錯誤 DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR\_DS\_CANT\_WITH\_ACCT\_GROUP\_MEMBERSHPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-895">8493 (0x212D) </span><span class="sxs-lookup"><span data-stu-id="790c2-895">8493 (0x212D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-896">一旦移動後，就無法移動具有網域界限成員資格的物件，這會違反帳戶群組的成員資格條件。</span><span class="sxs-lookup"><span data-stu-id="790c2-896">Can't move objects with memberships across domain boundaries as once moved, this would violate the membership conditions of the account group.</span></span> <span data-ttu-id="790c2-897">請從任何帳戶群組成員資格中移除該物件，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="790c2-897">Remove the object from any account group memberships and retry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**錯誤 \_ DS \_ NC \_ 必須 \_ 有 \_ NC \_ 父系**</span><span class="sxs-lookup"><span data-stu-id="790c2-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERROR\_DS\_NC\_MUST\_HAVE\_NC\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-899">8494 (0x212E) </span><span class="sxs-lookup"><span data-stu-id="790c2-899">8494 (0x212E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-900">命名內容標頭必須是另一個命名內容標頭的直屬子系，而非內部節點的子系。</span><span class="sxs-lookup"><span data-stu-id="790c2-900">A naming context head must be the immediate child of another naming context head, not of an interior node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**\_ \_ \_ 無法驗證 DS CR \_ 的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-902">8495 (0x212F) </span><span class="sxs-lookup"><span data-stu-id="790c2-902">8495 (0x212F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-903">目錄無法驗證建議的命名內容名稱，因為它不會在建議的命名內容上方保留命名內容的複本。</span><span class="sxs-lookup"><span data-stu-id="790c2-903">The directory cannot validate the proposed naming context name because it does not hold a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="790c2-904">請確定網網域命名主機角色是由設定為通用類別目錄伺服器的伺服器所持有，而且伺服器與複寫協力電腦是最新的。</span><span class="sxs-lookup"><span data-stu-id="790c2-904">Please ensure that the domain naming master role is held by a server that is configured as a global catalog server, and that the server is up to date with its replication partners.</span></span> <span data-ttu-id="790c2-905"> (僅適用于 Windows 2000 網網域命名主機。 ) </span><span class="sxs-lookup"><span data-stu-id="790c2-905">(Applies only to Windows 2000 Domain Naming masters.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**錯誤 \_ DS \_ DST \_ 網域 \_ 不是 \_ 原生**</span><span class="sxs-lookup"><span data-stu-id="790c2-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR\_DS\_DST\_DOMAIN\_NOT\_NATIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-907">8496 (0x2130) </span><span class="sxs-lookup"><span data-stu-id="790c2-907">8496 (0x2130)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-908">目的地網域必須處於原生模式。</span><span class="sxs-lookup"><span data-stu-id="790c2-908">Destination domain must be in native mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**錯誤 \_ DS \_ 遺失 \_ 基礎結構 \_ 容器**</span><span class="sxs-lookup"><span data-stu-id="790c2-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR\_DS\_MISSING\_INFRASTRUCTURE\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-910">8497 (0x2131) </span><span class="sxs-lookup"><span data-stu-id="790c2-910">8497 (0x2131)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-911">無法執行作業，因為伺服器上沒有感興趣網域中的基礎結構容器。</span><span class="sxs-lookup"><span data-stu-id="790c2-911">The operation cannot be performed because the server does not have an infrastructure container in the domain of interest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 帳戶 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="790c2-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR\_DS\_CANT\_MOVE\_ACCOUNT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-913">8498 (0x2132) </span><span class="sxs-lookup"><span data-stu-id="790c2-913">8498 (0x2132)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-914">不允許跨網域移動非空白的帳戶群組。</span><span class="sxs-lookup"><span data-stu-id="790c2-914">Cross-domain move of non-empty account groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 資源 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="790c2-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR\_DS\_CANT\_MOVE\_RESOURCE\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-916">8499 (0x2133) </span><span class="sxs-lookup"><span data-stu-id="790c2-916">8499 (0x2133)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-917">不允許跨網域移動非空白的資源群組。</span><span class="sxs-lookup"><span data-stu-id="790c2-917">Cross-domain move of non-empty resource groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**錯誤 \_ DS \_ 不正確 \_ 搜尋 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="790c2-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-919">8500 (0x2134) </span><span class="sxs-lookup"><span data-stu-id="790c2-919">8500 (0x2134)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-920">屬性的搜尋旗標無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-920">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="790c2-921">ANR 位只適用于 Unicode 或 Teletex 字串的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-921">The ANR bit is valid only on attributes of Unicode or Teletex strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**錯誤 \_ DS \_ 未 \_ 在 \_ \_ NC 上 \_ 刪除任何樹狀結構**</span><span class="sxs-lookup"><span data-stu-id="790c2-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR\_DS\_NO\_TREE\_DELETE\_ABOVE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-923">8501 (0x2135) </span><span class="sxs-lookup"><span data-stu-id="790c2-923">8501 (0x2135)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-924">不允許從具有 NC 標頭的物件開始刪除樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="790c2-924">Tree deletions starting at an object which has an NC head as a descendant are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**\_ \_ \_ \_ \_ 用於 \_ 刪除的錯誤 DS 無法鎖定樹**</span><span class="sxs-lookup"><span data-stu-id="790c2-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR\_DS\_COULDNT\_LOCK\_TREE\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-926">8502 (0x2136) </span><span class="sxs-lookup"><span data-stu-id="790c2-926">8502 (0x2136)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-927">目錄服務無法鎖定樹狀結構，以準備刪除樹狀結構，因為該樹狀結構正在使用中。</span><span class="sxs-lookup"><span data-stu-id="790c2-927">The directory service failed to lock a tree in preparation for a tree deletion because the tree was in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**錯誤 \_ DS \_ 無法 \_ 識別 \_ \_ 用於 \_ 樹系 \_ 刪除的物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR\_DS\_COULDNT\_IDENTIFY\_OBJECTS\_FOR\_TREE\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-929">8503 (0x2137) </span><span class="sxs-lookup"><span data-stu-id="790c2-929">8503 (0x2137)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-930">目錄服務無法識別在嘗試刪除樹狀結構時要刪除的物件清單。</span><span class="sxs-lookup"><span data-stu-id="790c2-930">The directory service failed to identify the list of objects to delete while attempting a tree deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**\_DS \_ SAM \_ 初始化 \_ 失敗錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-932">8504 (0x2138) </span><span class="sxs-lookup"><span data-stu-id="790c2-932">8504 (0x2138)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-933">安全性帳戶管理員初始化失敗，因為發生下列錯誤： %1。</span><span class="sxs-lookup"><span data-stu-id="790c2-933">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="790c2-934">錯誤狀態： 0x %2。</span><span class="sxs-lookup"><span data-stu-id="790c2-934">Error Status: 0x%2.</span></span> <span data-ttu-id="790c2-935">請關閉此系統並重新啟動至目錄服務還原模式，檢查事件記錄檔以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="790c2-935">Please shutdown this system and reboot into Directory Services Restore Mode, check the event log for more detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**錯誤 \_ DS \_ 敏感性 \_ 群組 \_ 違規**</span><span class="sxs-lookup"><span data-stu-id="790c2-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR\_DS\_SENSITIVE\_GROUP\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-937">8505 (0x2139) </span><span class="sxs-lookup"><span data-stu-id="790c2-937">8505 (0x2139)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-938">只有系統管理員可以修改系統管理群組的成員資格清單。</span><span class="sxs-lookup"><span data-stu-id="790c2-938">Only an administrator can modify the membership list of an administrative group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**錯誤 \_ DS \_ 無法 \_ MOD \_ PRIMARYGROUPID**</span><span class="sxs-lookup"><span data-stu-id="790c2-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR\_DS\_CANT\_MOD\_PRIMARYGROUPID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-940">8506 (0x213A) </span><span class="sxs-lookup"><span data-stu-id="790c2-940">8506 (0x213A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-941">無法變更網域控制站帳戶的主要群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-941">Cannot change the primary group ID of a domain controller account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**錯誤 \_ DS 不 \_ 合法的 \_ 基底 \_ 架構 \_ MOD**</span><span class="sxs-lookup"><span data-stu-id="790c2-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR\_DS\_ILLEGAL\_BASE\_SCHEMA\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-943">8507 (0x213B) </span><span class="sxs-lookup"><span data-stu-id="790c2-943">8507 (0x213B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-944">嘗試修改基底架構。</span><span class="sxs-lookup"><span data-stu-id="790c2-944">An attempt is made to modify the base schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**錯誤 \_ DS \_ NONSAFE \_ 架構 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="790c2-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR\_DS\_NONSAFE\_SCHEMA\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-946">8508 (0x213C) </span><span class="sxs-lookup"><span data-stu-id="790c2-946">8508 (0x213C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-947">將新的強制屬性加入至現有的類別、從現有的類別中刪除強制屬性，或將選擇性屬性新增至不是 backlink 屬性的特殊類別 Top (直接或透過繼承，例如，藉由新增或刪除輔助類別) 則不允許。</span><span class="sxs-lookup"><span data-stu-id="790c2-947">Adding a new mandatory attribute to an existing class, deleting a mandatory attribute from an existing class, or adding an optional attribute to the special class Top that is not a backlink attribute (directly or through inheritance, for example, by adding or deleting an auxiliary class) is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**不 \_ 允許的 DS \_ 架構 \_ 更新 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR\_DS\_SCHEMA\_UPDATE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-949">8509 (0x213D) </span><span class="sxs-lookup"><span data-stu-id="790c2-949">8509 (0x213D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-950">因為 DC 不是架構 FSMO 角色擁有者，所以不允許在此 DC 上進行架構更新。</span><span class="sxs-lookup"><span data-stu-id="790c2-950">Schema update is not allowed on this DC because the DC is not the schema FSMO Role Owner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**無法 \_ \_ \_ \_ 在架構下建立錯誤 DS \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR\_DS\_CANT\_CREATE\_UNDER\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-952">8510 (0x213E) </span><span class="sxs-lookup"><span data-stu-id="790c2-952">8510 (0x213E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-953">此類別的物件無法在架構容器底下建立。</span><span class="sxs-lookup"><span data-stu-id="790c2-953">An object of this class cannot be created under the schema container.</span></span> <span data-ttu-id="790c2-954">您只能在架構容器底下建立屬性架構和類別架構物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-954">You can only create attribute-schema and class-schema objects under the schema container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**錯誤 \_ DS \_ 安裝 \_ 沒有 \_ SRC \_ .SCH \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="790c2-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR\_DS\_INSTALL\_NO\_SRC\_SCH\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-956">8511 (0x213F) </span><span class="sxs-lookup"><span data-stu-id="790c2-956">8511 (0x213F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-957">複本/子系安裝無法取得來源 DC 上架構容器上的 objectVersion 屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-957">The replica/child install failed to get the objectVersion attribute on the schema container on the source DC.</span></span> <span data-ttu-id="790c2-958">架構容器上缺少屬性，或提供的認證沒有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="790c2-958">Either the attribute is missing on the schema container or the credentials supplied do not have permission to read it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**錯誤 \_ DS \_ \_ \_ \_ \_ 在 INIFILE 中安裝沒有 .SCH 版本 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR\_DS\_INSTALL\_NO\_SCH\_VERSION\_IN\_INIFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-960">8512 (0x2140) </span><span class="sxs-lookup"><span data-stu-id="790c2-960">8512 (0x2140)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-961">在 system32 目錄的檔案 schema.ini 的 [架構] 區段中，複本/子安裝無法讀取 objectVersion 屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-961">The replica/child install failed to read the objectVersion attribute in the SCHEMA section of the file schema.ini in the system32 directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**錯誤 \_ DS \_ 不正確 \_ 群組 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="790c2-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR\_DS\_INVALID\_GROUP\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-963">8513 (0x2141) </span><span class="sxs-lookup"><span data-stu-id="790c2-963">8513 (0x2141)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-964">指定的群組類型無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-964">The specified group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**錯誤 \_ DS \_ \_ \_ \_ 在 MIXEDDOMAIN 中沒有任何嵌套 GLOBALGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_GLOBALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-966">8514 (0x2142) </span><span class="sxs-lookup"><span data-stu-id="790c2-966">8514 (0x2142)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-967">如果群組已啟用安全性，您就無法在混合網域中嵌套全域群組。</span><span class="sxs-lookup"><span data-stu-id="790c2-967">You cannot nest global groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**錯誤 \_ DS \_ \_ \_ \_ 在 MIXEDDOMAIN 中沒有任何嵌套 LOCALGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_LOCALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-969">8515 (0x2143) </span><span class="sxs-lookup"><span data-stu-id="790c2-969">8515 (0x2143)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-970">如果群組已啟用安全性，您就無法將本機群組嵌套在混合網域中。</span><span class="sxs-lookup"><span data-stu-id="790c2-970">You cannot nest local groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**錯誤 \_ DS \_ 全域 \_ 不 \_ 能有 \_ 本地 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="790c2-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-972">8516 (0x2144) </span><span class="sxs-lookup"><span data-stu-id="790c2-972">8516 (0x2144)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-973">全域群組不能有本機群組做為成員。</span><span class="sxs-lookup"><span data-stu-id="790c2-973">A global group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**錯誤 \_ DS \_ 全域 \_ 不 \_ 能有 \_ 通用 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="790c2-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-975">8517 (0x2145) </span><span class="sxs-lookup"><span data-stu-id="790c2-975">8517 (0x2145)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-976">全域群組不能有萬用群組作為成員。</span><span class="sxs-lookup"><span data-stu-id="790c2-976">A global group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**錯誤 \_ DS \_ 通用 \_ 不 \_ 可以有 \_ 本地 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="790c2-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR\_DS\_UNIVERSAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-978">8518 (0x2146) </span><span class="sxs-lookup"><span data-stu-id="790c2-978">8518 (0x2146)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-979">萬用群組不能將本機群組作為成員。</span><span class="sxs-lookup"><span data-stu-id="790c2-979">A universal group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**錯誤 \_ DS \_ 全域 \_ 不 \_ 能有 \_ MICROSOFT.AZURE.MOBILE.SERVER.CROSSDOMAIN \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="790c2-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_CROSSDOMAIN\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-981">8519 (0x2147) </span><span class="sxs-lookup"><span data-stu-id="790c2-981">8519 (0x2147)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-982">全域群組不能有跨網域成員。</span><span class="sxs-lookup"><span data-stu-id="790c2-982">A global group cannot have a cross-domain member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**錯誤 \_ DS \_ 本機 \_ 無法 \_ 具有 \_ MICROSOFT.AZURE.MOBILE.SERVER.CROSSDOMAIN \_ 本地 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="790c2-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR\_DS\_LOCAL\_CANT\_HAVE\_CROSSDOMAIN\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-984">8520 (0x2148) </span><span class="sxs-lookup"><span data-stu-id="790c2-984">8520 (0x2148)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-985">本機群組不能有另一個跨網網域本機群組做為成員。</span><span class="sxs-lookup"><span data-stu-id="790c2-985">A local group cannot have another cross domain local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**錯誤 \_ DS \_ 有 \_ 主要 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="790c2-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERROR\_DS\_HAVE\_PRIMARY\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-987">8521 (0x2149) </span><span class="sxs-lookup"><span data-stu-id="790c2-987">8521 (0x2149)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-988">具有主要成員的群組不能變更為安全性停用的群組。</span><span class="sxs-lookup"><span data-stu-id="790c2-988">A group with primary members cannot change to a security-disabled group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**錯誤 \_ DS \_ 字串 \_ SD \_ 轉換 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR\_DS\_STRING\_SD\_CONVERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-990">8522 (0x214A) </span><span class="sxs-lookup"><span data-stu-id="790c2-990">8522 (0x214A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-991">架構快取載入無法轉換類別架構物件上的字串預設 SD。</span><span class="sxs-lookup"><span data-stu-id="790c2-991">The schema cache load failed to convert the string default SD on a class-schema object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**\_DS \_ 命名 \_ 主機 \_ GC 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR\_DS\_NAMING\_MASTER\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-993">8523 (0x214B) </span><span class="sxs-lookup"><span data-stu-id="790c2-993">8523 (0x214B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-994">只有設定為通用類別目錄伺服器的設定為通用類別目錄伺服器的設定，才應允許持有網網域命名主機 FSMO 角色。</span><span class="sxs-lookup"><span data-stu-id="790c2-994">Only DSAs configured to be Global Catalog servers should be allowed to hold the Domain Naming Master FSMO role.</span></span> <span data-ttu-id="790c2-995"> (僅適用于 Windows 2000 伺服器。 ) </span><span class="sxs-lookup"><span data-stu-id="790c2-995">(Applies only to Windows 2000 servers.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**\_DS \_ DNS \_ 查閱 \_ 失敗錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR\_DS\_DNS\_LOOKUP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-997">8524 (0x214C) </span><span class="sxs-lookup"><span data-stu-id="790c2-997">8524 (0x214C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-998">因為 DNS 查閱失敗，所以 DSA 操作無法繼續。</span><span class="sxs-lookup"><span data-stu-id="790c2-998">The DSA operation is unable to proceed because of a DNS lookup failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**錯誤 \_ DS \_ 無法 \_ 更新 \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="790c2-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERROR\_DS\_COULDNT\_UPDATE\_SPNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1000">8525 (0x214D) </span><span class="sxs-lookup"><span data-stu-id="790c2-1000">8525 (0x214D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1001">處理物件的 DNS 主機名稱變更時，服務主體的名稱值無法保持同步。</span><span class="sxs-lookup"><span data-stu-id="790c2-1001">While processing a change to the DNS Host Name for an object, the Service Principal Name values could not be kept in sync.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**錯誤 \_ DS \_ 無法 \_ 取出 \_ SD**</span><span class="sxs-lookup"><span data-stu-id="790c2-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR\_DS\_CANT\_RETRIEVE\_SD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1003">8526 (0x214E) </span><span class="sxs-lookup"><span data-stu-id="790c2-1003">8526 (0x214E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1004">無法讀取安全描述項屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-1004">The Security Descriptor attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**錯誤 \_ DS \_ 金鑰 \_ 不是 \_ 唯一的**</span><span class="sxs-lookup"><span data-stu-id="790c2-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR\_DS\_KEY\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1006">8527 (0x214F) </span><span class="sxs-lookup"><span data-stu-id="790c2-1006">8527 (0x214F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1007">找不到要求的物件，但找到具有該索引鍵的物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-1007">The object requested was not found, but an object with that key was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**錯誤 \_ DS \_ \_ 連結的 \_ ATT \_ 語法錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR\_DS\_WRONG\_LINKED\_ATT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1009">8528 (0x2150) </span><span class="sxs-lookup"><span data-stu-id="790c2-1009">8528 (0x2150)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1010">所加入之連結屬性的語法不正確。</span><span class="sxs-lookup"><span data-stu-id="790c2-1010">The syntax of the linked attribute being added is incorrect.</span></span> <span data-ttu-id="790c2-1011">轉寄連結只能有語法2.5.5.1、2.5.5.7 和2.5.5.14，而 backlinks 只能有語法2.5.5.1。</span><span class="sxs-lookup"><span data-stu-id="790c2-1011">Forward links can only have syntax 2.5.5.1, 2.5.5.7, and 2.5.5.14, and backlinks can only have syntax 2.5.5.1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**錯誤 \_ DS \_ SAM \_ 需要 \_ BOOTKEY \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="790c2-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1013">8529 (0x2151) </span><span class="sxs-lookup"><span data-stu-id="790c2-1013">8529 (0x2151)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1014">安全性帳戶管理員需要取得開機密碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-1014">Security Account Manager needs to get the boot password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**錯誤 \_ DS \_ SAM \_ 需要 \_ BOOTKEY \_ 軟碟**</span><span class="sxs-lookup"><span data-stu-id="790c2-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_FLOPPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1016">8530 (0x2152) </span><span class="sxs-lookup"><span data-stu-id="790c2-1016">8530 (0x2152)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1017">安全性帳戶管理員需要從磁片磁碟機取得開機金鑰。</span><span class="sxs-lookup"><span data-stu-id="790c2-1017">Security Account Manager needs to get the boot key from floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**錯誤 \_ DS \_ 無法 \_ 啟動**</span><span class="sxs-lookup"><span data-stu-id="790c2-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR\_DS\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1019">8531 (0x2153) </span><span class="sxs-lookup"><span data-stu-id="790c2-1019">8531 (0x2153)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1020">無法啟動目錄服務。</span><span class="sxs-lookup"><span data-stu-id="790c2-1020">Directory Service cannot start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**錯誤 \_ DS \_ 初始化 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR\_DS\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1022">8532 (0x2154) </span><span class="sxs-lookup"><span data-stu-id="790c2-1022">8532 (0x2154)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1023">無法啟動目錄服務。</span><span class="sxs-lookup"><span data-stu-id="790c2-1023">Directory Services could not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**錯誤 \_ DS \_ 沒有 \_ \_ \_ 連接的 PKT \_ 隱私權**</span><span class="sxs-lookup"><span data-stu-id="790c2-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR\_DS\_NO\_PKT\_PRIVACY\_ON\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1025">8533 (0x2155) </span><span class="sxs-lookup"><span data-stu-id="790c2-1025">8533 (0x2155)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1026">用戶端與伺服器之間的連線需要封包隱私權或更好的資訊。</span><span class="sxs-lookup"><span data-stu-id="790c2-1026">The connection between client and server requires packet privacy or better.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**\_樹系 \_ \_ \_ 中的 DS 來源網域 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERROR\_DS\_SOURCE\_DOMAIN\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1028">8534 (0x2156) </span><span class="sxs-lookup"><span data-stu-id="790c2-1028">8534 (0x2156)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1029">來源網域可能不在與目的地相同的樹系中。</span><span class="sxs-lookup"><span data-stu-id="790c2-1029">The source domain may not be in the same forest as destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**錯誤 \_ DS \_ 目的地 \_ 網域 \_ 不 \_ 在 \_ 樹系中**</span><span class="sxs-lookup"><span data-stu-id="790c2-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR\_DS\_DESTINATION\_DOMAIN\_NOT\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1031">8535 (0x2157) </span><span class="sxs-lookup"><span data-stu-id="790c2-1031">8535 (0x2157)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1032">目的地網域必須在樹系中。</span><span class="sxs-lookup"><span data-stu-id="790c2-1032">The destination domain must be in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**\_ \_ \_ \_ 未啟用 DS 目的地審核 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR\_DS\_DESTINATION\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1034">8536 (0x2158) </span><span class="sxs-lookup"><span data-stu-id="790c2-1034">8536 (0x2158)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1035">作業需要啟用目的地網域審核。</span><span class="sxs-lookup"><span data-stu-id="790c2-1035">The operation requires that destination domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**錯誤 \_ DS \_ \_ 找不 \_ 到 \_ \_ SRC \_ 網域的 DC**</span><span class="sxs-lookup"><span data-stu-id="790c2-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR\_DS\_CANT\_FIND\_DC\_FOR\_SRC\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1037">8537 (0x2159) </span><span class="sxs-lookup"><span data-stu-id="790c2-1037">8537 (0x2159)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1038">操作找不到來源網域的 DC。</span><span class="sxs-lookup"><span data-stu-id="790c2-1038">The operation couldn't locate a DC for the source domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**錯誤 \_ DS \_ SRC \_ OBJ \_ 非 \_ 群組 \_ 或 \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="790c2-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR\_DS\_SRC\_OBJ\_NOT\_GROUP\_OR\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1040">8538 (0x215A) </span><span class="sxs-lookup"><span data-stu-id="790c2-1040">8538 (0x215A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1041">來源物件必須是群組或使用者。</span><span class="sxs-lookup"><span data-stu-id="790c2-1041">The source object must be a group or user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**\_樹系 \_ \_ \_ \_ 中存在 \_ DS SRC SID 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR\_DS\_SRC\_SID\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1043">8539 (0x215B) </span><span class="sxs-lookup"><span data-stu-id="790c2-1043">8539 (0x215B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1044">來源物件的 SID 已存在於目的地樹系中。</span><span class="sxs-lookup"><span data-stu-id="790c2-1044">The source object's SID already exists in destination forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**\_DS \_ SRC \_ 和 \_ DST \_ 物件 \_ 類別 \_ 不符的錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR\_DS\_SRC\_AND\_DST\_OBJECT\_CLASS\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1046">8540 (0x215C) </span><span class="sxs-lookup"><span data-stu-id="790c2-1046">8540 (0x215C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1047">來源和目的地物件必須是相同的類型。</span><span class="sxs-lookup"><span data-stu-id="790c2-1047">The source and destination object must be of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**錯誤 \_ SAM \_ 初始化 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1049">8541 (0x215D) </span><span class="sxs-lookup"><span data-stu-id="790c2-1049">8541 (0x215D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1050">安全性帳戶管理員初始化失敗，因為發生下列錯誤： %1。</span><span class="sxs-lookup"><span data-stu-id="790c2-1050">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="790c2-1051">錯誤狀態： 0x %2。</span><span class="sxs-lookup"><span data-stu-id="790c2-1051">Error Status: 0x%2.</span></span> <span data-ttu-id="790c2-1052">按一下 [確定] 關閉系統，然後重新開機進入安全模式。</span><span class="sxs-lookup"><span data-stu-id="790c2-1052">Click OK to shut down the system and reboot into Safe Mode.</span></span> <span data-ttu-id="790c2-1053">請檢查事件記錄檔以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="790c2-1053">Check the event log for detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**\_傳送的 DS \_ DRA \_ 架構 \_ 資訊 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR\_DS\_DRA\_SCHEMA\_INFO\_SHIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1055">8542 (0x215E) </span><span class="sxs-lookup"><span data-stu-id="790c2-1055">8542 (0x215E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1056">無法在複寫要求中包含架構資訊。</span><span class="sxs-lookup"><span data-stu-id="790c2-1056">Schema information could not be included in the replication request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**\_DS \_ DRA \_ 架構 \_ 衝突錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERROR\_DS\_DRA\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1058">8543 (0x215F) </span><span class="sxs-lookup"><span data-stu-id="790c2-1058">8543 (0x215F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1059">因為架構不相容，所以無法完成複寫作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-1059">The replication operation could not be completed due to a schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**錯誤 \_ DS \_ DRA \_ 先前的 \_ 架構 \_ 衝突**</span><span class="sxs-lookup"><span data-stu-id="790c2-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERROR\_DS\_DRA\_EARLIER\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1061">8544 (0x2160) </span><span class="sxs-lookup"><span data-stu-id="790c2-1061">8544 (0x2160)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1062">因為先前的架構不相容，所以無法完成複寫作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-1062">The replication operation could not be completed due to a previous schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**錯誤 \_ DS \_ DRA 的 \_ OBJ \_ NC \_ 不相符**</span><span class="sxs-lookup"><span data-stu-id="790c2-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR\_DS\_DRA\_OBJ\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1064">8545 (0x2161) </span><span class="sxs-lookup"><span data-stu-id="790c2-1064">8545 (0x2161)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1065">無法套用複寫更新，因為來源或目的地尚未收到有關最近跨網域移動作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="790c2-1065">The replication update could not be applied because either the source or the destination has not yet received information regarding a recent cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**錯誤 \_ DS \_ NC \_ 仍 \_ 具有 \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="790c2-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERROR\_DS\_NC\_STILL\_HAS\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1067">8546 (0x2162) </span><span class="sxs-lookup"><span data-stu-id="790c2-1067">8546 (0x2162)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1068">無法刪除要求的網域，因為存在仍裝載此網域的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="790c2-1068">The requested domain could not be deleted because there exist domain controllers that still host this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**\_需要錯誤 DS \_ GC \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR\_DS\_GC\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1070">8547 (0x2163) </span><span class="sxs-lookup"><span data-stu-id="790c2-1070">8547 (0x2163)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1071">要求的作業只能在通用類別目錄伺服器上執行。</span><span class="sxs-lookup"><span data-stu-id="790c2-1071">The requested operation can be performed only on a global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**\_ \_ \_ \_ 本機的錯誤 \_ DS 本機成員 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR\_DS\_LOCAL\_MEMBER\_OF\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1073">8548 (0x2164) </span><span class="sxs-lookup"><span data-stu-id="790c2-1073">8548 (0x2164)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1074">本機群組只能是相同網域中其他本機群組的成員。</span><span class="sxs-lookup"><span data-stu-id="790c2-1074">A local group can only be a member of other local groups in the same domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**錯誤 \_ DS \_ \_ \_ 在 \_ 萬用群組中 \_ 沒有任何 FPO**</span><span class="sxs-lookup"><span data-stu-id="790c2-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR\_DS\_NO\_FPO\_IN\_UNIVERSAL\_GROUPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1076">8549 (0x2165) </span><span class="sxs-lookup"><span data-stu-id="790c2-1076">8549 (0x2165)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1077">外部安全性主體不可以是萬用群組的成員。</span><span class="sxs-lookup"><span data-stu-id="790c2-1077">Foreign security principals cannot be members of universal groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**錯誤 \_ DS \_ \_ 無法新增 \_ 至 \_ GC**</span><span class="sxs-lookup"><span data-stu-id="790c2-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR\_DS\_CANT\_ADD\_TO\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1079">8550 (0x2166) </span><span class="sxs-lookup"><span data-stu-id="790c2-1079">8550 (0x2166)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1080">基於安全性考慮，不允許將屬性複寫至 GC。</span><span class="sxs-lookup"><span data-stu-id="790c2-1080">The attribute is not allowed to be replicated to the GC because of security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**錯誤 \_ DS \_ 沒有 \_ \_ PDC 的檢查點 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR\_DS\_NO\_CHECKPOINT\_WITH\_PDC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1082">8551 (0x2167) </span><span class="sxs-lookup"><span data-stu-id="790c2-1082">8551 (0x2167)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1083">因為目前正在處理太多修改，所以無法取得具有 PDC 的檢查點。</span><span class="sxs-lookup"><span data-stu-id="790c2-1083">The checkpoint with the PDC could not be taken because there too many modifications being processed currently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**\_ \_ \_ \_ 未啟用錯誤 DS 來源 \_ 審核**</span><span class="sxs-lookup"><span data-stu-id="790c2-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR\_DS\_SOURCE\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1085">8552 (0x2168) </span><span class="sxs-lookup"><span data-stu-id="790c2-1085">8552 (0x2168)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1086">作業需要啟用來源網域審核。</span><span class="sxs-lookup"><span data-stu-id="790c2-1086">The operation requires that source domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**無法 \_ 在非網域 \_ \_ \_ \_ NC 中 \_ 建立錯誤 DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR\_DS\_CANT\_CREATE\_IN\_NONDOMAIN\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1088">8553 (0x2169) </span><span class="sxs-lookup"><span data-stu-id="790c2-1088">8553 (0x2169)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1089">安全性主體物件只能在網域命名內容內建立。</span><span class="sxs-lookup"><span data-stu-id="790c2-1089">Security principal objects can only be created inside domain naming contexts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**\_ \_ \_ \_ SPN 的錯誤 DS 名稱 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="790c2-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR\_DS\_INVALID\_NAME\_FOR\_SPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1091">8554 (0x216A) </span><span class="sxs-lookup"><span data-stu-id="790c2-1091">8554 (0x216A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1092">因為提供的主機名稱不是所需的格式，所以無法建立服務主體名稱 (SPN) 。</span><span class="sxs-lookup"><span data-stu-id="790c2-1092">A Service Principal Name (SPN) could not be constructed because the provided hostname is not in the necessary format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**錯誤 \_ DS \_ 篩選器 \_ 使用 \_ 效果 \_ ATTRS**</span><span class="sxs-lookup"><span data-stu-id="790c2-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERROR\_DS\_FILTER\_USES\_CONTRUCTED\_ATTRS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1094">8555 (0x216B) </span><span class="sxs-lookup"><span data-stu-id="790c2-1094">8555 (0x216B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1095">傳遞的篩選會使用已建立的屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-1095">A Filter was passed that uses constructed attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**錯誤 \_ DS \_ UNICODEPWD \_ 不 \_ 在 \_ 引號中**</span><span class="sxs-lookup"><span data-stu-id="790c2-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR\_DS\_UNICODEPWD\_NOT\_IN\_QUOTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1097">8556 (0x216C) </span><span class="sxs-lookup"><span data-stu-id="790c2-1097">8556 (0x216C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1098">UnicodePwd 屬性值必須用雙引號括住。</span><span class="sxs-lookup"><span data-stu-id="790c2-1098">The unicodePwd attribute value must be enclosed in double quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**\_超出 DS \_ 電腦 \_ 帳戶 \_ 配額 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1100">8557 (0x216D) </span><span class="sxs-lookup"><span data-stu-id="790c2-1100">8557 (0x216D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1101">您的電腦無法加入網域。</span><span class="sxs-lookup"><span data-stu-id="790c2-1101">Your computer could not be joined to the domain.</span></span> <span data-ttu-id="790c2-1102">您已超過允許在此網域中建立的電腦帳戶數目上限。</span><span class="sxs-lookup"><span data-stu-id="790c2-1102">You have exceeded the maximum number of computer accounts you are allowed to create in this domain.</span></span> <span data-ttu-id="790c2-1103">請洽詢您的系統管理員，以重設或增加此限制。</span><span class="sxs-lookup"><span data-stu-id="790c2-1103">Contact your system administrator to have this limit reset or increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**\_ \_ 必須 \_ \_ \_ 在 \_ DST \_ DC 上執行錯誤 DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**ERROR\_DS\_MUST\_BE\_RUN\_ON\_DST\_DC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1105">8558 (0x216E) </span><span class="sxs-lookup"><span data-stu-id="790c2-1105">8558 (0x216E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1106">基於安全性考慮，必須在目的地 DC 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-1106">For security reasons, the operation must be run on the destination DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**錯誤 \_ DS \_ SRC \_ DC \_ 必須 \_ 是 \_ SP4 \_ 或 \_ 更高版本**</span><span class="sxs-lookup"><span data-stu-id="790c2-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR\_DS\_SRC\_DC\_MUST\_BE\_SP4\_OR\_GREATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1108">8559 (0x216F) </span><span class="sxs-lookup"><span data-stu-id="790c2-1108">8559 (0x216F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1109">基於安全性理由，來源 DC 必須是 NT4SP4 或更高的版本。</span><span class="sxs-lookup"><span data-stu-id="790c2-1109">For security reasons, the source DC must be NT4SP4 or greater.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**錯誤 \_ DS \_ 無法 \_ \_ 刪除 \_ 重要的 \_ OBJ**</span><span class="sxs-lookup"><span data-stu-id="790c2-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR\_DS\_CANT\_TREE\_DELETE\_CRITICAL\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1111">8560 (0x2170) </span><span class="sxs-lookup"><span data-stu-id="790c2-1111">8560 (0x2170)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1112">在樹系刪除作業期間，無法刪除重要目錄服務系統物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-1112">Critical Directory Service System objects cannot be deleted during tree delete operations.</span></span> <span data-ttu-id="790c2-1113">樹狀目錄刪除可能已部分執行。</span><span class="sxs-lookup"><span data-stu-id="790c2-1113">The tree delete may have been partially performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**錯誤 \_ DS \_ 初始化 \_ 失敗 \_ 主控台**</span><span class="sxs-lookup"><span data-stu-id="790c2-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR\_DS\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1115">8561 (0x2171) </span><span class="sxs-lookup"><span data-stu-id="790c2-1115">8561 (0x2171)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1116">目錄服務無法啟動，因為發生下列錯誤： %1。</span><span class="sxs-lookup"><span data-stu-id="790c2-1116">Directory Services could not start because of the following error: %1.</span></span> <span data-ttu-id="790c2-1117">錯誤狀態： 0x %2。</span><span class="sxs-lookup"><span data-stu-id="790c2-1117">Error Status: 0x%2.</span></span> <span data-ttu-id="790c2-1118">請按一下 [確定] 以關閉系統。</span><span class="sxs-lookup"><span data-stu-id="790c2-1118">Please click OK to shutdown the system.</span></span> <span data-ttu-id="790c2-1119">您可以使用 [修復主控台] 進一步診斷系統。</span><span class="sxs-lookup"><span data-stu-id="790c2-1119">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**錯誤 \_ DS \_ SAM \_ 初始化 \_ 失敗 \_ 主控台**</span><span class="sxs-lookup"><span data-stu-id="790c2-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1121">8562 (0x2172) </span><span class="sxs-lookup"><span data-stu-id="790c2-1121">8562 (0x2172)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1122">安全性帳戶管理員初始化失敗，因為發生下列錯誤： %1。</span><span class="sxs-lookup"><span data-stu-id="790c2-1122">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="790c2-1123">錯誤狀態： 0x %2。</span><span class="sxs-lookup"><span data-stu-id="790c2-1123">Error Status: 0x%2.</span></span> <span data-ttu-id="790c2-1124">請按一下 [確定] 以關閉系統。</span><span class="sxs-lookup"><span data-stu-id="790c2-1124">Please click OK to shutdown the system.</span></span> <span data-ttu-id="790c2-1125">您可以使用 [修復主控台] 進一步診斷系統。</span><span class="sxs-lookup"><span data-stu-id="790c2-1125">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**錯誤 \_ DS \_ 樹系 \_ 版本 \_ 過 \_ 高**</span><span class="sxs-lookup"><span data-stu-id="790c2-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1127">8563 (0x2173) </span><span class="sxs-lookup"><span data-stu-id="790c2-1127">8563 (0x2173)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1128">作業系統的版本與目前的 AD DS 樹系功能等級或 AD LDS 設定集功能等級不相容。</span><span class="sxs-lookup"><span data-stu-id="790c2-1128">The version of the operating system is incompatible with the current AD DS forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="790c2-1129">您必須升級為新版的作業系統，此伺服器才能成為 AD DS 網域控制站，或在此 AD DS 樹系或 AD LDS 設定集中新增 AD LDS 實例。</span><span class="sxs-lookup"><span data-stu-id="790c2-1129">You must upgrade to a new version of the operating system before this server can become an AD DS Domain Controller or add an AD LDS Instance in this AD DS Forest or AD LDS Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**錯誤 \_ DS \_ 網域 \_ 版本 \_ 過 \_ 高**</span><span class="sxs-lookup"><span data-stu-id="790c2-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1131">8564 (0x2174) </span><span class="sxs-lookup"><span data-stu-id="790c2-1131">8564 (0x2174)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1132">安裝的作業系統版本與目前的網域功能等級不相容。</span><span class="sxs-lookup"><span data-stu-id="790c2-1132">The version of the operating system installed is incompatible with the current domain functional level.</span></span> <span data-ttu-id="790c2-1133">您必須先升級為新版的作業系統，此伺服器才能成為此網域中的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="790c2-1133">You must upgrade to a new version of the operating system before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**錯誤 \_ DS \_ 樹系 \_ 版本 \_ 太 \_ 低**</span><span class="sxs-lookup"><span data-stu-id="790c2-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1135">8565 (0x2175) </span><span class="sxs-lookup"><span data-stu-id="790c2-1135">8565 (0x2175)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1136">安裝在這部伺服器上的作業系統版本不再支援目前的 AD DS 樹系功能等級或 AD LDS 設定集功能等級。</span><span class="sxs-lookup"><span data-stu-id="790c2-1136">The version of the operating system installed on this server no longer supports the current AD DS Forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="790c2-1137">您必須提高 AD DS 樹系功能等級或 AD LDS 設定集功能等級，此伺服器才能成為此樹系或設定集中的 AD DS 網域控制站或 AD LDS 實例。</span><span class="sxs-lookup"><span data-stu-id="790c2-1137">You must raise the AD DS Forest functional level or AD LDS Configuration Set functional level before this server can become an AD DS Domain Controller or an AD LDS Instance in this Forest or Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**錯誤 \_ DS \_ 網域 \_ 版本 \_ 太 \_ 低**</span><span class="sxs-lookup"><span data-stu-id="790c2-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1139">8566 (0x2176) </span><span class="sxs-lookup"><span data-stu-id="790c2-1139">8566 (0x2176)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1140">安裝在此伺服器上的作業系統版本不再支援目前的網域功能等級。</span><span class="sxs-lookup"><span data-stu-id="790c2-1140">The version of the operating system installed on this server no longer supports the current domain functional level.</span></span> <span data-ttu-id="790c2-1141">您必須提高網域功能等級，此伺服器才能成為此網域中的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="790c2-1141">You must raise the domain functional level before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**錯誤 \_ DS \_ 不相容的 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="790c2-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR\_DS\_INCOMPATIBLE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1143">8567 (0x2177) </span><span class="sxs-lookup"><span data-stu-id="790c2-1143">8567 (0x2177)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1144">此伺服器上安裝的作業系統版本與網域或樹系的功能等級不相容。</span><span class="sxs-lookup"><span data-stu-id="790c2-1144">The version of the operating system installed on this server is incompatible with the functional level of the domain or forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**錯誤 \_ DS \_ 低 \_ DSA \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="790c2-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR\_DS\_LOW\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1146">8568 (0x2178) </span><span class="sxs-lookup"><span data-stu-id="790c2-1146">8568 (0x2178)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1147">網域 (或樹系) 的功能等級無法提高為要求的值，因為網域 (或樹系) 中有一或多個網域控制站位於較不相容的功能等級。</span><span class="sxs-lookup"><span data-stu-id="790c2-1147">The functional level of the domain (or forest) cannot be raised to the requested value, because there exist one or more domain controllers in the domain (or forest) that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**錯誤 \_ DS \_ \_ \_ \_ 在 MIXEDDOMAIN 中沒有行為版本 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR\_DS\_NO\_BEHAVIOR\_VERSION\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1149">8569 (0x2179) </span><span class="sxs-lookup"><span data-stu-id="790c2-1149">8569 (0x2179)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1150">樹系功能等級無法提高為要求的值，因為有一或多個網域仍處於混合網域模式。</span><span class="sxs-lookup"><span data-stu-id="790c2-1150">The forest functional level cannot be raised to the requested value since one or more domains are still in mixed domain mode.</span></span> <span data-ttu-id="790c2-1151">樹系中的所有網域必須處於原生模式，您才能提高樹系功能等級。</span><span class="sxs-lookup"><span data-stu-id="790c2-1151">All domains in the forest must be in native mode, for you to raise the forest functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**錯誤 \_ DS \_ 不 \_ 支援的 \_ 排序 \_ 順序**</span><span class="sxs-lookup"><span data-stu-id="790c2-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR\_DS\_NOT\_SUPPORTED\_SORT\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1153">8570 (0x217A) </span><span class="sxs-lookup"><span data-stu-id="790c2-1153">8570 (0x217A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1154">不支援要求的排序次序。</span><span class="sxs-lookup"><span data-stu-id="790c2-1154">The sort order requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**錯誤 \_ DS \_ 名稱 \_ 不是 \_ 唯一的**</span><span class="sxs-lookup"><span data-stu-id="790c2-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR\_DS\_NAME\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1156">8571 (0x217B) </span><span class="sxs-lookup"><span data-stu-id="790c2-1156">8571 (0x217B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1157">要求的名稱已存在為唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-1157">The requested name already exists as a unique identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**\_PRENT4 建立的 DS \_ 電腦 \_ 帳戶 \_ \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_CREATED\_PRENT4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1159">8572 (0x217C) </span><span class="sxs-lookup"><span data-stu-id="790c2-1159">8572 (0x217C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1160">電腦帳戶是在 NT4 之前建立的。</span><span class="sxs-lookup"><span data-stu-id="790c2-1160">The machine account was created pre-NT4.</span></span> <span data-ttu-id="790c2-1161">需要重新建立帳戶。</span><span class="sxs-lookup"><span data-stu-id="790c2-1161">The account needs to be recreated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**\_ \_ \_ \_ 版本 \_ 存放區發生錯誤 DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR\_DS\_OUT\_OF\_VERSION\_STORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1163">8573 (0x217D) </span><span class="sxs-lookup"><span data-stu-id="790c2-1163">8573 (0x217D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1164">資料庫不在版本存放區中。</span><span class="sxs-lookup"><span data-stu-id="790c2-1164">The database is out of version store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**\_使用了 DS \_ 不相容的錯誤 \_ 控制項 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR\_DS\_INCOMPATIBLE\_CONTROLS\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1166">8574 (0x217E) </span><span class="sxs-lookup"><span data-stu-id="790c2-1166">8574 (0x217E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1167">因為使用了多個衝突的控制項，所以無法繼續操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-1167">Unable to continue operation because multiple conflicting controls were used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**錯誤 \_ DS \_ 沒有任何 \_ REF \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="790c2-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR\_DS\_NO\_REF\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1169">8575 (0x217F) </span><span class="sxs-lookup"><span data-stu-id="790c2-1169">8575 (0x217F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1170">找不到此分割區的有效安全描述項參考網域。</span><span class="sxs-lookup"><span data-stu-id="790c2-1170">Unable to find a valid security descriptor reference domain for this partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**\_DS \_ 保留 \_ 連結 \_ 識別碼錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERROR\_DS\_RESERVED\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1172">8576 (0x2180) </span><span class="sxs-lookup"><span data-stu-id="790c2-1172">8576 (0x2180)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1173">架構更新失敗：連結識別碼已保留。</span><span class="sxs-lookup"><span data-stu-id="790c2-1173">Schema update failed: The link identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**錯誤 \_ DS \_ 連結 \_ 識別碼 \_ 無法 \_ 使用**</span><span class="sxs-lookup"><span data-stu-id="790c2-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERROR\_DS\_LINK\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1175">8577 (0x2181) </span><span class="sxs-lookup"><span data-stu-id="790c2-1175">8577 (0x2181)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1176">架構更新失敗：沒有可用的連結識別碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-1176">Schema update failed: There are no link identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**錯誤 \_ DS \_ AG \_ 不 \_ 能有 \_ 通用 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="790c2-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR\_DS\_AG\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1178">8578 (0x2182) </span><span class="sxs-lookup"><span data-stu-id="790c2-1178">8578 (0x2182)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1179">帳戶群組不能有萬用群組作為成員。</span><span class="sxs-lookup"><span data-stu-id="790c2-1179">An account group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**\_ \_ \_ \_ \_ 實例類型不允許的 DS \_ MODIFYDN 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1181">8579 (0x2183) </span><span class="sxs-lookup"><span data-stu-id="790c2-1181">8579 (0x2183)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1182">不允許對命名內容標頭或唯讀物件進行重新命名或移動作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-1182">Rename or move operations on naming context heads or read-only objects are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**錯誤 \_ DS \_ \_ \_ \_ 在 \_ 架構 \_ NC 中沒有物件移動**</span><span class="sxs-lookup"><span data-stu-id="790c2-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR\_DS\_NO\_OBJECT\_MOVE\_IN\_SCHEMA\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1184">8580 (0x2184) </span><span class="sxs-lookup"><span data-stu-id="790c2-1184">8580 (0x2184)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1185">不允許對架構命名內容中的物件進行移動作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-1185">Move operations on objects in the schema naming context are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**\_旗標 \_ 不 \_ 允許 \_ 的 \_ 錯誤 DS MODIFYDN**</span><span class="sxs-lookup"><span data-stu-id="790c2-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1187">8581 (0x2185) </span><span class="sxs-lookup"><span data-stu-id="790c2-1187">8581 (0x2185)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1188">物件上已設定系統旗標，且不允許移動或重新命名物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-1188">A system flag has been set on the object and does not allow the object to be moved or renamed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**錯誤 \_ DS \_ MODIFYDN \_ 錯誤的 \_ 祖系**</span><span class="sxs-lookup"><span data-stu-id="790c2-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR\_DS\_MODIFYDN\_WRONG\_GRANDPARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1190">8582 (0x2186) </span><span class="sxs-lookup"><span data-stu-id="790c2-1190">8582 (0x2186)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1191">此物件不允許變更其祖系容器。</span><span class="sxs-lookup"><span data-stu-id="790c2-1191">This object is not allowed to change its grandparent container.</span></span> <span data-ttu-id="790c2-1192">在此物件上不禁止移動，但受限於同級容器。</span><span class="sxs-lookup"><span data-stu-id="790c2-1192">Moves are not forbidden on this object, but are restricted to sibling containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**錯誤 \_ DS \_ 名稱 \_ 錯誤 \_ 信任 \_ 參考**</span><span class="sxs-lookup"><span data-stu-id="790c2-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERROR\_DS\_NAME\_ERROR\_TRUST\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1194">8583 (0x2187) </span><span class="sxs-lookup"><span data-stu-id="790c2-1194">8583 (0x2187)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1195">無法完全解決，會產生對另一個樹系的參考。</span><span class="sxs-lookup"><span data-stu-id="790c2-1195">Unable to resolve completely, a referral to another forest is generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**\_ \_ \_ \_ 標準伺服器不支援的 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR\_NOT\_SUPPORTED\_ON\_STANDARD\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1197">8584 (0x2188) </span><span class="sxs-lookup"><span data-stu-id="790c2-1197">8584 (0x2188)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1198">標準伺服器不支援要求的動作。</span><span class="sxs-lookup"><span data-stu-id="790c2-1198">The requested action is not supported on standard server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**錯誤 \_ DS \_ 無法 \_ 存取 \_ \_ \_ AD 的遠端 \_ 部分**</span><span class="sxs-lookup"><span data-stu-id="790c2-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR\_DS\_CANT\_ACCESS\_REMOTE\_PART\_OF\_AD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1200">8585 (0x2189) </span><span class="sxs-lookup"><span data-stu-id="790c2-1200">8585 (0x2189)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1201">無法存取位於遠端伺服器上目錄服務的磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="790c2-1201">Could not access a partition of the directory service located on a remote server.</span></span> <span data-ttu-id="790c2-1202">請確定至少有一部伺服器正在針對有問題的分割區執行。</span><span class="sxs-lookup"><span data-stu-id="790c2-1202">Make sure at least one server is running for the partition in question.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**\_ \_ \_ 無法 \_ \_ 驗證 \_ V2 的 DS CR 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE\_V2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1204">8586 (0x218A) </span><span class="sxs-lookup"><span data-stu-id="790c2-1204">8586 (0x218A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1205">目錄無法驗證建議的命名內容 (或分割區) 名稱，因為它不會保存複本，也不能在建議的命名內容上方連接命名內容的複本。</span><span class="sxs-lookup"><span data-stu-id="790c2-1205">The directory cannot validate the proposed naming context (or partition) name because it does not hold a replica nor can it contact a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="790c2-1206">請確定已在 DNS 中正確註冊父命名內容，且網網域命名主機至少可以連線到此命名內容的一個複本。</span><span class="sxs-lookup"><span data-stu-id="790c2-1206">Please ensure that the parent naming context is properly registered in DNS, and at least one replica of this naming context is reachable by the Domain Naming master.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**\_超過錯誤 DS \_ 執行緒 \_ 限制 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERROR\_DS\_THREAD\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1208">8587 (0x218B) </span><span class="sxs-lookup"><span data-stu-id="790c2-1208">8587 (0x218B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1209">已超過此要求的執行緒限制。</span><span class="sxs-lookup"><span data-stu-id="790c2-1209">The thread limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**錯誤 \_ DS \_ 未 \_ 最接近**</span><span class="sxs-lookup"><span data-stu-id="790c2-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR\_DS\_NOT\_CLOSEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1211">8588 (0x218C) </span><span class="sxs-lookup"><span data-stu-id="790c2-1211">8588 (0x218C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1212">通用類別目錄伺服器不在最接近的網站。</span><span class="sxs-lookup"><span data-stu-id="790c2-1212">The Global catalog server is not in the closest site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**錯誤 \_ DS 無法在 \_ \_ \_ \_ 沒有 \_ 伺服器 \_ REF 的情況下衍生 SPN**</span><span class="sxs-lookup"><span data-stu-id="790c2-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_WITHOUT\_SERVER\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1214">8589 (0x218D) </span><span class="sxs-lookup"><span data-stu-id="790c2-1214">8589 (0x218D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1215">DS 無法衍生服務主體名稱 (SPN) 用來相互驗證目標伺服器，因為本機 DS 資料庫中對應的伺服器物件沒有 serverReference 屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-1215">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the corresponding server object in the local DS database has no serverReference attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**錯誤 \_ DS \_ 單一 \_ 使用者 \_ 模式 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR\_DS\_SINGLE\_USER\_MODE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1217">8590 (0x218E) </span><span class="sxs-lookup"><span data-stu-id="790c2-1217">8590 (0x218E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1218">目錄服務無法進入單一使用者模式。</span><span class="sxs-lookup"><span data-stu-id="790c2-1218">The Directory Service failed to enter single user mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**錯誤 \_ DS \_ NTDSCRIPT \_ 語法 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**ERROR\_DS\_NTDSCRIPT\_SYNTAX\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1220">8591 (0x218F) </span><span class="sxs-lookup"><span data-stu-id="790c2-1220">8591 (0x218F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1221">由於語法錯誤，目錄服務無法剖析腳本。</span><span class="sxs-lookup"><span data-stu-id="790c2-1221">The Directory Service cannot parse the script because of a syntax error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**錯誤 \_ DS \_ NTDSCRIPT \_ 進程 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERROR\_DS\_NTDSCRIPT\_PROCESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1223">8592 (0x2190) </span><span class="sxs-lookup"><span data-stu-id="790c2-1223">8592 (0x2190)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1224">目錄服務無法處理腳本，因為發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="790c2-1224">The Directory Service cannot process the script because of an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**錯誤 \_ DS \_ 不同的複寫 \_ \_ EPOCH**</span><span class="sxs-lookup"><span data-stu-id="790c2-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERROR\_DS\_DIFFERENT\_REPL\_EPOCHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1226">8593 (0x2191) </span><span class="sxs-lookup"><span data-stu-id="790c2-1226">8593 (0x2191)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1227">目錄服務無法執行要求的作業，因為涉及的伺服器屬於不同的複寫 epoch (這通常與進行中的網域重新命名相關) 。</span><span class="sxs-lookup"><span data-stu-id="790c2-1227">The directory service cannot perform the requested operation because the servers involved are of different replication epochs (which is usually related to a domain rename that is in progress).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**錯誤 \_ DS \_ DRS \_ 擴充功能 \_ 已變更**</span><span class="sxs-lookup"><span data-stu-id="790c2-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERROR\_DS\_DRS\_EXTENSIONS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1229">8594 (0x2192) </span><span class="sxs-lookup"><span data-stu-id="790c2-1229">8594 (0x2192)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1230">因為伺服器擴充功能資訊的變更，所以必須重新協商目錄服務系結。</span><span class="sxs-lookup"><span data-stu-id="790c2-1230">The directory service binding must be renegotiated due to a change in the server extensions information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**\_ \_ \_ \_ \_ \_ \_ \_ 停用的 CR 上不允許 \_ 發生錯誤 DS 複本集變更**</span><span class="sxs-lookup"><span data-stu-id="790c2-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR\_DS\_REPLICA\_SET\_CHANGE\_NOT\_ALLOWED\_ON\_DISABLED\_CR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1232">8595 (0x2193) </span><span class="sxs-lookup"><span data-stu-id="790c2-1232">8595 (0x2193)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1233">不允許在停用的交叉參考上進行操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-1233">Operation not allowed on a disabled cross ref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**錯誤 \_ DS \_ 無 \_ \_ INTID**</span><span class="sxs-lookup"><span data-stu-id="790c2-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR\_DS\_NO\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1235">8596 (0x2194) </span><span class="sxs-lookup"><span data-stu-id="790c2-1235">8596 (0x2194)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1236">架構更新失敗：無法使用 IntId 的值。</span><span class="sxs-lookup"><span data-stu-id="790c2-1236">Schema update failed: No values for msDS-IntId are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**錯誤 \_ DS \_ DUP \_ \_ INTID**</span><span class="sxs-lookup"><span data-stu-id="790c2-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR\_DS\_DUP\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1238">8597 (0x2195) </span><span class="sxs-lookup"><span data-stu-id="790c2-1238">8597 (0x2195)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1239">架構更新失敗：重複的 INtId。</span><span class="sxs-lookup"><span data-stu-id="790c2-1239">Schema update failed: Duplicate msDS-INtId.</span></span> <span data-ttu-id="790c2-1240">重試作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-1240">Retry the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**\_ \_ \_ RDNATTID 中有錯誤 \_ DS**</span><span class="sxs-lookup"><span data-stu-id="790c2-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERROR\_DS\_EXISTS\_IN\_RDNATTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1242">8598 (0x2196) </span><span class="sxs-lookup"><span data-stu-id="790c2-1242">8598 (0x2196)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1243">架構刪除失敗：屬性在 rDNAttID 中使用。</span><span class="sxs-lookup"><span data-stu-id="790c2-1243">Schema deletion failed: attribute is used in rDNAttID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**錯誤 \_ DS \_ 授權 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR\_DS\_AUTHORIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1245">8599 (0x2197) </span><span class="sxs-lookup"><span data-stu-id="790c2-1245">8599 (0x2197)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1246">目錄服務無法授權要求。</span><span class="sxs-lookup"><span data-stu-id="790c2-1246">The directory service failed to authorize the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**錯誤 \_ DS \_ 不正確 \_ 腳本**</span><span class="sxs-lookup"><span data-stu-id="790c2-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR\_DS\_INVALID\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1248">8600 (0x2198) </span><span class="sxs-lookup"><span data-stu-id="790c2-1248">8600 (0x2198)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1249">目錄服務無法處理腳本，因為它無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-1249">The Directory Service cannot process the script because it is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**錯誤 \_ DS \_ 遠端 \_ 交叉交叉操作作業 \_ \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR\_DS\_REMOTE\_CROSSREF\_OP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1251">8601 (0x2199) </span><span class="sxs-lookup"><span data-stu-id="790c2-1251">8601 (0x2199)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1252">網網域命名主機 FSMO 上的遠端建立交互參照操作失敗。</span><span class="sxs-lookup"><span data-stu-id="790c2-1252">The remote create cross reference operation failed on the Domain Naming Master FSMO.</span></span> <span data-ttu-id="790c2-1253">作業的錯誤是在擴充的資料中。</span><span class="sxs-lookup"><span data-stu-id="790c2-1253">The operation's error is in the extended data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**錯誤 \_ DS \_ 交互 \_ 參照 \_ 忙碌**</span><span class="sxs-lookup"><span data-stu-id="790c2-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR\_DS\_CROSS\_REF\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1255">8602 (0x219A) </span><span class="sxs-lookup"><span data-stu-id="790c2-1255">8602 (0x219A)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1256">交互參照在本機使用相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="790c2-1256">A cross reference is in use locally with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**錯誤 \_ DS \_ 無法 \_ 衍生 \_ \_ \_ 已刪除 \_ 網域的 SPN**</span><span class="sxs-lookup"><span data-stu-id="790c2-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_FOR\_DELETED\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1258">8603 (0x219B) </span><span class="sxs-lookup"><span data-stu-id="790c2-1258">8603 (0x219B)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1259">因為伺服器的網域已從樹系中刪除，所以 DS 無法衍生服務主體名稱 (SPN) 用來相互驗證目標伺服器。</span><span class="sxs-lookup"><span data-stu-id="790c2-1259">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the server's domain has been deleted from the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**無法 \_ \_ 使用可 \_ \_ \_ 寫入 NC 降級 \_ 的 DS 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR\_DS\_CANT\_DEMOTE\_WITH\_WRITEABLE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1261">8604 (0x219C) </span><span class="sxs-lookup"><span data-stu-id="790c2-1261">8604 (0x219C)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1262">可寫入的 Nc 會防止此 DC 降級。</span><span class="sxs-lookup"><span data-stu-id="790c2-1262">Writeable NCs prevent this DC from demoting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**\_發現錯誤 DS \_ 重複 \_ 識別碼 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR\_DS\_DUPLICATE\_ID\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1264">8605 (0x219D) </span><span class="sxs-lookup"><span data-stu-id="790c2-1264">8605 (0x219D)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1265">要求的物件具有非唯一的識別碼，因此無法抓取。</span><span class="sxs-lookup"><span data-stu-id="790c2-1265">The requested object has a non-unique identifier and cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**錯誤 \_ DS \_ 沒有 \_ 足夠 \_ 的 ATTR 可 \_ 建立 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR\_DS\_INSUFFICIENT\_ATTR\_TO\_CREATE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1267">8606 (0x219E) </span><span class="sxs-lookup"><span data-stu-id="790c2-1267">8606 (0x219E)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1268">提供的屬性不足，無法建立物件。</span><span class="sxs-lookup"><span data-stu-id="790c2-1268">Insufficient attributes were given to create an object.</span></span> <span data-ttu-id="790c2-1269">此物件可能已被刪除且已進行垃圾收集，因此可能不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-1269">This object may not exist because it may have been deleted and already garbage collected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**錯誤 \_ DS \_ 群組 \_ 轉換 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**ERROR\_DS\_GROUP\_CONVERSION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1271">8607 (0x219F) </span><span class="sxs-lookup"><span data-stu-id="790c2-1271">8607 (0x219F)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1272">因為要求的群組類型上的屬性限制，所以無法轉換群組。</span><span class="sxs-lookup"><span data-stu-id="790c2-1272">The group cannot be converted due to attribute restrictions on the requested group type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 應用程式 \_ 基本 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="790c2-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_BASIC\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1274">8608 (0x21A0) </span><span class="sxs-lookup"><span data-stu-id="790c2-1274">8608 (0x21A0)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1275">不允許跨網域移動非空白的基本應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="790c2-1275">Cross-domain move of non-empty basic application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**錯誤 \_ DS \_ 無法 \_ 移動 \_ 應用程式 \_ 查詢 \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="790c2-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_QUERY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1277">8609 (0x21A1) </span><span class="sxs-lookup"><span data-stu-id="790c2-1277">8609 (0x21A1)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1278">不允許跨網域移動非空白的查詢應用程式群組。</span><span class="sxs-lookup"><span data-stu-id="790c2-1278">Cross-domain move of non-empty query based application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**\_ \_ \_ 未驗證 DS 角色 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERROR\_DS\_ROLE\_NOT\_VERIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1280">8610 (0x21A2) </span><span class="sxs-lookup"><span data-stu-id="790c2-1280">8610 (0x21A2)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1281">無法驗證 FSMO 角色擁有權，因為它的目錄分割未成功地複寫至少一個複寫協力的複本。</span><span class="sxs-lookup"><span data-stu-id="790c2-1281">The FSMO role ownership could not be verified because its directory partition has not replicated successfully with at least one replication partner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**錯誤 \_ DS \_ WKO \_ 容器 \_ 不可 \_ 為 \_ 特殊**</span><span class="sxs-lookup"><span data-stu-id="790c2-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERROR\_DS\_WKO\_CONTAINER\_CANNOT\_BE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1283">8611 (0x21A3) </span><span class="sxs-lookup"><span data-stu-id="790c2-1283">8611 (0x21A3)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1284">已知物件容器重新導向的目標容器不可以是特殊的容器。</span><span class="sxs-lookup"><span data-stu-id="790c2-1284">The target container for a redirection of a well known object container cannot already be a special container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**錯誤 \_ DS \_ 網域 \_ 重新 \_ 命名 \_ 進行中**</span><span class="sxs-lookup"><span data-stu-id="790c2-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR\_DS\_DOMAIN\_RENAME\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1286">8612 (0x21A4) </span><span class="sxs-lookup"><span data-stu-id="790c2-1286">8612 (0x21A4)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1287">目錄服務無法執行要求的作業，因為網域重新命名操作正在進行中。</span><span class="sxs-lookup"><span data-stu-id="790c2-1287">The Directory Service cannot perform the requested operation because a domain rename operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**錯誤 \_ DS \_ 現有的 \_ AD \_ 子 \_ NC**</span><span class="sxs-lookup"><span data-stu-id="790c2-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR\_DS\_EXISTING\_AD\_CHILD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1289">8613 (0x21A5) </span><span class="sxs-lookup"><span data-stu-id="790c2-1289">8613 (0x21A5)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1290">目錄服務在要求的分割區名稱底下偵測到子磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="790c2-1290">The directory service detected a child partition below the requested partition name.</span></span> <span data-ttu-id="790c2-1291">您必須在由上而下的方法中建立資料分割階層。</span><span class="sxs-lookup"><span data-stu-id="790c2-1291">The partition hierarchy must be created in a top down method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**\_超過錯誤 DS 複寫 \_ \_ 存留期 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR\_DS\_REPL\_LIFETIME\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1293">8614 (0x21A6) </span><span class="sxs-lookup"><span data-stu-id="790c2-1293">8614 (0x21A6)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1294">目錄服務無法與此伺服器複寫，因為與此伺服器進行最後一次複寫以來的時間已超過標記存留期。</span><span class="sxs-lookup"><span data-stu-id="790c2-1294">The directory service cannot replicate with this server because the time since the last replication with this server has exceeded the tombstone lifetime.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**\_ \_ \_ \_ 系統容器中不允許的 DS 錯誤 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR\_DS\_DISALLOWED\_IN\_SYSTEM\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1296">8615 (0x21A7) </span><span class="sxs-lookup"><span data-stu-id="790c2-1296">8615 (0x21A7)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1297">系統容器下的物件不允許要求的作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-1297">The requested operation is not allowed on an object under the system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**錯誤 \_ DS \_ LDAP \_ 傳送 \_ 佇列已 \_ 滿**</span><span class="sxs-lookup"><span data-stu-id="790c2-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR\_DS\_LDAP\_SEND\_QUEUE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1299">8616 (0x21A8) </span><span class="sxs-lookup"><span data-stu-id="790c2-1299">8616 (0x21A8)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1300">LDAP 伺服器網路傳送佇列已填滿，因為用戶端未處理其要求的結果速度夠快。</span><span class="sxs-lookup"><span data-stu-id="790c2-1300">The LDAP servers network send queue has filled up because the client is not processing the results of its requests fast enough.</span></span> <span data-ttu-id="790c2-1301">在用戶端趕上之前，將不會再處理任何要求。</span><span class="sxs-lookup"><span data-stu-id="790c2-1301">No more requests will be processed until the client catches up.</span></span> <span data-ttu-id="790c2-1302">如果用戶端未趕上，則會中斷連線。</span><span class="sxs-lookup"><span data-stu-id="790c2-1302">If the client does not catch up then it will be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**錯誤 \_ DS \_ DRA \_ 出 \_ 排程 \_ 視窗**</span><span class="sxs-lookup"><span data-stu-id="790c2-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERROR\_DS\_DRA\_OUT\_SCHEDULE\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1304">8617 (0x21A9) </span><span class="sxs-lookup"><span data-stu-id="790c2-1304">8617 (0x21A9)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1305">因為系統太忙碌而無法在 [排程] 視窗內執行要求，所以未進行排程的複寫。</span><span class="sxs-lookup"><span data-stu-id="790c2-1305">The scheduled replication did not take place because the system was too busy to execute the request within the schedule window.</span></span> <span data-ttu-id="790c2-1306">複寫佇列已超載。</span><span class="sxs-lookup"><span data-stu-id="790c2-1306">The replication queue is overloaded.</span></span> <span data-ttu-id="790c2-1307">請考慮減少夥伴數目或減少排程的複寫頻率。</span><span class="sxs-lookup"><span data-stu-id="790c2-1307">Consider reducing the number of partners or decreasing the scheduled replication frequency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**錯誤 \_ DS \_ 原則 \_ 未知 \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR\_DS\_POLICY\_NOT\_KNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1309">8618 (0x21AA) </span><span class="sxs-lookup"><span data-stu-id="790c2-1309">8618 (0x21AA)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1310">目前無法判斷是否可在中樞網域控制站上使用分支複寫原則。</span><span class="sxs-lookup"><span data-stu-id="790c2-1310">At this time, it cannot be determined if the branch replication policy is available on the hub domain controller.</span></span> <span data-ttu-id="790c2-1311">請稍後再試一次，以考慮複寫延遲。</span><span class="sxs-lookup"><span data-stu-id="790c2-1311">Please retry at a later time to account for replication latencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**錯誤 \_ 的 \_ 網站 \_ 設定 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR\_NO\_SITE\_SETTINGS\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1313">8619 (0x21AB) </span><span class="sxs-lookup"><span data-stu-id="790c2-1313">8619 (0x21AB)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1314">指定網站的網站設定物件不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-1314">The site settings object for the specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**錯誤 \_ 的 \_ 秘密**</span><span class="sxs-lookup"><span data-stu-id="790c2-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR\_NO\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1316">8620 (0x21AC) </span><span class="sxs-lookup"><span data-stu-id="790c2-1316">8620 (0x21AC)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1317">本機帳戶存放區未包含指定之帳戶的秘密內容。</span><span class="sxs-lookup"><span data-stu-id="790c2-1317">The local account store does not contain secret material for the specified account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**錯誤 \_ ， \_ 找不到可寫入 \_ DC \_**</span><span class="sxs-lookup"><span data-stu-id="790c2-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR\_NO\_WRITABLE\_DC\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1319">8621 (0x21AD) </span><span class="sxs-lookup"><span data-stu-id="790c2-1319">8621 (0x21AD)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1320">在網域中找不到可寫入的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="790c2-1320">Could not find a writable domain controller in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**錯誤 \_ DS \_ 沒有 \_ 伺服器 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR\_DS\_NO\_SERVER\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1322">8622 (0x21AE) </span><span class="sxs-lookup"><span data-stu-id="790c2-1322">8622 (0x21AE)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1323">網域控制站的伺服器物件不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-1323">The server object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**錯誤 \_ DS \_ 沒有 \_ NTDSA \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="790c2-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR\_DS\_NO\_NTDSA\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1325">8623 (0x21AF) </span><span class="sxs-lookup"><span data-stu-id="790c2-1325">8623 (0x21AF)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1326">網域控制站的 NTDS 設定物件不存在。</span><span class="sxs-lookup"><span data-stu-id="790c2-1326">The NTDS Settings object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**錯誤 \_ DS \_ 非 \_ ASQ \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="790c2-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR\_DS\_NON\_ASQ\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1328">8624 (0x21B0) </span><span class="sxs-lookup"><span data-stu-id="790c2-1328">8624 (0x21B0)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1329">ASQ 搜尋不支援要求的搜尋作業。</span><span class="sxs-lookup"><span data-stu-id="790c2-1329">The requested search operation is not supported for ASQ searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**錯誤 \_ DS \_ 審核 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR\_DS\_AUDIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1331">8625 (0x21B1) </span><span class="sxs-lookup"><span data-stu-id="790c2-1331">8625 (0x21B1)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1332">無法為作業產生必要的 audit 事件。</span><span class="sxs-lookup"><span data-stu-id="790c2-1332">A required audit event could not be generated for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**錯誤 \_ DS \_ 不正確 \_ 搜尋 \_ 旗標 \_ 子樹**</span><span class="sxs-lookup"><span data-stu-id="790c2-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_SUBTREE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1334">8626 (0x21B2) </span><span class="sxs-lookup"><span data-stu-id="790c2-1334">8626 (0x21B2)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1335">屬性的搜尋旗標無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-1335">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="790c2-1336">子樹索引位只適用于單一值屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-1336">The subtree index bit is valid only on single valued attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**錯誤 \_ DS \_ 不正確 \_ 搜尋 \_ 旗標 \_ 元組**</span><span class="sxs-lookup"><span data-stu-id="790c2-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_TUPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1338">8627 (0x21B3) </span><span class="sxs-lookup"><span data-stu-id="790c2-1338">8627 (0x21B3)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1339">屬性的搜尋旗標無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-1339">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="790c2-1340">元組索引位只有在 Unicode 字串的屬性上才有效。</span><span class="sxs-lookup"><span data-stu-id="790c2-1340">The tuple index bit is valid only on attributes of Unicode strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**錯誤 \_ DS \_ 階層 \_ 資料表 \_ 太 \_ 深**</span><span class="sxs-lookup"><span data-stu-id="790c2-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_TOO\_DEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1342">8628 (0x21B4) </span><span class="sxs-lookup"><span data-stu-id="790c2-1342">8628 (0x21B4)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1343">通訊錄的嵌套太深。</span><span class="sxs-lookup"><span data-stu-id="790c2-1343">The address books are nested too deeply.</span></span> <span data-ttu-id="790c2-1344">無法建立階層資料表。</span><span class="sxs-lookup"><span data-stu-id="790c2-1344">Failed to build the hierarchy table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**\_DS DRA 損毀 \_ \_ \_ UTD \_ 向量錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR\_DS\_DRA\_CORRUPT\_UTD\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1346">8629 (0x21B5) </span><span class="sxs-lookup"><span data-stu-id="790c2-1346">8629 (0x21B5)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1347">指定的最新性質向量已損毀。</span><span class="sxs-lookup"><span data-stu-id="790c2-1347">The specified up-to-date-ness vector is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**\_拒絕 DS \_ DRA \_ 秘密 \_ 的錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR\_DS\_DRA\_SECRETS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1349">8630 (0x21B6) </span><span class="sxs-lookup"><span data-stu-id="790c2-1349">8630 (0x21B6)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1350">複寫秘密的要求遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="790c2-1350">The request to replicate secrets is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**錯誤 \_ DS \_ 保留的 \_ MAPI \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="790c2-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR\_DS\_RESERVED\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1352">8631 (0x21B7) </span><span class="sxs-lookup"><span data-stu-id="790c2-1352">8631 (0x21B7)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1353">架構更新失敗：已保留 MAPI 識別碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-1353">Schema update failed: The MAPI identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**\_ \_ \_ \_ 無法使用錯誤 DS MAPI \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="790c2-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR\_DS\_MAPI\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1355">8632 (0x21B8) </span><span class="sxs-lookup"><span data-stu-id="790c2-1355">8632 (0x21B8)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1356">架構更新失敗：沒有可用的 MAPI 識別碼。</span><span class="sxs-lookup"><span data-stu-id="790c2-1356">Schema update failed: There are no MAPI identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**錯誤 \_ DS \_ DRA \_ 遺失 \_ KRBTGT \_ 秘密**</span><span class="sxs-lookup"><span data-stu-id="790c2-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR\_DS\_DRA\_MISSING\_KRBTGT\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1358">8633 (0x21B9) </span><span class="sxs-lookup"><span data-stu-id="790c2-1358">8633 (0x21B9)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1359">複寫作業失敗，因為遺漏本機 krbtgt 物件的必要屬性。</span><span class="sxs-lookup"><span data-stu-id="790c2-1359">The replication operation failed because the required attributes of the local krbtgt object are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**\_樹系 \_ \_ \_ \_ 中存在 \_ 錯誤 DS 功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="790c2-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR\_DS\_DOMAIN\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1361">8634 (0x21BA) </span><span class="sxs-lookup"><span data-stu-id="790c2-1361">8634 (0x21BA)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1362">樹系中已經有受信任網域的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="790c2-1362">The domain name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**\_樹系 \_ \_ \_ \_ 中存在 \_ 錯誤 DS 一般名稱**</span><span class="sxs-lookup"><span data-stu-id="790c2-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR\_DS\_FLAT\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1364">8635 (0x21BB) </span><span class="sxs-lookup"><span data-stu-id="790c2-1364">8635 (0x21BB)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1365">受信任網域的一般名稱已存在於樹系中。</span><span class="sxs-lookup"><span data-stu-id="790c2-1365">The flat name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**錯誤 \_ 不正確 \_ 使用者 \_ 主體 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="790c2-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR\_INVALID\_USER\_PRINCIPAL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1367">8636 (0x21BC) </span><span class="sxs-lookup"><span data-stu-id="790c2-1367">8636 (0x21BC)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1368"> (UPN) 的使用者主體名稱無效。</span><span class="sxs-lookup"><span data-stu-id="790c2-1368">The User Principal Name (UPN) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**錯誤 \_ DS \_ OID \_ 對應 \_ 群組 \_ 不 \_ 能有 \_ 成員**</span><span class="sxs-lookup"><span data-stu-id="790c2-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR\_DS\_OID\_MAPPED\_GROUP\_CANT\_HAVE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1370">8637 (0x21BD) </span><span class="sxs-lookup"><span data-stu-id="790c2-1370">8637 (0x21BD)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1371">OID 對應的群組不能有成員。</span><span class="sxs-lookup"><span data-stu-id="790c2-1371">OID mapped groups cannot have members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 DS OID**</span><span class="sxs-lookup"><span data-stu-id="790c2-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR\_DS\_OID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1373">8638 (0x21BE) </span><span class="sxs-lookup"><span data-stu-id="790c2-1373">8638 (0x21BE)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1374">找不到指定的 OID。</span><span class="sxs-lookup"><span data-stu-id="790c2-1374">The specified OID cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**\_DS \_ DRA \_ 回收 \_ 目標錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERROR\_DS\_DRA\_RECYCLED\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1376">8639 (0x21BF) </span><span class="sxs-lookup"><span data-stu-id="790c2-1376">8639 (0x21BF)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1377">複寫作業失敗，因為連結值所參考的目標物件已回收。</span><span class="sxs-lookup"><span data-stu-id="790c2-1377">The replication operation failed because the target object referred by a link value is recycled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**錯誤 \_ DS 不 \_ 允許的 NC 重新 \_ \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="790c2-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR\_DS\_DISALLOWED\_NC\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1379">8640 (0x21C0) </span><span class="sxs-lookup"><span data-stu-id="790c2-1379">8640 (0x21C0)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1380">重新導向作業失敗，因為目標物件位於與目前網域控制站的網域 NC 不同的 NC 中。</span><span class="sxs-lookup"><span data-stu-id="790c2-1380">The redirect operation failed because the target object is in a NC different from the domain NC of the current domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR \_ DS \_ HIGH \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="790c2-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR\_DS\_HIGH\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1382">8641 (0x21C1) </span><span class="sxs-lookup"><span data-stu-id="790c2-1382">8641 (0x21C1)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1383">AD LDS 設定集的功能等級無法降到要求的值。</span><span class="sxs-lookup"><span data-stu-id="790c2-1383">The functional level of the AD LDS configuration set cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**錯誤 \_ DS \_ 高 \_ DSA \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="790c2-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR\_DS\_HIGH\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1385">8642 (0x21C2) </span><span class="sxs-lookup"><span data-stu-id="790c2-1385">8642 (0x21C2)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1386">網域 (或樹系) 的功能等級無法降到要求的值。</span><span class="sxs-lookup"><span data-stu-id="790c2-1386">The functional level of the domain (or forest) cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**錯誤 \_ DS \_ 低 \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="790c2-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR\_DS\_LOW\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1388">8643 (0x21C3) </span><span class="sxs-lookup"><span data-stu-id="790c2-1388">8643 (0x21C3)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1389">因為有一或多個 ADLDS 實例位於較不相容的功能等級，所以無法將 AD LDS 設定集的功能層級提升為要求的值。</span><span class="sxs-lookup"><span data-stu-id="790c2-1389">The functional level of the AD LDS configuration set cannot be raised to the requested value, because there exist one or more ADLDS instances that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**\_ \_ \_ \_ 與 \_ 本機工作站相同的 \_ 網域 SID 錯誤**</span><span class="sxs-lookup"><span data-stu-id="790c2-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**ERROR\_DOMAIN\_SID\_SAME\_AS\_LOCAL\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1391">8644 (0x21C4) </span><span class="sxs-lookup"><span data-stu-id="790c2-1391">8644 (0x21C4)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1392">無法完成加入網域，因為您嘗試加入的網域 SID 等同于這部電腦的 SID。</span><span class="sxs-lookup"><span data-stu-id="790c2-1392">The domain join cannot be completed because the SID of the domain you attempted to join was identical to the SID of this machine.</span></span> <span data-ttu-id="790c2-1393">這是作業系統安裝未正確複製的徵兆。</span><span class="sxs-lookup"><span data-stu-id="790c2-1393">This is a symptom of an improperly cloned operating system install.</span></span> <span data-ttu-id="790c2-1394">您應該在這部電腦上執行 sysprep，才能產生新的電腦 SID。</span><span class="sxs-lookup"><span data-stu-id="790c2-1394">You should run sysprep on this machine in order to generate a new machine SID.</span></span> <span data-ttu-id="790c2-1395">請參閱 <https://go.microsoft.com/fwlink/p/?linkid=168895> 以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="790c2-1395">Please see <https://go.microsoft.com/fwlink/p/?linkid=168895> for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**錯誤 \_ DS 取消 \_ 刪除 \_ SAM \_ 驗證 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="790c2-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR\_DS\_UNDELETE\_SAM\_VALIDATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1397">8645 (0x21C5) </span><span class="sxs-lookup"><span data-stu-id="790c2-1397">8645 (0x21C5)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1398">取消刪除作業失敗，因為正在刪除之物件的 Sam 帳戶名稱或其他 Sam 帳戶名稱與現有的即時物件相衝突。</span><span class="sxs-lookup"><span data-stu-id="790c2-1398">The undelete operation failed because the Sam Account Name or Additional Sam Account Name of the object being undeleted conflicts with an existing live object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="790c2-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**錯誤 \_ 的 \_ 帳戶 \_ 類型不正確**</span><span class="sxs-lookup"><span data-stu-id="790c2-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR\_INCORRECT\_ACCOUNT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790c2-1400">8646 (0x21C6) </span><span class="sxs-lookup"><span data-stu-id="790c2-1400">8646 (0x21C6)</span></span>
</dt> <dt>



<span data-ttu-id="790c2-1401">系統不是指定帳戶的授權，因此無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-1401">The system is not authoritative for the specified account and therefore cannot complete the operation.</span></span> <span data-ttu-id="790c2-1402">請使用與此帳戶相關聯的提供者重試操作。</span><span class="sxs-lookup"><span data-stu-id="790c2-1402">Please retry the operation using the provider associated with this account.</span></span> <span data-ttu-id="790c2-1403">如果這是線上提供者，請使用提供者的線上網站。</span><span class="sxs-lookup"><span data-stu-id="790c2-1403">If this is an online provider please use the provider's online site.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="790c2-1404">規格需求</span><span class="sxs-lookup"><span data-stu-id="790c2-1404">Requirements</span></span>



| <span data-ttu-id="790c2-1405">需求</span><span class="sxs-lookup"><span data-stu-id="790c2-1405">Requirement</span></span> | <span data-ttu-id="790c2-1406">值</span><span class="sxs-lookup"><span data-stu-id="790c2-1406">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="790c2-1407">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="790c2-1407">Minimum supported client</span></span><br/> | <span data-ttu-id="790c2-1408">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="790c2-1408">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="790c2-1409">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="790c2-1409">Minimum supported server</span></span><br/> | <span data-ttu-id="790c2-1410">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="790c2-1410">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="790c2-1411">標頭</span><span class="sxs-lookup"><span data-stu-id="790c2-1411">Header</span></span><br/>                   | <dl> <span data-ttu-id="790c2-1412"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="790c2-1412"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="790c2-1413">另請參閱</span><span class="sxs-lookup"><span data-stu-id="790c2-1413">See also</span></span>

<dl> <dt>

[<span data-ttu-id="790c2-1414">系統錯誤碼</span><span class="sxs-lookup"><span data-stu-id="790c2-1414">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




