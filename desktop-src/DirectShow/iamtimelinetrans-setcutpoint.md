---
description: SetCutPoint 方法會設定當轉換轉譯為剪下時，轉換從某個來源剪下的時間。
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'IAMTimelineTrans：： SetCutPoint 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998395"
---
# <a name="iamtimelinetranssetcutpoint-method"></a><span data-ttu-id="b1447-103">IAMTimelineTrans：： SetCutPoint 方法</span><span class="sxs-lookup"><span data-stu-id="b1447-103">IAMTimelineTrans::SetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="b1447-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b1447-104">\[Deprecated.</span></span> <span data-ttu-id="b1447-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b1447-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1447-106">`SetCutPoint`如果轉換是轉譯為剪下，則方法會設定轉換從某個來源減少到下一個來源的時間。</span><span class="sxs-lookup"><span data-stu-id="b1447-106">The `SetCutPoint` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1447-107">語法</span><span class="sxs-lookup"><span data-stu-id="b1447-107">Syntax</span></span>


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="b1447-108">參數</span><span class="sxs-lookup"><span data-stu-id="b1447-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1447-109">*TLTime*</span><span class="sxs-lookup"><span data-stu-id="b1447-109">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="b1447-110">相對於開始轉換起點的剪下（以 100-毫微秒單位）。</span><span class="sxs-lookup"><span data-stu-id="b1447-110">Cut point relative to the start of the transition, in 100-nanosecond units.</span></span> <span data-ttu-id="b1447-111">如果值落在轉換範圍之外，則會截斷為最接近的有效時間。</span><span class="sxs-lookup"><span data-stu-id="b1447-111">If the value falls outside the bounds of the transition, it is truncated to the nearest valid time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1447-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1447-112">Return value</span></span>

<span data-ttu-id="b1447-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b1447-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1447-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b1447-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1447-115">備註</span><span class="sxs-lookup"><span data-stu-id="b1447-115">Remarks</span></span>

<span data-ttu-id="b1447-116">根據預設，剪點是轉換的中間。</span><span class="sxs-lookup"><span data-stu-id="b1447-116">By default, the cut-point is the middle of the transition.</span></span> <span data-ttu-id="b1447-117">例如，在橫跨1秒的轉換中，預設的剪下點在轉換中是0.5 秒。</span><span class="sxs-lookup"><span data-stu-id="b1447-117">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

> [!Note]  
> <span data-ttu-id="b1447-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b1447-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b1447-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b1447-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b1447-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b1447-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1447-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1447-121">Requirements</span></span>



| <span data-ttu-id="b1447-122">需求</span><span class="sxs-lookup"><span data-stu-id="b1447-122">Requirement</span></span> | <span data-ttu-id="b1447-123">值</span><span class="sxs-lookup"><span data-stu-id="b1447-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1447-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b1447-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b1447-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1447-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b1447-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1447-126">Library</span></span><br/> | <dl> <span data-ttu-id="b1447-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1447-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1447-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1447-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1447-129">**IAMTimelineTrans 介面**</span><span class="sxs-lookup"><span data-stu-id="b1447-129">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="b1447-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="b1447-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




