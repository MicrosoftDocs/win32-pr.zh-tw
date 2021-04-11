---
description: 叫用指定的非同步作業報告進度時，所呼叫的方法。
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: IAsyncOperationWithProgressCompletedHandler<TResult，TProgress>：： Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113120"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a><span data-ttu-id="1fd73-103">IAsyncOperationWithProgressCompletedHandler<TResult，TProgress>：： Invoke 方法</span><span class="sxs-lookup"><span data-stu-id="1fd73-103">IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke method</span></span>

<span data-ttu-id="1fd73-104">叫用指定的非同步作業報告進度時，所呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="1fd73-104">Invokes the method that is called when the specified asynchronous operation reports progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd73-105">語法</span><span class="sxs-lookup"><span data-stu-id="1fd73-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1fd73-106">參數</span><span class="sxs-lookup"><span data-stu-id="1fd73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fd73-107">*system.runtime.interopservices.windowsruntime.asyncinfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1fd73-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fd73-108">Type： \**[**IAsyncOperationWithProgress<TResult，TProgress>**](/previous-versions//br205807(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="1fd73-108">Type: \**[**IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\** _</span></span>

<span data-ttu-id="1fd73-109">報告完成的非同步動作。</span><span class="sxs-lookup"><span data-stu-id="1fd73-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fd73-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fd73-110">Return value</span></span>

<span data-ttu-id="1fd73-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1fd73-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1fd73-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1fd73-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1fd73-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1fd73-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd73-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fd73-114">Requirements</span></span>



| <span data-ttu-id="1fd73-115">需求</span><span class="sxs-lookup"><span data-stu-id="1fd73-115">Requirement</span></span> | <span data-ttu-id="1fd73-116">值</span><span class="sxs-lookup"><span data-stu-id="1fd73-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1fd73-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fd73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd73-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1fd73-118">Windows 8</span></span><br/>           |
| <span data-ttu-id="1fd73-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fd73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd73-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fd73-120">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fd73-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fd73-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="1fd73-122">[**IAsyncOperationWithProgressCompletedHandler<TResult，TProgress>**](/previous-versions//br205808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1fd73-122">[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))</span></span>
</dt> </dl>

 

 
