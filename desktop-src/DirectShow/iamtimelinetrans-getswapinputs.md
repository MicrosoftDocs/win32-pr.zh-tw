---
description: GetSwapInputs 方法會抓取值，指出是否交換轉換輸入。
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'IAMTimelineTrans：： GetSwapInputs 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980229"
---
# <a name="iamtimelinetransgetswapinputs-method"></a><span data-ttu-id="8ecd9-103">IAMTimelineTrans：： GetSwapInputs 方法</span><span class="sxs-lookup"><span data-stu-id="8ecd9-103">IAMTimelineTrans::GetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="8ecd9-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-104">\[Deprecated.</span></span> <span data-ttu-id="8ecd9-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="8ecd9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8ecd9-106">`GetSwapInputs`方法會抓取值，指出是否交換轉換輸入。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-106">The `GetSwapInputs` method retrieves a value that indicates whether the transition inputs are swapped.</span></span>

<span data-ttu-id="8ecd9-107">根據預設，轉換會從所有較低優先順序層級的複合轉換成轉換所在的圖層。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="8ecd9-108">您可以反轉這項進展，讓轉換從它所在的圖層移回較低優先順序層級的組合。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ecd9-109">語法</span><span class="sxs-lookup"><span data-stu-id="8ecd9-109">Syntax</span></span>


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8ecd9-110">參數</span><span class="sxs-lookup"><span data-stu-id="8ecd9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ecd9-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="8ecd9-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="8ecd9-112">接收布林值。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-112">Receives a Boolean value.</span></span> <span data-ttu-id="8ecd9-113">如果值為 **FALSE**，則轉換會從所有較低優先順序層級到轉換圖層的複合。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-113">If the value is **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="8ecd9-114">如果值為 **TRUE**，則轉換會以相反的方向進行。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-114">If the value is **TRUE**, the transition goes in the opposite direction.</span></span> <span data-ttu-id="8ecd9-115">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-115">The default value is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ecd9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ecd9-116">Return value</span></span>

<span data-ttu-id="8ecd9-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ecd9-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ecd9-119">備註</span><span class="sxs-lookup"><span data-stu-id="8ecd9-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ecd9-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8ecd9-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8ecd9-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="8ecd9-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ecd9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ecd9-123">Requirements</span></span>



| <span data-ttu-id="8ecd9-124">需求</span><span class="sxs-lookup"><span data-stu-id="8ecd9-124">Requirement</span></span> | <span data-ttu-id="8ecd9-125">值</span><span class="sxs-lookup"><span data-stu-id="8ecd9-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ecd9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8ecd9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8ecd9-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ecd9-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8ecd9-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ecd9-128">Library</span></span><br/> | <dl> <span data-ttu-id="8ecd9-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ecd9-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ecd9-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ecd9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ecd9-131">**IAMTimelineTrans 介面**</span><span class="sxs-lookup"><span data-stu-id="8ecd9-131">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="8ecd9-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="8ecd9-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




