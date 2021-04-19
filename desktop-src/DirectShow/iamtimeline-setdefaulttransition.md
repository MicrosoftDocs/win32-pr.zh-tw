---
description: SetDefaultTransition 方法會設定預設轉換。 如果轉譯引擎無法轉譯轉換，則會替代預設轉換。
ms.assetid: 5ee84a12-402f-4f1c-9f08-206431c7ecdb
title: 'IAMTimeline：： SetDefaultTransition 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeea5563ca9a2548507d3b4333d857d7cc156dd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995964"
---
# <a name="iamtimelinesetdefaulttransition-method"></a><span data-ttu-id="997c2-104">IAMTimeline：： SetDefaultTransition 方法</span><span class="sxs-lookup"><span data-stu-id="997c2-104">IAMTimeline::SetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="997c2-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="997c2-105">\[Deprecated.</span></span> <span data-ttu-id="997c2-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="997c2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="997c2-107">`SetDefaultTransition`方法會設定預設轉換。</span><span class="sxs-lookup"><span data-stu-id="997c2-107">The `SetDefaultTransition` method sets the default transition.</span></span> <span data-ttu-id="997c2-108">如果轉譯引擎無法轉譯轉換，則會替代預設轉換。</span><span class="sxs-lookup"><span data-stu-id="997c2-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="997c2-109">語法</span><span class="sxs-lookup"><span data-stu-id="997c2-109">Syntax</span></span>


```C++
HRESULT SetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="997c2-110">參數</span><span class="sxs-lookup"><span data-stu-id="997c2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="997c2-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="997c2-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="997c2-112">變數的指標，其中包含預設轉換的 GUID。</span><span class="sxs-lookup"><span data-stu-id="997c2-112">Pointer to a variable that contains the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="997c2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="997c2-113">Return value</span></span>

<span data-ttu-id="997c2-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="997c2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="997c2-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="997c2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="997c2-116">備註</span><span class="sxs-lookup"><span data-stu-id="997c2-116">Remarks</span></span>

<span data-ttu-id="997c2-117">如果您未設定預設轉換，或您指定為預設值的轉換造成錯誤，DES 會使用自己的預設轉換。</span><span class="sxs-lookup"><span data-stu-id="997c2-117">If you do not set a default transition, or if the transition that you specify as a default causes an error, DES uses its own default transition.</span></span>

> [!Note]  
> <span data-ttu-id="997c2-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="997c2-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="997c2-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="997c2-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="997c2-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="997c2-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="997c2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="997c2-121">Requirements</span></span>



| <span data-ttu-id="997c2-122">需求</span><span class="sxs-lookup"><span data-stu-id="997c2-122">Requirement</span></span> | <span data-ttu-id="997c2-123">值</span><span class="sxs-lookup"><span data-stu-id="997c2-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="997c2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="997c2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="997c2-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="997c2-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="997c2-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="997c2-126">Library</span></span><br/> | <dl> <span data-ttu-id="997c2-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="997c2-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="997c2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="997c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="997c2-129">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="997c2-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="997c2-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="997c2-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




