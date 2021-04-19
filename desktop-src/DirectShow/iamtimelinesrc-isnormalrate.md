---
description: IsNormalRate 方法會指出剪輯是否會以正常播放速率播放;也就是原始檔案的播放速度。
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'IAMTimelineSrc：： IsNormalRate 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993541"
---
# <a name="iamtimelinesrcisnormalrate-method"></a><span data-ttu-id="da8ed-103">IAMTimelineSrc：： IsNormalRate 方法</span><span class="sxs-lookup"><span data-stu-id="da8ed-103">IAMTimelineSrc::IsNormalRate method</span></span>

> [!Note]  
> <span data-ttu-id="da8ed-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="da8ed-104">\[Deprecated.</span></span> <span data-ttu-id="da8ed-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="da8ed-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="da8ed-106">`IsNormalRate`方法會指出剪輯是否會以正常播放速率播放，也就是原始檔案的播放速度。</span><span class="sxs-lookup"><span data-stu-id="da8ed-106">The `IsNormalRate` method indicates whether the clip will play at the normal playback rate; that is, the playback rate of the original file.</span></span>

## <a name="syntax"></a><span data-ttu-id="da8ed-107">語法</span><span class="sxs-lookup"><span data-stu-id="da8ed-107">Syntax</span></span>


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="da8ed-108">參數</span><span class="sxs-lookup"><span data-stu-id="da8ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da8ed-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="da8ed-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="da8ed-110">接收布林值，指出剪輯將如何轉譯。</span><span class="sxs-lookup"><span data-stu-id="da8ed-110">Receives a Boolean value indicating how the clip will render.</span></span> <span data-ttu-id="da8ed-111">如果該值為 **TRUE**，則會以一般速率播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="da8ed-111">If the value is **TRUE**, the clip will play at the normal rate.</span></span> <span data-ttu-id="da8ed-112">否則，它的播放速度會比平常更快或更慢。</span><span class="sxs-lookup"><span data-stu-id="da8ed-112">Otherwise, it will play faster or slower than normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da8ed-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="da8ed-113">Return value</span></span>

<span data-ttu-id="da8ed-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="da8ed-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="da8ed-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da8ed-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da8ed-116">備註</span><span class="sxs-lookup"><span data-stu-id="da8ed-116">Remarks</span></span>

<span data-ttu-id="da8ed-117">剪輯的播放速率取決於其媒體的開始和停止時間，相對於其時間軸時間：</span><span class="sxs-lookup"><span data-stu-id="da8ed-117">A clip's playback rate is determined by its media start and stop times, relative to its timeline times:</span></span>


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



<span data-ttu-id="da8ed-118">如果此比率等於1，則剪輯會以撰寫的速度播放。</span><span class="sxs-lookup"><span data-stu-id="da8ed-118">If this ratio is equal to 1, the clip plays at the authored speed.</span></span> <span data-ttu-id="da8ed-119">否則，它的播放速度會更快或更慢。</span><span class="sxs-lookup"><span data-stu-id="da8ed-119">Otherwise, it plays faster or slower.</span></span> <span data-ttu-id="da8ed-120">如需詳細資訊，請參閱 [DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="da8ed-120">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="da8ed-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="da8ed-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="da8ed-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="da8ed-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="da8ed-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="da8ed-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="da8ed-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="da8ed-124">Requirements</span></span>



| <span data-ttu-id="da8ed-125">需求</span><span class="sxs-lookup"><span data-stu-id="da8ed-125">Requirement</span></span> | <span data-ttu-id="da8ed-126">值</span><span class="sxs-lookup"><span data-stu-id="da8ed-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da8ed-127">標頭</span><span class="sxs-lookup"><span data-stu-id="da8ed-127">Header</span></span><br/>  | <dl> <span data-ttu-id="da8ed-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="da8ed-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="da8ed-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="da8ed-129">Library</span></span><br/> | <dl> <span data-ttu-id="da8ed-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="da8ed-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da8ed-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da8ed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8ed-132">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="da8ed-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="da8ed-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="da8ed-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




