---
description: IsSmartRecompressFormatSet 方法會判斷是否已針對群組設定智慧 recompression 格式。
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: 'IAMTimelineGroup：： IsSmartRecompressFormatSet 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 078649fd42cd44596ff27558b29d14b6f8cbeddc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977541"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a><span data-ttu-id="e6e86-103">IAMTimelineGroup：： IsSmartRecompressFormatSet 方法</span><span class="sxs-lookup"><span data-stu-id="e6e86-103">IAMTimelineGroup::IsSmartRecompressFormatSet method</span></span>

> [!Note]  
> <span data-ttu-id="e6e86-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="e6e86-104">\[Deprecated.</span></span> <span data-ttu-id="e6e86-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="e6e86-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e6e86-106">`IsSmartRecompressFormatSet`方法會判斷是否已針對群組設定智慧 recompression 格式。</span><span class="sxs-lookup"><span data-stu-id="e6e86-106">The `IsSmartRecompressFormatSet` method determines whether a smart recompression format was set for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e86-107">語法</span><span class="sxs-lookup"><span data-stu-id="e6e86-107">Syntax</span></span>


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e6e86-108">參數</span><span class="sxs-lookup"><span data-stu-id="e6e86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e86-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="e6e86-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e86-110">接收布林值，指出是否已設定壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="e6e86-110">Receives a Boolean value indicating whether a compression format was set.</span></span> <span data-ttu-id="e6e86-111">若 **為 TRUE**，則已設定壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="e6e86-111">If **TRUE**, a compression format was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e86-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6e86-112">Return value</span></span>

<span data-ttu-id="e6e86-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e6e86-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6e86-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e6e86-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e86-115">備註</span><span class="sxs-lookup"><span data-stu-id="e6e86-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6e86-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="e6e86-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6e86-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e6e86-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e6e86-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="e6e86-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6e86-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6e86-119">Requirements</span></span>



| <span data-ttu-id="e6e86-120">需求</span><span class="sxs-lookup"><span data-stu-id="e6e86-120">Requirement</span></span> | <span data-ttu-id="e6e86-121">值</span><span class="sxs-lookup"><span data-stu-id="e6e86-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e86-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e6e86-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e6e86-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e86-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e6e86-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="e6e86-124">Library</span></span><br/> | <dl> <span data-ttu-id="e6e86-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6e86-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e86-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6e86-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e86-127">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="e6e86-127">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="e6e86-128">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="e6e86-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




