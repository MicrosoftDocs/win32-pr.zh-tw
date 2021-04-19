---
title: 'IWMDRMLicense GetAnalogVideoRestrictionLevels 方法 (Wmdrmsdk .h) '
description: GetAnalogVideoRestrictionLevels 方法會抓取目前授權所設定的所有類比影片限制。
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- GetAnalogVideoRestrictionLevels 方法 windows Media 格式
- GetAnalogVideoRestrictionLevels 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetAnalogVideoRestrictionLevels 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989619"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a><span data-ttu-id="bddc1-106">IWMDRMLicense：： GetAnalogVideoRestrictionLevels 方法</span><span class="sxs-lookup"><span data-stu-id="bddc1-106">IWMDRMLicense::GetAnalogVideoRestrictionLevels method</span></span>

<span data-ttu-id="bddc1-107">**GetAnalogVideoRestrictionLevels** 方法會抓取目前授權所設定的所有類比影片限制。</span><span class="sxs-lookup"><span data-stu-id="bddc1-107">The **GetAnalogVideoRestrictionLevels** method retrieves all analog video restrictions set on the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="bddc1-108">語法</span><span class="sxs-lookup"><span data-stu-id="bddc1-108">Syntax</span></span>


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a><span data-ttu-id="bddc1-109">參數</span><span class="sxs-lookup"><span data-stu-id="bddc1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bddc1-110">*\[ rgAnalogVideoRestrictions \]*\[out\]</span><span class="sxs-lookup"><span data-stu-id="bddc1-110">*rgAnalogVideoRestrictions\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bddc1-111">接收 [**WMDRM \_ 類比 \_ 影片 \_ 限制**](wmdrm-analog-video-restrictions.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="bddc1-111">Receives an array of [**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**](wmdrm-analog-video-restrictions.md) structures.</span></span> <span data-ttu-id="bddc1-112">設定為 **Null** ，以取得 *pcResctrictions* 中陣列的元素數目。</span><span class="sxs-lookup"><span data-stu-id="bddc1-112">Set to **NULL** to get the number of elements in the array in *pcResctrictions*.</span></span>

</dd> <dt>

<span data-ttu-id="bddc1-113">*pcRestrictions* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bddc1-113">*pcRestrictions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bddc1-114">限制陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="bddc1-114">The number of elements in the array of restrictions.</span></span> <span data-ttu-id="bddc1-115">如果 *rgAnalogVideoRestrictions* 設定為 **Null**，則此值會設定為數組中所需的元素數目。</span><span class="sxs-lookup"><span data-stu-id="bddc1-115">If *rgAnalogVideoRestrictions* is set to **NULL**, this value is set to the number of elements needed in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bddc1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bddc1-116">Return value</span></span>

<span data-ttu-id="bddc1-117">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bddc1-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bddc1-118">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="bddc1-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bddc1-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bddc1-119">Return code</span></span>                                                                          | <span data-ttu-id="bddc1-120">Description</span><span class="sxs-lookup"><span data-stu-id="bddc1-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bddc1-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bddc1-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bddc1-122">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="bddc1-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bddc1-123">備註</span><span class="sxs-lookup"><span data-stu-id="bddc1-123">Remarks</span></span>

<span data-ttu-id="bddc1-124">您必須為限制陣列配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="bddc1-124">You must allocate memory for the array of restrictions.</span></span> <span data-ttu-id="bddc1-125">若要這樣做，請先呼叫方法，並將 *rgAnalogVideoRestrictions* 設定為 **Null**，這會將 *pcRestrictions* 的值設定為所需的元素數目。</span><span class="sxs-lookup"><span data-stu-id="bddc1-125">To do so, first call the method with *rgAnalogVideoRestrictions* set to **NULL**, which will set the value at *pcRestrictions* to the number of required elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="bddc1-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="bddc1-126">Requirements</span></span>



| <span data-ttu-id="bddc1-127">需求</span><span class="sxs-lookup"><span data-stu-id="bddc1-127">Requirement</span></span> | <span data-ttu-id="bddc1-128">值</span><span class="sxs-lookup"><span data-stu-id="bddc1-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bddc1-129">標頭</span><span class="sxs-lookup"><span data-stu-id="bddc1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bddc1-130"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="bddc1-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="bddc1-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="bddc1-131">Library</span></span><br/> | <dl> <span data-ttu-id="bddc1-132"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bddc1-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bddc1-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bddc1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddc1-134">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="bddc1-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





