---
description: SetOutputBuffering 方法會指定預覽期間預先轉譯的畫面格數目。
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'IAMTimelineGroup：： SetOutputBuffering 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999468"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a><span data-ttu-id="98ad4-103">IAMTimelineGroup：： SetOutputBuffering 方法</span><span class="sxs-lookup"><span data-stu-id="98ad4-103">IAMTimelineGroup::SetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="98ad4-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="98ad4-104">\[Deprecated.</span></span> <span data-ttu-id="98ad4-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="98ad4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="98ad4-106">`SetOutputBuffering`方法會指定預覽期間預先轉譯的畫面格數。</span><span class="sxs-lookup"><span data-stu-id="98ad4-106">The `SetOutputBuffering` method specifies the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="98ad4-107">語法</span><span class="sxs-lookup"><span data-stu-id="98ad4-107">Syntax</span></span>


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="98ad4-108">參數</span><span class="sxs-lookup"><span data-stu-id="98ad4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98ad4-109">*nBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98ad4-109">*nBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98ad4-110">預覽期間要緩衝的框架數目。</span><span class="sxs-lookup"><span data-stu-id="98ad4-110">Number of frames to buffer during preview.</span></span> <span data-ttu-id="98ad4-111">必須是2或以上。</span><span class="sxs-lookup"><span data-stu-id="98ad4-111">Must be two or greater.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98ad4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="98ad4-112">Return value</span></span>

<span data-ttu-id="98ad4-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="98ad4-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98ad4-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="98ad4-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98ad4-115">備註</span><span class="sxs-lookup"><span data-stu-id="98ad4-115">Remarks</span></span>

<span data-ttu-id="98ad4-116">較大的緩衝區需要更多記憶體，但會導致更流暢的預覽，尤其是在需要更多時間轉譯的效果或轉換期間。</span><span class="sxs-lookup"><span data-stu-id="98ad4-116">A larger buffer requires more memory but can result in smoother previewing, especially during effects or transitions that require more time to render.</span></span> <span data-ttu-id="98ad4-117">預設緩衝區為30個畫面格。</span><span class="sxs-lookup"><span data-stu-id="98ad4-117">The default buffer is 30 frames.</span></span>

> [!Note]  
> <span data-ttu-id="98ad4-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="98ad4-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="98ad4-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="98ad4-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="98ad4-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="98ad4-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98ad4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="98ad4-121">Requirements</span></span>



| <span data-ttu-id="98ad4-122">需求</span><span class="sxs-lookup"><span data-stu-id="98ad4-122">Requirement</span></span> | <span data-ttu-id="98ad4-123">值</span><span class="sxs-lookup"><span data-stu-id="98ad4-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98ad4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="98ad4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="98ad4-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="98ad4-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="98ad4-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="98ad4-126">Library</span></span><br/> | <dl> <span data-ttu-id="98ad4-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="98ad4-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98ad4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98ad4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ad4-129">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="98ad4-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="98ad4-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="98ad4-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




