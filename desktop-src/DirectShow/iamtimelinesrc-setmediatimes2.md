---
description: SetMediaTimes2 方法會設定媒體停止和開始時間。 這個方法相當於 IAMTimelineSrc：： SetMediaTimes，但會接受 REFTIME 的值。
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: 'IAMTimelineSrc：： SetMediaTimes2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4aa4f68a6fb93c329507edceea4e9665bfecd5f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981325"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a><span data-ttu-id="be318-104">IAMTimelineSrc：： SetMediaTimes2 方法</span><span class="sxs-lookup"><span data-stu-id="be318-104">IAMTimelineSrc::SetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="be318-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="be318-105">\[Deprecated.</span></span> <span data-ttu-id="be318-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="be318-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="be318-107">`SetMediaTimes2`方法會設定媒體停止和開始時間。</span><span class="sxs-lookup"><span data-stu-id="be318-107">The `SetMediaTimes2` method sets the media stop and start times.</span></span> <span data-ttu-id="be318-108">這個方法相當於 [**IAMTimelineSrc：： SetMediaTimes**](iamtimelinesrc-setmediatimes.md)，但會接受 [**REFTIME**](reftime.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="be318-108">This method is equivalent to [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="be318-109">語法</span><span class="sxs-lookup"><span data-stu-id="be318-109">Syntax</span></span>


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="be318-110">參數</span><span class="sxs-lookup"><span data-stu-id="be318-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be318-111">*開始*</span><span class="sxs-lookup"><span data-stu-id="be318-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="be318-112">媒體開始時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="be318-112">Media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="be318-113">*停止*</span><span class="sxs-lookup"><span data-stu-id="be318-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="be318-114">媒體停止時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="be318-114">Media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be318-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="be318-115">Return value</span></span>

<span data-ttu-id="be318-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="be318-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be318-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="be318-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be318-118">備註</span><span class="sxs-lookup"><span data-stu-id="be318-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="be318-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="be318-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="be318-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="be318-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="be318-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="be318-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="be318-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="be318-122">Requirements</span></span>



| <span data-ttu-id="be318-123">需求</span><span class="sxs-lookup"><span data-stu-id="be318-123">Requirement</span></span> | <span data-ttu-id="be318-124">值</span><span class="sxs-lookup"><span data-stu-id="be318-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be318-125">標頭</span><span class="sxs-lookup"><span data-stu-id="be318-125">Header</span></span><br/>  | <dl> <span data-ttu-id="be318-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="be318-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="be318-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="be318-127">Library</span></span><br/> | <dl> <span data-ttu-id="be318-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="be318-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be318-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be318-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be318-130">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="be318-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="be318-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="be318-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




