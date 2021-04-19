---
description: SetUserID 方法會設定物件的應用程式定義識別碼。
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: 'IAMTimelineObj：： SetUserID 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 31a0c59c6c93535be1200b2cd7678d4c355b5bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991136"
---
# <a name="iamtimelineobjsetuserid-method"></a><span data-ttu-id="e3858-103">IAMTimelineObj：： SetUserID 方法</span><span class="sxs-lookup"><span data-stu-id="e3858-103">IAMTimelineObj::SetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="e3858-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="e3858-104">\[Deprecated.</span></span> <span data-ttu-id="e3858-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="e3858-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e3858-106">`SetUserID`方法會設定物件的應用程式定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3858-106">The `SetUserID` method sets an application-defined identifier for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3858-107">語法</span><span class="sxs-lookup"><span data-stu-id="e3858-107">Syntax</span></span>


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e3858-108">參數</span><span class="sxs-lookup"><span data-stu-id="e3858-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3858-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="e3858-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e3858-110">指定識別碼的值。</span><span class="sxs-lookup"><span data-stu-id="e3858-110">Value that specifies the identifier.</span></span> <span data-ttu-id="e3858-111">此識別碼只能由應用程式使用，而且可以是任何值。</span><span class="sxs-lookup"><span data-stu-id="e3858-111">This identifier is used only by the application and can be any value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3858-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3858-112">Return value</span></span>

<span data-ttu-id="e3858-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e3858-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3858-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e3858-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3858-115">備註</span><span class="sxs-lookup"><span data-stu-id="e3858-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e3858-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="e3858-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e3858-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e3858-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e3858-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="e3858-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3858-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3858-119">Requirements</span></span>



| <span data-ttu-id="e3858-120">需求</span><span class="sxs-lookup"><span data-stu-id="e3858-120">Requirement</span></span> | <span data-ttu-id="e3858-121">值</span><span class="sxs-lookup"><span data-stu-id="e3858-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3858-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e3858-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e3858-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3858-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e3858-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3858-124">Library</span></span><br/> | <dl> <span data-ttu-id="e3858-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3858-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3858-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3858-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3858-127">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="e3858-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e3858-128">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="e3858-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




