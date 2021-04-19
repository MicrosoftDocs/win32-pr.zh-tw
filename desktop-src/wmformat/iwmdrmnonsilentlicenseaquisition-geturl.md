---
title: 'IWMDRMNonSilentLicenseAquisition GetURL 方法 (Wmdrmsdk .h) '
description: GetURL 方法會抓取授權挑戰應張貼至其中的 URL。
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- GetURL 方法 windows Media 格式
- GetURL 方法 windows Media Format，IWMDRMNonSilentLicenseAquisition 介面
- IWMDRMNonSilentLicenseAquisition 介面 windows Media Format，GetURL 方法
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998596"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a><span data-ttu-id="434d8-106">IWMDRMNonSilentLicenseAquisition：： GetURL 方法</span><span class="sxs-lookup"><span data-stu-id="434d8-106">IWMDRMNonSilentLicenseAquisition::GetURL method</span></span>

<span data-ttu-id="434d8-107">**GetURL** 方法會抓取授權挑戰應張貼至其中的 URL。</span><span class="sxs-lookup"><span data-stu-id="434d8-107">The **GetURL** method retrieves the URL to which the license challenge should be posted.</span></span>

## <a name="syntax"></a><span data-ttu-id="434d8-108">語法</span><span class="sxs-lookup"><span data-stu-id="434d8-108">Syntax</span></span>


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a><span data-ttu-id="434d8-109">參數</span><span class="sxs-lookup"><span data-stu-id="434d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434d8-110">*pbstrURL* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="434d8-110">*pbstrURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="434d8-111">接收 URL 之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="434d8-111">Address of a variable that receives the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434d8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="434d8-112">Return value</span></span>

<span data-ttu-id="434d8-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="434d8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="434d8-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="434d8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="434d8-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="434d8-115">Return code</span></span>                                                                          | <span data-ttu-id="434d8-116">Description</span><span class="sxs-lookup"><span data-stu-id="434d8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="434d8-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="434d8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="434d8-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="434d8-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="434d8-119">備註</span><span class="sxs-lookup"><span data-stu-id="434d8-119">Remarks</span></span>

<span data-ttu-id="434d8-120">無。</span><span class="sxs-lookup"><span data-stu-id="434d8-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="434d8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="434d8-121">Requirements</span></span>



| <span data-ttu-id="434d8-122">需求</span><span class="sxs-lookup"><span data-stu-id="434d8-122">Requirement</span></span> | <span data-ttu-id="434d8-123">值</span><span class="sxs-lookup"><span data-stu-id="434d8-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="434d8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="434d8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="434d8-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="434d8-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="434d8-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="434d8-126">Library</span></span><br/> | <dl> <span data-ttu-id="434d8-127"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="434d8-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="434d8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="434d8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434d8-129">**IWMDRMNonSilentLicenseAquisition 介面**</span><span class="sxs-lookup"><span data-stu-id="434d8-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





