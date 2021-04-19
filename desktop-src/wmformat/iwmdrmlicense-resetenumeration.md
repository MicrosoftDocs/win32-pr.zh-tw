---
title: 'IWMDRMLicense ResetEnumeration 方法 (Wmdrmsdk .h) '
description: ResetEnumeration 方法會將授權清單重設為其原始狀態。 作用中的授權會成為清單中的第一個授權。
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- ResetEnumeration 方法 windows Media 格式
- ResetEnumeration 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，ResetEnumeration 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982999"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a><span data-ttu-id="191a8-107">IWMDRMLicense：： ResetEnumeration 方法</span><span class="sxs-lookup"><span data-stu-id="191a8-107">IWMDRMLicense::ResetEnumeration method</span></span>

<span data-ttu-id="191a8-108">**ResetEnumeration** 方法會將授權清單重設為其原始狀態。</span><span class="sxs-lookup"><span data-stu-id="191a8-108">The **ResetEnumeration** method resets the license list to its original state.</span></span> <span data-ttu-id="191a8-109">作用中的授權會成為清單中的第一個授權。</span><span class="sxs-lookup"><span data-stu-id="191a8-109">The active license becomes the first license in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="191a8-110">語法</span><span class="sxs-lookup"><span data-stu-id="191a8-110">Syntax</span></span>


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a><span data-ttu-id="191a8-111">參數</span><span class="sxs-lookup"><span data-stu-id="191a8-111">Parameters</span></span>

<span data-ttu-id="191a8-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="191a8-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="191a8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="191a8-113">Return value</span></span>

<span data-ttu-id="191a8-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="191a8-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="191a8-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="191a8-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="191a8-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="191a8-116">Return code</span></span>                                                                                                | <span data-ttu-id="191a8-117">Description</span><span class="sxs-lookup"><span data-stu-id="191a8-117">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="191a8-118"><dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="191a8-118"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="191a8-119">需要更新的內容撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="191a8-119">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="191a8-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="191a8-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="191a8-121">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="191a8-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="191a8-122">備註</span><span class="sxs-lookup"><span data-stu-id="191a8-122">Remarks</span></span>

<span data-ttu-id="191a8-123">無。</span><span class="sxs-lookup"><span data-stu-id="191a8-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="191a8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="191a8-124">Requirements</span></span>



| <span data-ttu-id="191a8-125">需求</span><span class="sxs-lookup"><span data-stu-id="191a8-125">Requirement</span></span> | <span data-ttu-id="191a8-126">值</span><span class="sxs-lookup"><span data-stu-id="191a8-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="191a8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="191a8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="191a8-128"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="191a8-128"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="191a8-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="191a8-129">Library</span></span><br/> | <dl> <span data-ttu-id="191a8-130"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="191a8-130"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="191a8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="191a8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="191a8-132">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="191a8-132">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





