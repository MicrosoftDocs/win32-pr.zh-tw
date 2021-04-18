---
description: GetMediaTimes 方法會抓取媒體的開始和停止時間。
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: 'IAMTimelineSrc：： GetMediaTimes 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa6e9cbb69da504a929e23722068583489063b9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996282"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a><span data-ttu-id="f5c20-103">IAMTimelineSrc：： GetMediaTimes 方法</span><span class="sxs-lookup"><span data-stu-id="f5c20-103">IAMTimelineSrc::GetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="f5c20-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="f5c20-104">\[Deprecated.</span></span> <span data-ttu-id="f5c20-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="f5c20-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5c20-106">方法會抓取 `GetMediaTimes` 媒體的開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="f5c20-106">The `GetMediaTimes` method retrieves the media start and stop times.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c20-107">語法</span><span class="sxs-lookup"><span data-stu-id="f5c20-107">Syntax</span></span>


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="f5c20-108">參數</span><span class="sxs-lookup"><span data-stu-id="f5c20-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c20-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="f5c20-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c20-110">接收媒體開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="f5c20-110">Receives the media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="f5c20-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="f5c20-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="f5c20-112">接收媒體停止時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="f5c20-112">Receives the media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c20-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5c20-113">Return value</span></span>

<span data-ttu-id="f5c20-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f5c20-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5c20-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f5c20-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c20-116">備註</span><span class="sxs-lookup"><span data-stu-id="f5c20-116">Remarks</span></span>

<span data-ttu-id="f5c20-117">媒體時間相對於原始媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="f5c20-117">The media times are relative to the original media file.</span></span> <span data-ttu-id="f5c20-118">如需詳細資訊，請參閱 [DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="f5c20-118">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="f5c20-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="f5c20-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5c20-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="f5c20-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f5c20-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="f5c20-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5c20-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5c20-122">Requirements</span></span>



| <span data-ttu-id="f5c20-123">需求</span><span class="sxs-lookup"><span data-stu-id="f5c20-123">Requirement</span></span> | <span data-ttu-id="f5c20-124">值</span><span class="sxs-lookup"><span data-stu-id="f5c20-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c20-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f5c20-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f5c20-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c20-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f5c20-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="f5c20-127">Library</span></span><br/> | <dl> <span data-ttu-id="f5c20-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5c20-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c20-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5c20-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c20-130">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="f5c20-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="f5c20-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="f5c20-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




