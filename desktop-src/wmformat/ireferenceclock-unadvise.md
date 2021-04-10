---
title: IReferenceClock Unadvise 方法
description: Unadvise 方法會取消通知要求。
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Unadvise 方法 windows Media 格式
- Unadvise 方法 windows Media Format，IReferenceClock 介面
- IReferenceClock 介面 windows Media Format，Unadvise 方法
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092416"
---
# <a name="ireferenceclockunadvise-method"></a><span data-ttu-id="b645f-106">IReferenceClock：： Unadvise 方法</span><span class="sxs-lookup"><span data-stu-id="b645f-106">IReferenceClock::Unadvise method</span></span>

<span data-ttu-id="b645f-107">**Unadvise** 方法會取消通知要求。</span><span class="sxs-lookup"><span data-stu-id="b645f-107">The **Unadvise** method cancels a notification request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b645f-108">語法</span><span class="sxs-lookup"><span data-stu-id="b645f-108">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="b645f-109">參數</span><span class="sxs-lookup"><span data-stu-id="b645f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b645f-110">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="b645f-110">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="b645f-111">要移除之要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b645f-111">Identifier of the request to remove.</span></span> <span data-ttu-id="b645f-112">使用 AdviseTime 在 pdwAdviseCookie 參數中所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="b645f-112">Use the value returned by AdviseTime in the pdwAdviseCookie parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b645f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b645f-113">Return value</span></span>

<span data-ttu-id="b645f-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="b645f-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b645f-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="b645f-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b645f-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b645f-116">Return code</span></span>                                                                             | <span data-ttu-id="b645f-117">Description</span><span class="sxs-lookup"><span data-stu-id="b645f-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="b645f-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b645f-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b645f-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="b645f-119">The method succeeded.</span></span><br/>                    |
| <dl> <span data-ttu-id="b645f-120"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="b645f-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b645f-121">傳入的識別碼不存在。</span><span class="sxs-lookup"><span data-stu-id="b645f-121">The identifier passed in does not exist.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="b645f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b645f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b645f-123">**IReferenceClock 介面**</span><span class="sxs-lookup"><span data-stu-id="b645f-123">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





