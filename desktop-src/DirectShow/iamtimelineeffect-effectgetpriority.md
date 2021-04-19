---
description: EffectGetPriority 方法會抓取效果的優先權層級。 針對指定的物件，轉譯引擎會依優先權順序套用效果，從優先權層級零開始。
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: 'IAMTimelineEffect：： EffectGetPriority 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 26ea9795e3ffe36a75c354e51ff2f7e64fae40ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996518"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a><span data-ttu-id="a85d1-104">IAMTimelineEffect：： EffectGetPriority 方法</span><span class="sxs-lookup"><span data-stu-id="a85d1-104">IAMTimelineEffect::EffectGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="a85d1-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="a85d1-105">\[Deprecated.</span></span> <span data-ttu-id="a85d1-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="a85d1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a85d1-107">方法會抓取 `EffectGetPriority` 效果的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="a85d1-107">The `EffectGetPriority` method retrieves the effect's priority level.</span></span> <span data-ttu-id="a85d1-108">針對指定的物件，轉譯引擎會依優先權順序套用效果，從優先權層級零開始。</span><span class="sxs-lookup"><span data-stu-id="a85d1-108">For a given object, the render engine applies effects in order of priority, starting with priority level zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="a85d1-109">語法</span><span class="sxs-lookup"><span data-stu-id="a85d1-109">Syntax</span></span>


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a85d1-110">參數</span><span class="sxs-lookup"><span data-stu-id="a85d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a85d1-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="a85d1-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="a85d1-112">接收優先權層級。</span><span class="sxs-lookup"><span data-stu-id="a85d1-112">Receives the priority level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a85d1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a85d1-113">Return value</span></span>

<span data-ttu-id="a85d1-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a85d1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a85d1-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a85d1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a85d1-116">備註</span><span class="sxs-lookup"><span data-stu-id="a85d1-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a85d1-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="a85d1-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a85d1-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a85d1-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a85d1-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="a85d1-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a85d1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a85d1-120">Requirements</span></span>



| <span data-ttu-id="a85d1-121">需求</span><span class="sxs-lookup"><span data-stu-id="a85d1-121">Requirement</span></span> | <span data-ttu-id="a85d1-122">值</span><span class="sxs-lookup"><span data-stu-id="a85d1-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a85d1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a85d1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a85d1-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a85d1-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a85d1-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="a85d1-125">Library</span></span><br/> | <dl> <span data-ttu-id="a85d1-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a85d1-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a85d1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a85d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a85d1-128">**IAMTimelineEffect 介面**</span><span class="sxs-lookup"><span data-stu-id="a85d1-128">**IAMTimelineEffect Interface**</span></span>](iamtimelineeffect.md)
</dt> <dt>

[<span data-ttu-id="a85d1-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="a85d1-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




