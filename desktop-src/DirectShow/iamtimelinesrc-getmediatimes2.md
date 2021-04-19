---
description: GetMediaTimes2 方法會抓取媒體的開始和停止時間。 這個方法相當於 IAMTimelineSrc：： GetMediaTimes，但會接受 REFTIME 的值。
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: 'IAMTimelineSrc：： GetMediaTimes2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 779876e542ab51914725b326a0e3b217b893f254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995368"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a><span data-ttu-id="3b1e7-104">IAMTimelineSrc：： GetMediaTimes2 方法</span><span class="sxs-lookup"><span data-stu-id="3b1e7-104">IAMTimelineSrc::GetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="3b1e7-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-105">\[Deprecated.</span></span> <span data-ttu-id="3b1e7-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3b1e7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3b1e7-107">方法會抓取 `GetMediaTimes2` 媒體的開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-107">The `GetMediaTimes2` method retrieves the media start and stop times.</span></span> <span data-ttu-id="3b1e7-108">這個方法相當於 [**IAMTimelineSrc：： GetMediaTimes**](iamtimelinesrc-getmediatimes.md)，但會接受 [**REFTIME**](reftime.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-108">This method is equivalent to [**IAMTimelineSrc::GetMediaTimes**](iamtimelinesrc-getmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b1e7-109">語法</span><span class="sxs-lookup"><span data-stu-id="3b1e7-109">Syntax</span></span>


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="3b1e7-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b1e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b1e7-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="3b1e7-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="3b1e7-112">接收媒體開始時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-112">Receives the media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="3b1e7-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="3b1e7-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="3b1e7-114">接收媒體停止時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-114">Receives the media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b1e7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b1e7-115">Return value</span></span>

<span data-ttu-id="3b1e7-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b1e7-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b1e7-118">備註</span><span class="sxs-lookup"><span data-stu-id="3b1e7-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3b1e7-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3b1e7-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3b1e7-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="3b1e7-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b1e7-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b1e7-122">Requirements</span></span>



| <span data-ttu-id="3b1e7-123">需求</span><span class="sxs-lookup"><span data-stu-id="3b1e7-123">Requirement</span></span> | <span data-ttu-id="3b1e7-124">值</span><span class="sxs-lookup"><span data-stu-id="3b1e7-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1e7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3b1e7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3b1e7-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b1e7-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3b1e7-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b1e7-127">Library</span></span><br/> | <dl> <span data-ttu-id="3b1e7-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b1e7-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b1e7-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b1e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b1e7-130">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="3b1e7-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="3b1e7-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="3b1e7-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




