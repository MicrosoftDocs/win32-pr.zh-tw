---
title: 'IWMDRMIndividualizationStatus GetStatus 方法 (Wmdrmsdk .h) '
description: GetStatus 方法會抓取有關「個人化進度」的詳細資訊。
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- GetStatus 方法 windows Media 格式
- GetStatus 方法 windows Media Format，IWMDRMIndividualizationStatus 介面
- IWMDRMIndividualizationStatus 介面 windows Media Format，GetStatus 方法
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994104"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a><span data-ttu-id="f4584-106">IWMDRMIndividualizationStatus：： GetStatus 方法</span><span class="sxs-lookup"><span data-stu-id="f4584-106">IWMDRMIndividualizationStatus::GetStatus method</span></span>

<span data-ttu-id="f4584-107">**GetStatus** 方法會抓取有關「個人化進度」的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f4584-107">The **GetStatus** method retrieves detailed information about individualization progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4584-108">語法</span><span class="sxs-lookup"><span data-stu-id="f4584-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f4584-109">參數</span><span class="sxs-lookup"><span data-stu-id="f4584-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4584-110">*pStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f4584-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4584-111">接收 [**WM \_ 賦予 \_ 狀態**](drmwm-individualize-status.md) 結構，其中包含有關「個人化嘗試」狀態的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f4584-111">Receives a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure containing detailed information about the status of the individualization attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4584-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4584-112">Return value</span></span>

<span data-ttu-id="f4584-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f4584-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f4584-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f4584-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f4584-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f4584-115">Return code</span></span>                                                                          | <span data-ttu-id="f4584-116">Description</span><span class="sxs-lookup"><span data-stu-id="f4584-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f4584-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f4584-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f4584-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f4584-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4584-119">備註</span><span class="sxs-lookup"><span data-stu-id="f4584-119">Remarks</span></span>

<span data-ttu-id="f4584-120">無。</span><span class="sxs-lookup"><span data-stu-id="f4584-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4584-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4584-121">Requirements</span></span>



| <span data-ttu-id="f4584-122">需求</span><span class="sxs-lookup"><span data-stu-id="f4584-122">Requirement</span></span> | <span data-ttu-id="f4584-123">值</span><span class="sxs-lookup"><span data-stu-id="f4584-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4584-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f4584-124">Header</span></span><br/> | <dl> <span data-ttu-id="f4584-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4584-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4584-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4584-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4584-127">**IWMDRMIndividualizationStatus 介面**</span><span class="sxs-lookup"><span data-stu-id="f4584-127">**IWMDRMIndividualizationStatus Interface**</span></span>](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





