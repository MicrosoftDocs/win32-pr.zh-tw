---
description: 不支援這個方法。
ms.assetid: f263116b-e492-4468-9829-124a096c9d74
title: 'IAMTimelineTrack：： MoveEverythingBy 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.MoveEverythingBy
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4eded92548c047e6d5102e603a5ab0554bd1f4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990126"
---
# <a name="iamtimelinetrackmoveeverythingby-method"></a><span data-ttu-id="69121-103">IAMTimelineTrack：： MoveEverythingBy 方法</span><span class="sxs-lookup"><span data-stu-id="69121-103">IAMTimelineTrack::MoveEverythingBy method</span></span>

<span data-ttu-id="69121-104">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="69121-104">This method is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="69121-105">語法</span><span class="sxs-lookup"><span data-stu-id="69121-105">Syntax</span></span>


```C++
HRESULT MoveEverythingBy(
   REFERENCE_TIME Start,
   REFERENCE_TIME MoveBy
);
```



## <a name="parameters"></a><span data-ttu-id="69121-106">參數</span><span class="sxs-lookup"><span data-stu-id="69121-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69121-107">*開始*</span><span class="sxs-lookup"><span data-stu-id="69121-107">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="69121-108">保留的。</span><span class="sxs-lookup"><span data-stu-id="69121-108">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="69121-109">*MoveBy*</span><span class="sxs-lookup"><span data-stu-id="69121-109">*MoveBy*</span></span> 
</dt> <dd>

<span data-ttu-id="69121-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="69121-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69121-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="69121-111">Return value</span></span>

<span data-ttu-id="69121-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="69121-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69121-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="69121-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="69121-114">備註</span><span class="sxs-lookup"><span data-stu-id="69121-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="69121-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="69121-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="69121-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="69121-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="69121-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="69121-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69121-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="69121-118">Requirements</span></span>



| <span data-ttu-id="69121-119">需求</span><span class="sxs-lookup"><span data-stu-id="69121-119">Requirement</span></span> | <span data-ttu-id="69121-120">值</span><span class="sxs-lookup"><span data-stu-id="69121-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69121-121">標頭</span><span class="sxs-lookup"><span data-stu-id="69121-121">Header</span></span><br/>  | <dl> <span data-ttu-id="69121-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="69121-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="69121-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="69121-123">Library</span></span><br/> | <dl> <span data-ttu-id="69121-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="69121-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69121-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69121-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69121-126">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="69121-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> </dl>

 

 




