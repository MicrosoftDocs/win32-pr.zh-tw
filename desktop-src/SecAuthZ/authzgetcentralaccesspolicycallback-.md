---
description: AuthzGetCentralAccessPolicyCallback 函式是可取得集中存取原則的應用程式定義函數。 AuthzGetCentralAccessPolicyCallback 是應用程式定義函數名稱的預留位置。
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: AuthzGetCentralAccessPolicyCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976376"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a><span data-ttu-id="9622c-104">AuthzGetCentralAccessPolicyCallback 回呼函式</span><span class="sxs-lookup"><span data-stu-id="9622c-104">AuthzGetCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="9622c-105">*AuthzGetCentralAccessPolicyCallback* 函式是可取得集中存取原則的應用程式定義函數。</span><span class="sxs-lookup"><span data-stu-id="9622c-105">The *AuthzGetCentralAccessPolicyCallback* function is an application-defined function that retrieves the central access policy.</span></span> <span data-ttu-id="9622c-106">*AuthzGetCentralAccessPolicyCallback* 是應用程式定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="9622c-106">*AuthzGetCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="9622c-107">語法</span><span class="sxs-lookup"><span data-stu-id="9622c-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="9622c-108">參數</span><span class="sxs-lookup"><span data-stu-id="9622c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9622c-109">*hAuthzClientCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9622c-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9622c-110">用戶端內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9622c-110">Handle to the client context.</span></span>

</dd> <dt>

<span data-ttu-id="9622c-111">*capid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9622c-111">*capid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9622c-112">要取出的集中存取原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="9622c-112">ID of the central access policy to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9622c-113">*pArgs* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9622c-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9622c-114">透過 [**AUTHZ \_ 存取 \_ 要求**](/windows/desktop/api/Authz/ns-authz-authz_access_request)結構的 **OptionalArguments** 成員傳遞至 [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)函數的選擇性引數。</span><span class="sxs-lookup"><span data-stu-id="9622c-114">Optional arguments that were passed to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function through the **OptionalArguments** member of the [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9622c-115">*pCentralAccessPolicyApplicable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9622c-115">*pCentralAccessPolicyApplicable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9622c-116">指向布林值的指標，資源管理員會使用這個值指出是否應該在存取評估期間使用集中存取原則。</span><span class="sxs-lookup"><span data-stu-id="9622c-116">Pointer to a Boolean value that the resource manager uses to indicate whether a central access policy should be used during access evaluation.</span></span>

</dd> <dt>

<span data-ttu-id="9622c-117">*ppCentralAccessPolicy* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9622c-117">*ppCentralAccessPolicy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9622c-118">用來評估存取權的集中存取原則 (端點) 的指標。</span><span class="sxs-lookup"><span data-stu-id="9622c-118">Pointer to the central access policy (CAP) to be used for evaluating access.</span></span> <span data-ttu-id="9622c-119">如果這個值為 **Null**，則會套用預設上限。</span><span class="sxs-lookup"><span data-stu-id="9622c-119">If this value is **NULL**, the default CAP is applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9622c-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="9622c-120">Return value</span></span>

<span data-ttu-id="9622c-121">如果函式成功，函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9622c-121">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="9622c-122">如果函數無法執行評估，則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9622c-122">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="9622c-123">使用 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) 將錯誤傳回存取檢查函數。</span><span class="sxs-lookup"><span data-stu-id="9622c-123">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9622c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="9622c-124">Requirements</span></span>



| <span data-ttu-id="9622c-125">需求</span><span class="sxs-lookup"><span data-stu-id="9622c-125">Requirement</span></span> | <span data-ttu-id="9622c-126">值</span><span class="sxs-lookup"><span data-stu-id="9622c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="9622c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9622c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9622c-128">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9622c-128">Windows 8 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9622c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9622c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9622c-130">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9622c-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="9622c-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9622c-131">Redistributable</span></span><br/>          | <span data-ttu-id="9622c-132">Windows XP 上的 windows Server 2003 管理工具套件</span><span class="sxs-lookup"><span data-stu-id="9622c-132">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9622c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9622c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9622c-134">**AUTHZ \_ 存取 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="9622c-134">**AUTHZ\_ACCESS\_REQUEST**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[<span data-ttu-id="9622c-135">**AUTHZ \_ INIT \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="9622c-135">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="9622c-136">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="9622c-136">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

