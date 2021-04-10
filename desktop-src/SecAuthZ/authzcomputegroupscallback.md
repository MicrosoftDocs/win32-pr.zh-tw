---
description: 應用程式定義的函式，會建立套用至用戶端 (Sid) 的安全識別碼清單。 AuthzComputeGroupsCallback 是應用程式定義函數名稱的預留位置。
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: AuthzComputeGroupsCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695860"
---
# <a name="authzcomputegroupscallback-callback-function"></a><span data-ttu-id="5f4bb-104">AuthzComputeGroupsCallback 回呼函式</span><span class="sxs-lookup"><span data-stu-id="5f4bb-104">AuthzComputeGroupsCallback callback function</span></span>

<span data-ttu-id="5f4bb-105">**AuthzComputeGroupsCallback** 函式是一種應用程式定義的函式，它會建立適用于用戶端 (sid) 的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly)清單。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-105">The **AuthzComputeGroupsCallback** function is an application-defined function that creates a list of [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that apply to a client.</span></span> <span data-ttu-id="5f4bb-106">**AuthzComputeGroupsCallback** 是應用程式定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-106">**AuthzComputeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f4bb-107">語法</span><span class="sxs-lookup"><span data-stu-id="5f4bb-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a><span data-ttu-id="5f4bb-108">參數</span><span class="sxs-lookup"><span data-stu-id="5f4bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f4bb-109">*hAuthzClientCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f4bb-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4bb-110">用戶端內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="5f4bb-111">*Args* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f4bb-111">*Args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4bb-112">在呼叫 [**AuthzInitializeCoNtextFromAuthzCoNtext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)、 [**AuthzInitializeCoNtextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)或 [**AuthzInitializeCoNtextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)函數的 *DynamicGroupArgs* 參數中傳遞的資料。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-112">Data passed in the *DynamicGroupArgs* parameter of a call to the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid), or [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function.</span></span>

</dd> <dt>

<span data-ttu-id="5f4bb-113">*pSidAttrArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5f4bb-113">*pSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4bb-114">指標變數的指標，此變數會接收 [**SID \_ 和 \_ 屬性**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) 結構陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-114">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="5f4bb-115">這些結構代表用戶端所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-115">These structures represent the groups to which the client belongs.</span></span>

</dd> <dt>

<span data-ttu-id="5f4bb-116">*pSidCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5f4bb-116">*pSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4bb-117">*PSidAttrArray* 中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-117">The number of structures in *pSidAttrArray*.</span></span>

</dd> <dt>

<span data-ttu-id="5f4bb-118">*pRestrictedSidAttrArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5f4bb-118">*pRestrictedSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4bb-119">指標變數的指標，此變數會接收 [**SID \_ 和 \_ 屬性**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) 結構陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-119">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="5f4bb-120">這些結構代表受限於用戶端的群組。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-120">These structures represent the groups from which the client is restricted.</span></span>

</dd> <dt>

<span data-ttu-id="5f4bb-121">*pRestrictedSidCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5f4bb-121">*pRestrictedSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4bb-122">*PSidRestrictedAttrArray* 中的結構數目。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-122">The number of structures in *pSidRestrictedAttrArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f4bb-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f4bb-123">Return value</span></span>

<span data-ttu-id="5f4bb-124">如果函式成功傳回 Sid 清單，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-124">If the function successfully returns a list of SIDs, the return value is **TRUE**.</span></span>

<span data-ttu-id="5f4bb-125">如果函式失敗，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-125">If the function fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f4bb-126">備註</span><span class="sxs-lookup"><span data-stu-id="5f4bb-126">Remarks</span></span>

<span data-ttu-id="5f4bb-127">應用程式也可以藉由呼叫 [**AuthzAddSidsToCoNtext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)，將 sid 新增至用戶端內容。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-127">Applications can also add SIDs to the client context by calling [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span></span>

<span data-ttu-id="5f4bb-128">使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。</span><span class="sxs-lookup"><span data-stu-id="5f4bb-128">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f4bb-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f4bb-129">Requirements</span></span>



| <span data-ttu-id="5f4bb-130">需求</span><span class="sxs-lookup"><span data-stu-id="5f4bb-130">Requirement</span></span> | <span data-ttu-id="5f4bb-131">值</span><span class="sxs-lookup"><span data-stu-id="5f4bb-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="5f4bb-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f4bb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5f4bb-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f4bb-133">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5f4bb-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f4bb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5f4bb-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f4bb-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="5f4bb-136">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5f4bb-136">Redistributable</span></span><br/>          | <span data-ttu-id="5f4bb-137">Windows XP 上的 windows Server 2003 管理工具套件</span><span class="sxs-lookup"><span data-stu-id="5f4bb-137">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f4bb-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f4bb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f4bb-139">基本存取控制功能</span><span class="sxs-lookup"><span data-stu-id="5f4bb-139">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="5f4bb-140">**AuthzAddSidsToCoNtext**</span><span class="sxs-lookup"><span data-stu-id="5f4bb-140">**AuthzAddSidsToContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[<span data-ttu-id="5f4bb-141">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="5f4bb-141">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="5f4bb-142">**AuthzInitializeCoNtextFromAuthzCoNtext**</span><span class="sxs-lookup"><span data-stu-id="5f4bb-142">**AuthzInitializeContextFromAuthzContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[<span data-ttu-id="5f4bb-143">**AuthzInitializeCoNtextFromSid**</span><span class="sxs-lookup"><span data-stu-id="5f4bb-143">**AuthzInitializeContextFromSid**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[<span data-ttu-id="5f4bb-144">**AuthzInitializeCoNtextFromToken**</span><span class="sxs-lookup"><span data-stu-id="5f4bb-144">**AuthzInitializeContextFromToken**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[<span data-ttu-id="5f4bb-145">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="5f4bb-145">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[<span data-ttu-id="5f4bb-146">**SID \_ 和 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="5f4bb-146">**SID\_AND\_ATTRIBUTES**</span></span>](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

