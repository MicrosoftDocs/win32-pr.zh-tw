---
description: GetRange 方法會取得指定之資料流程品質屬性的有效值範圍。
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: 'ITStreamQualityControl：： GetRange 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea8b20c2617eb0fe54ccc4603997464fca25f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977742"
---
# <a name="itstreamqualitycontrolgetrange-method"></a><span data-ttu-id="071aa-103">ITStreamQualityControl：： GetRange 方法</span><span class="sxs-lookup"><span data-stu-id="071aa-103">ITStreamQualityControl::GetRange method</span></span>

<span data-ttu-id="071aa-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="071aa-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="071aa-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="071aa-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="071aa-106">**GetRange** 方法會取得指定之 [**資料流程品質屬性**](streamqualityproperty.md)的有效值範圍。</span><span class="sxs-lookup"><span data-stu-id="071aa-106">The **GetRange** method gets the range of valid values for a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="071aa-107">語法</span><span class="sxs-lookup"><span data-stu-id="071aa-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="071aa-108">參數</span><span class="sxs-lookup"><span data-stu-id="071aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="071aa-109">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="071aa-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="071aa-110">[**StreamQualityProperty**](streamqualityproperty.md)列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="071aa-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="071aa-111">*plMin* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="071aa-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="071aa-112">輸入屬性的最小有效值。</span><span class="sxs-lookup"><span data-stu-id="071aa-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="071aa-113">*plMax* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="071aa-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="071aa-114">輸入屬性的最大有效值。</span><span class="sxs-lookup"><span data-stu-id="071aa-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="071aa-115">*plSteppingDelta* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="071aa-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="071aa-116">可以增加或減少屬性值的遞增量。</span><span class="sxs-lookup"><span data-stu-id="071aa-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="071aa-117">*plDefault* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="071aa-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="071aa-118">*Property* 參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="071aa-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="071aa-119">*plFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="071aa-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="071aa-120">[**TAPIControlFlags**](tapicontrolflags.md)列舉的值，指出 *屬性* 值的控制方式。</span><span class="sxs-lookup"><span data-stu-id="071aa-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="071aa-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="071aa-121">Return value</span></span>

<span data-ttu-id="071aa-122">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="071aa-122">This method can return one of these values.</span></span>



| <span data-ttu-id="071aa-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="071aa-123">Return code</span></span>                                                                                   | <span data-ttu-id="071aa-124">Description</span><span class="sxs-lookup"><span data-stu-id="071aa-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="071aa-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="071aa-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="071aa-126">方法成功。</span><span class="sxs-lookup"><span data-stu-id="071aa-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="071aa-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="071aa-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="071aa-128">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="071aa-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="071aa-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="071aa-129">Requirements</span></span>



| <span data-ttu-id="071aa-130">需求</span><span class="sxs-lookup"><span data-stu-id="071aa-130">Requirement</span></span> | <span data-ttu-id="071aa-131">值</span><span class="sxs-lookup"><span data-stu-id="071aa-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="071aa-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="071aa-132">TAPI version</span></span><br/> | <span data-ttu-id="071aa-133">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="071aa-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="071aa-134">標頭</span><span class="sxs-lookup"><span data-stu-id="071aa-134">Header</span></span><br/>       | <dl> <span data-ttu-id="071aa-135"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="071aa-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="071aa-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="071aa-136">Library</span></span><br/>      | <dl> <span data-ttu-id="071aa-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="071aa-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="071aa-138">DLL</span><span class="sxs-lookup"><span data-stu-id="071aa-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="071aa-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="071aa-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="071aa-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="071aa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071aa-141">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="071aa-141">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="071aa-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="071aa-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="071aa-143">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="071aa-143">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




