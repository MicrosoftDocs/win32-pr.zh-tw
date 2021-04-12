---
description: 釋放 AuthzComputeGroupsCallback 函式所配置記憶體的應用程式定義函數。 AuthzFreeGroupsCallback 是應用程式定義函數名稱的預留位置。
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: AuthzFreeGroupsCallback 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695859"
---
# <a name="authzfreegroupscallback-callback-function"></a><span data-ttu-id="63188-104">AuthzFreeGroupsCallback 回呼函式</span><span class="sxs-lookup"><span data-stu-id="63188-104">AuthzFreeGroupsCallback callback function</span></span>

<span data-ttu-id="63188-105">**AuthzFreeGroupsCallback** 函式是應用程式定義的函式，可釋出由 [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)函數配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="63188-105">The **AuthzFreeGroupsCallback** function is an application-defined function that frees memory allocated by the [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) function.</span></span> <span data-ttu-id="63188-106">**AuthzFreeGroupsCallback** 是應用程式定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="63188-106">**AuthzFreeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="63188-107">語法</span><span class="sxs-lookup"><span data-stu-id="63188-107">Syntax</span></span>


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a><span data-ttu-id="63188-108">參數</span><span class="sxs-lookup"><span data-stu-id="63188-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63188-109">*pSidAttrArray* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63188-109">*pSidAttrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63188-110">[**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)所配置之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="63188-110">A pointer to memory allocated by [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63188-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="63188-111">Return value</span></span>

<span data-ttu-id="63188-112">這個回呼函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="63188-112">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63188-113">備註</span><span class="sxs-lookup"><span data-stu-id="63188-113">Remarks</span></span>

<span data-ttu-id="63188-114">使用邏輯運算子時，屬性變數的格式必須是運算式;否則會評估為 unknown。</span><span class="sxs-lookup"><span data-stu-id="63188-114">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="63188-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="63188-115">Requirements</span></span>



| <span data-ttu-id="63188-116">需求</span><span class="sxs-lookup"><span data-stu-id="63188-116">Requirement</span></span> | <span data-ttu-id="63188-117">值</span><span class="sxs-lookup"><span data-stu-id="63188-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="63188-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63188-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63188-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63188-119">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="63188-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63188-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63188-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63188-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="63188-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="63188-122">Redistributable</span></span><br/>          | <span data-ttu-id="63188-123">Windows XP 上的 windows Server 2003 管理工具套件</span><span class="sxs-lookup"><span data-stu-id="63188-123">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63188-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63188-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63188-125">基本存取控制功能</span><span class="sxs-lookup"><span data-stu-id="63188-125">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="63188-126">**AuthzComputeGroupsCallback**</span><span class="sxs-lookup"><span data-stu-id="63188-126">**AuthzComputeGroupsCallback**</span></span>](authzcomputegroupscallback.md)
</dt> </dl>

 

 




