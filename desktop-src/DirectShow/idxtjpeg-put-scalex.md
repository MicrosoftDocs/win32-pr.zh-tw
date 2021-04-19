---
description: Put \_ ScaleX 方法會指定以水準方式延展抹除的量。
ms.assetid: d57af5dc-41e0-45a7-8f11-55ef3bc62549
title: 'IDxtJpeg：:p ut_ScaleX 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fff0583ce3163ebf5626cfdbb82edf5c927bdc9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989549"
---
# <a name="idxtjpegput_scalex-method"></a><span data-ttu-id="59f1c-103">IDxtJpeg：:p 的 ui \_ ScaleX 方法</span><span class="sxs-lookup"><span data-stu-id="59f1c-103">IDxtJpeg::put\_ScaleX method</span></span>

> [!Note]  
> <span data-ttu-id="59f1c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="59f1c-104">\[Deprecated.</span></span> <span data-ttu-id="59f1c-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="59f1c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="59f1c-106">`put_ScaleX`方法會指定以水準方式延展抹除的量。</span><span class="sxs-lookup"><span data-stu-id="59f1c-106">The `put_ScaleX` method specifies the amount by which the wipe is stretched horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f1c-107">語法</span><span class="sxs-lookup"><span data-stu-id="59f1c-107">Syntax</span></span>


```C++
HRESULT put_ScaleX(
  [in] double newVal
);
```



## <a name="parameters"></a><span data-ttu-id="59f1c-108">參數</span><span class="sxs-lookup"><span data-stu-id="59f1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59f1c-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="59f1c-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59f1c-110">抹除的水準延展量（以原始抹除定義的百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="59f1c-110">The amount by which the wipe is stretched horizontally, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="59f1c-111">例如，值1.0 表示無延展，2.0 表示200% 延展。</span><span class="sxs-lookup"><span data-stu-id="59f1c-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59f1c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="59f1c-112">Return value</span></span>

<span data-ttu-id="59f1c-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="59f1c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59f1c-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="59f1c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="59f1c-115">備註</span><span class="sxs-lookup"><span data-stu-id="59f1c-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="59f1c-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="59f1c-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="59f1c-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="59f1c-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="59f1c-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="59f1c-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59f1c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="59f1c-119">Requirements</span></span>



| <span data-ttu-id="59f1c-120">需求</span><span class="sxs-lookup"><span data-stu-id="59f1c-120">Requirement</span></span> | <span data-ttu-id="59f1c-121">值</span><span class="sxs-lookup"><span data-stu-id="59f1c-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59f1c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="59f1c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="59f1c-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="59f1c-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="59f1c-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="59f1c-124">Library</span></span><br/> | <dl> <span data-ttu-id="59f1c-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="59f1c-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59f1c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59f1c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f1c-127">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="59f1c-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




