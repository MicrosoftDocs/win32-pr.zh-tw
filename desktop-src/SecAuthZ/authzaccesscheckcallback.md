---
description: 應用程式定義的函式，可處理在存取檢查期間)  (Ace 的回呼存取控制專案。
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: AuthzAccessCheckCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195580"
---
# <a name="authzaccesscheckcallback-callback-function"></a><span data-ttu-id="5bb2d-103">AuthzAccessCheckCallback 回呼函式</span><span class="sxs-lookup"><span data-stu-id="5bb2d-103">AuthzAccessCheckCallback callback function</span></span>

<span data-ttu-id="5bb2d-104">**AuthzAccessCheckCallback** 函式是一種應用程式定義函式，可處理存取檢查期間)  (ace 的回呼 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-104">The **AuthzAccessCheckCallback** function is an application-defined function that handles callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) during an access check.</span></span> <span data-ttu-id="5bb2d-105">**AuthzAccessCheckCallback** 是應用程式定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-105">**AuthzAccessCheckCallback** is a placeholder for the application-defined function name.</span></span> <span data-ttu-id="5bb2d-106">應用程式會藉由呼叫 [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)來註冊此回呼。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-106">The application registers this callback by calling [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb2d-107">語法</span><span class="sxs-lookup"><span data-stu-id="5bb2d-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a><span data-ttu-id="5bb2d-108">參數</span><span class="sxs-lookup"><span data-stu-id="5bb2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bb2d-109">*hAuthzClientCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bb2d-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb2d-110">用戶端內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="5bb2d-111">*步調* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bb2d-111">*pAce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb2d-112">要在呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) 函式時，所要評估的 ACE 指標。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-112">A pointer to the ACE to evaluate for inclusion in the call to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

</dd> <dt>

<span data-ttu-id="5bb2d-113">*pArgs* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5bb2d-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb2d-114">在呼叫 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)或 [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)的 *DynamicGroupArgs* 參數中傳遞的資料。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-114">Data passed in the *DynamicGroupArgs* parameter of the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) or [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span></span>

</dd> <dt>

<span data-ttu-id="5bb2d-115">*pbAceApplicable* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5bb2d-115">*pbAceApplicable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb2d-116">布林值變數的指標，此變數會接收應用程式所定義之邏輯的評估結果。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-116">A pointer to a Boolean variable that receives the results of the evaluation of the logic defined by the application.</span></span>

<span data-ttu-id="5bb2d-117">如果邏輯判斷 ACE 適用且將包含在 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)的呼叫中，則結果為 **TRUE** 。否則，結果為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-117">The results are **TRUE** if the logic determines that the ACE is applicable and will be included in the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); otherwise, the results are **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bb2d-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="5bb2d-118">Return value</span></span>

<span data-ttu-id="5bb2d-119">如果函式成功，函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-119">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="5bb2d-120">如果函數無法執行評估，則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-120">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="5bb2d-121">使用 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) 將錯誤傳回存取檢查函數。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-121">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bb2d-122">備註</span><span class="sxs-lookup"><span data-stu-id="5bb2d-122">Remarks</span></span>

<span data-ttu-id="5bb2d-123">如果在條件運算式中參考，則安全性屬性變數必須存在於用戶端內容中，否則參考它們的條件運算式詞彙將會評估為 unknown。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-123">Security attribute variables must be present in the client context if referred to in a conditional expression, otherwise the conditional expression term referencing them will evaluate to unknown.</span></span>

<span data-ttu-id="5bb2d-124">如需詳細資訊，請參閱 [AccessCheck 的運作方式](how-dacls-control-access-to-an-object.md) 和 [集中式授權原則](centralized-authorization-policy.md) 的總覽。</span><span class="sxs-lookup"><span data-stu-id="5bb2d-124">For more information, see the [How AccessCheck Works](how-dacls-control-access-to-an-object.md) and [Centralized Authorization Policy](centralized-authorization-policy.md) overviews.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb2d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bb2d-125">Requirements</span></span>



| <span data-ttu-id="5bb2d-126">需求</span><span class="sxs-lookup"><span data-stu-id="5bb2d-126">Requirement</span></span> | <span data-ttu-id="5bb2d-127">值</span><span class="sxs-lookup"><span data-stu-id="5bb2d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="5bb2d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5bb2d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5bb2d-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bb2d-129">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5bb2d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5bb2d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5bb2d-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bb2d-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="5bb2d-132">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5bb2d-132">Redistributable</span></span><br/>          | <span data-ttu-id="5bb2d-133">Windows XP 上的 windows Server 2003 管理工具套件</span><span class="sxs-lookup"><span data-stu-id="5bb2d-133">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bb2d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bb2d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb2d-135">基本存取控制功能</span><span class="sxs-lookup"><span data-stu-id="5bb2d-135">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="5bb2d-136">集中式授權原則</span><span class="sxs-lookup"><span data-stu-id="5bb2d-136">Centralized Authorization Policy</span></span>](centralized-authorization-policy.md)
</dt> <dt>

[<span data-ttu-id="5bb2d-137">AccessCheck 的運作方式</span><span class="sxs-lookup"><span data-stu-id="5bb2d-137">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="5bb2d-138">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="5bb2d-138">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[<span data-ttu-id="5bb2d-139">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="5bb2d-139">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="5bb2d-140">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="5bb2d-140">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="5bb2d-141">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="5bb2d-141">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

