---
title: 'IWMDRMLicense GetNext 方法 (Wmdrmsdk .h) '
description: GetNext 方法會載入清單中下一個專案的相關資訊。
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- GetNext 方法 windows Media 格式
- GetNext 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetNext 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992856"
---
# <a name="iwmdrmlicensegetnext-method"></a><span data-ttu-id="190fa-106">IWMDRMLicense：： GetNext 方法</span><span class="sxs-lookup"><span data-stu-id="190fa-106">IWMDRMLicense::GetNext method</span></span>

<span data-ttu-id="190fa-107">**GetNext** 方法會載入清單中下一個專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="190fa-107">The **GetNext** method loads the information about the next item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="190fa-108">語法</span><span class="sxs-lookup"><span data-stu-id="190fa-108">Syntax</span></span>


```C++
HRESULT GetNext();
```



## <a name="parameters"></a><span data-ttu-id="190fa-109">參數</span><span class="sxs-lookup"><span data-stu-id="190fa-109">Parameters</span></span>

<span data-ttu-id="190fa-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="190fa-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="190fa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="190fa-111">Return value</span></span>

<span data-ttu-id="190fa-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="190fa-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="190fa-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="190fa-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="190fa-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="190fa-114">Return code</span></span>                                                                                                | <span data-ttu-id="190fa-115">Description</span><span class="sxs-lookup"><span data-stu-id="190fa-115">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="190fa-116"><dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="190fa-116"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="190fa-117">需要更新的內容撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="190fa-117">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="190fa-118"><dt>**\_沒有 \_ 其他 \_ 專案的錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="190fa-118"><dt>**ERROR\_NO\_MORE\_ITEMS**</dt></span></span> </dl>      | <span data-ttu-id="190fa-119">清單中沒有其他項目了。</span><span class="sxs-lookup"><span data-stu-id="190fa-119">There are no more items in the list.</span></span><br/>          |
| <dl> <span data-ttu-id="190fa-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="190fa-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="190fa-121">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="190fa-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="190fa-122">備註</span><span class="sxs-lookup"><span data-stu-id="190fa-122">Remarks</span></span>

<span data-ttu-id="190fa-123">[**IWMDRMLicense**](iwmdrmlicense.md)介面的方法會一次提供單一授權的相關資料。</span><span class="sxs-lookup"><span data-stu-id="190fa-123">The methods of the [**IWMDRMLicense**](iwmdrmlicense.md) interface provide data about a single license at a time.</span></span> <span data-ttu-id="190fa-124">基礎物件包含一或多個授權的清單。</span><span class="sxs-lookup"><span data-stu-id="190fa-124">The underlying object contains a list of one or more licenses.</span></span> <span data-ttu-id="190fa-125">當您呼叫這個方法時，介面會將其內部參考移至清單中的下一個授權。</span><span class="sxs-lookup"><span data-stu-id="190fa-125">When you call this method, the interface moves its internal references to the next license in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="190fa-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="190fa-126">Requirements</span></span>



| <span data-ttu-id="190fa-127">需求</span><span class="sxs-lookup"><span data-stu-id="190fa-127">Requirement</span></span> | <span data-ttu-id="190fa-128">值</span><span class="sxs-lookup"><span data-stu-id="190fa-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="190fa-129">標頭</span><span class="sxs-lookup"><span data-stu-id="190fa-129">Header</span></span><br/>  | <dl> <span data-ttu-id="190fa-130"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="190fa-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="190fa-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="190fa-131">Library</span></span><br/> | <dl> <span data-ttu-id="190fa-132"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="190fa-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="190fa-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="190fa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="190fa-134">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="190fa-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





