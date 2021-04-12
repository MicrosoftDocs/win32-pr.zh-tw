---
description: AuthzFreeCentralAccessPolicyCallback 函式是應用程式定義的函式，可釋出由 AuthzGetCentralAccessPolicyCallback 函數配置的記憶體。
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: AuthzFreeCentralAccessPolicyCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195578"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a><span data-ttu-id="d5808-103">AuthzFreeCentralAccessPolicyCallback 回呼函式</span><span class="sxs-lookup"><span data-stu-id="d5808-103">AuthzFreeCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="d5808-104">*AuthzFreeCentralAccessPolicyCallback* 函式是應用程式定義的函式，可釋出由 [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)函數配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d5808-104">The *AuthzFreeCentralAccessPolicyCallback* function is an application-defined function that frees memory allocated by the [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) function.</span></span> <span data-ttu-id="d5808-105">*AuthzFreeCentralAccessPolicyCallback* 是應用程式定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="d5808-105">*AuthzFreeCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5808-106">語法</span><span class="sxs-lookup"><span data-stu-id="d5808-106">Syntax</span></span>


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="d5808-107">參數</span><span class="sxs-lookup"><span data-stu-id="d5808-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5808-108">*pCentralAccessPolicy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5808-108">*pCentralAccessPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5808-109">要釋放的集中存取原則指標。</span><span class="sxs-lookup"><span data-stu-id="d5808-109">Pointer to the central access policy to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5808-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5808-110">Return value</span></span>

<span data-ttu-id="d5808-111">如果函式成功，函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d5808-111">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="d5808-112">如果函數無法執行評估，則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d5808-112">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="d5808-113">使用 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) 將錯誤傳回存取檢查函數。</span><span class="sxs-lookup"><span data-stu-id="d5808-113">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5808-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5808-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5808-115">**AUTHZ \_ INIT \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="d5808-115">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="d5808-116">*AuthzGetCentralAccessPolicyCallback*</span><span class="sxs-lookup"><span data-stu-id="d5808-116">*AuthzGetCentralAccessPolicyCallback*</span></span>](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
