---
title: 'IWMDRMLicense PersistLicense 方法 (Wmdrmsdk .h) '
description: PersistLicense 方法會將目前的授權從暫時存放區儲存到永久的本機授權存放區。
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- PersistLicense 方法 windows Media 格式
- PersistLicense 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，PersistLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987105"
---
# <a name="iwmdrmlicensepersistlicense-method"></a><span data-ttu-id="86687-106">IWMDRMLicense：:P ersistLicense 方法</span><span class="sxs-lookup"><span data-stu-id="86687-106">IWMDRMLicense::PersistLicense method</span></span>

<span data-ttu-id="86687-107">**PersistLicense** 方法會將目前的授權從暫時存放區儲存到永久的本機授權存放區。</span><span class="sxs-lookup"><span data-stu-id="86687-107">The **PersistLicense** method saves the current license from the temporary store into the permanent local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="86687-108">語法</span><span class="sxs-lookup"><span data-stu-id="86687-108">Syntax</span></span>


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a><span data-ttu-id="86687-109">參數</span><span class="sxs-lookup"><span data-stu-id="86687-109">Parameters</span></span>

<span data-ttu-id="86687-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="86687-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86687-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="86687-111">Return value</span></span>

<span data-ttu-id="86687-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="86687-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="86687-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="86687-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="86687-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="86687-114">Return code</span></span>                                                                          | <span data-ttu-id="86687-115">Description</span><span class="sxs-lookup"><span data-stu-id="86687-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="86687-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="86687-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="86687-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="86687-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86687-118">備註</span><span class="sxs-lookup"><span data-stu-id="86687-118">Remarks</span></span>

<span data-ttu-id="86687-119">如果目前的授權不在暫存存放區中，此方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="86687-119">If the current license is not in the temporary store, this method will fail.</span></span>

<span data-ttu-id="86687-120">您可以呼叫 [**CanPersist**](iwmdrmlicense-canpersist.md) 來查詢是否允許保存授權。</span><span class="sxs-lookup"><span data-stu-id="86687-120">You can call [**CanPersist**](iwmdrmlicense-canpersist.md) to query whether the license is allowed to be persisted.</span></span>

## <a name="requirements"></a><span data-ttu-id="86687-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="86687-121">Requirements</span></span>



| <span data-ttu-id="86687-122">需求</span><span class="sxs-lookup"><span data-stu-id="86687-122">Requirement</span></span> | <span data-ttu-id="86687-123">值</span><span class="sxs-lookup"><span data-stu-id="86687-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86687-124">標頭</span><span class="sxs-lookup"><span data-stu-id="86687-124">Header</span></span><br/> | <dl> <span data-ttu-id="86687-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="86687-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86687-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86687-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86687-127">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="86687-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





