---
description: TransitionsEnabled 方法會判斷是否已啟用轉換。
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'IAMTimeline：： TransitionsEnabled 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990289"
---
# <a name="iamtimelinetransitionsenabled-method"></a><span data-ttu-id="85d21-103">IAMTimeline：： TransitionsEnabled 方法</span><span class="sxs-lookup"><span data-stu-id="85d21-103">IAMTimeline::TransitionsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="85d21-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="85d21-104">\[Deprecated.</span></span> <span data-ttu-id="85d21-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="85d21-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="85d21-106">**TransitionsEnabled** 方法會判斷是否已啟用轉換。</span><span class="sxs-lookup"><span data-stu-id="85d21-106">The **TransitionsEnabled** method determines whether transitions are enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d21-107">語法</span><span class="sxs-lookup"><span data-stu-id="85d21-107">Syntax</span></span>


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="85d21-108">參數</span><span class="sxs-lookup"><span data-stu-id="85d21-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d21-109">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="85d21-109">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="85d21-110">接收布林值。</span><span class="sxs-lookup"><span data-stu-id="85d21-110">Receives a Boolean value.</span></span> <span data-ttu-id="85d21-111">若 **為 TRUE**，則會啟用轉換。</span><span class="sxs-lookup"><span data-stu-id="85d21-111">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="85d21-112">否則，就會停用轉換。</span><span class="sxs-lookup"><span data-stu-id="85d21-112">Otherwise, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d21-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="85d21-113">Return value</span></span>

<span data-ttu-id="85d21-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="85d21-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85d21-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="85d21-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d21-116">備註</span><span class="sxs-lookup"><span data-stu-id="85d21-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="85d21-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="85d21-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="85d21-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="85d21-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="85d21-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="85d21-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85d21-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="85d21-120">Requirements</span></span>



| <span data-ttu-id="85d21-121">需求</span><span class="sxs-lookup"><span data-stu-id="85d21-121">Requirement</span></span> | <span data-ttu-id="85d21-122">值</span><span class="sxs-lookup"><span data-stu-id="85d21-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85d21-123">標頭</span><span class="sxs-lookup"><span data-stu-id="85d21-123">Header</span></span><br/>  | <dl> <span data-ttu-id="85d21-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="85d21-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="85d21-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="85d21-125">Library</span></span><br/> | <dl> <span data-ttu-id="85d21-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="85d21-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85d21-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85d21-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d21-128">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="85d21-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="85d21-129">**IAMTimeline::EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="85d21-129">**IAMTimeline::EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)
</dt> <dt>

[<span data-ttu-id="85d21-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="85d21-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




