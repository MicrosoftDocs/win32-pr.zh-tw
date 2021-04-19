---
description: FixMediaTimes2 方法會將指定的時間值四捨五入到最接近的框架界限（如輸出畫面播放速率所定義）。 這個方法相當於 IAMTimelineSrc：： FixMediaTimes，但會接受 REFTIME 的值。
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: 'IAMTimelineSrc：： FixMediaTimes2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e38b6c1ea4c49372a52a805920fa95ccf795f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986158"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a><span data-ttu-id="f89a9-104">IAMTimelineSrc：： FixMediaTimes2 方法</span><span class="sxs-lookup"><span data-stu-id="f89a9-104">IAMTimelineSrc::FixMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="f89a9-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="f89a9-105">\[Deprecated.</span></span> <span data-ttu-id="f89a9-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="f89a9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f89a9-107">方法會將 `FixMediaTimes2` 指定的時間值四捨五入到最接近的框架界限（如輸出畫面播放速率所定義）。</span><span class="sxs-lookup"><span data-stu-id="f89a9-107">The `FixMediaTimes2` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="f89a9-108">這個方法相當於 [**IAMTimelineSrc：： FixMediaTimes**](iamtimelinesrc-fixmediatimes.md)，但會接受 [**REFTIME**](reftime.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="f89a9-108">This method is equivalent to [**IAMTimelineSrc::FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="f89a9-109">語法</span><span class="sxs-lookup"><span data-stu-id="f89a9-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="f89a9-110">參數</span><span class="sxs-lookup"><span data-stu-id="f89a9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f89a9-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="f89a9-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f89a9-112">包含開始時間（以秒為單位）之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="f89a9-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="f89a9-113">如果呼叫成功，這個變數會設定為舍入時間。</span><span class="sxs-lookup"><span data-stu-id="f89a9-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="f89a9-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="f89a9-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="f89a9-115">包含停止時間（以秒為單位）之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="f89a9-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="f89a9-116">如果呼叫成功，這個變數會設定為舍入時間。</span><span class="sxs-lookup"><span data-stu-id="f89a9-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f89a9-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f89a9-117">Return value</span></span>

<span data-ttu-id="f89a9-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f89a9-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f89a9-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f89a9-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f89a9-120">備註</span><span class="sxs-lookup"><span data-stu-id="f89a9-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f89a9-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="f89a9-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f89a9-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="f89a9-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f89a9-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="f89a9-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f89a9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f89a9-124">Requirements</span></span>



| <span data-ttu-id="f89a9-125">需求</span><span class="sxs-lookup"><span data-stu-id="f89a9-125">Requirement</span></span> | <span data-ttu-id="f89a9-126">值</span><span class="sxs-lookup"><span data-stu-id="f89a9-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f89a9-127">標頭</span><span class="sxs-lookup"><span data-stu-id="f89a9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f89a9-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="f89a9-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f89a9-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="f89a9-129">Library</span></span><br/> | <dl> <span data-ttu-id="f89a9-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f89a9-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f89a9-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f89a9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f89a9-132">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="f89a9-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="f89a9-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="f89a9-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




