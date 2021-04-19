---
description: Get OffsetY 方法會抓取抹除 \_ 來源的垂直位移。
ms.assetid: 0d8b8df2-b916-4143-b1f1-7912ef3fa025
title: 'IDxtJpeg：： get_OffsetY 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76c0d60ac5150fcec1bde63ccb4e03d820c38ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994650"
---
# <a name="idxtjpegget_offsety-method"></a><span data-ttu-id="dc4ed-103">IDxtJpeg：： get \_ OffsetY 方法</span><span class="sxs-lookup"><span data-stu-id="dc4ed-103">IDxtJpeg::get\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="dc4ed-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="dc4ed-104">\[Deprecated.</span></span> <span data-ttu-id="dc4ed-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="dc4ed-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dc4ed-106">方法會抓取抹除 `get_OffsetY` 來源的垂直位移。</span><span class="sxs-lookup"><span data-stu-id="dc4ed-106">The `get_OffsetY` method retrieves the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4ed-107">語法</span><span class="sxs-lookup"><span data-stu-id="dc4ed-107">Syntax</span></span>


```C++
HRESULT get_OffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="dc4ed-108">參數</span><span class="sxs-lookup"><span data-stu-id="dc4ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc4ed-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="dc4ed-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dc4ed-110">接收抹除來源的垂直位移（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="dc4ed-110">Receives the vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="dc4ed-111">抹除的中心會以此數量來位移。</span><span class="sxs-lookup"><span data-stu-id="dc4ed-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc4ed-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc4ed-112">Return value</span></span>

<span data-ttu-id="dc4ed-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="dc4ed-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dc4ed-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc4ed-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc4ed-115">備註</span><span class="sxs-lookup"><span data-stu-id="dc4ed-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dc4ed-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="dc4ed-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dc4ed-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="dc4ed-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dc4ed-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="dc4ed-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dc4ed-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc4ed-119">Requirements</span></span>



| <span data-ttu-id="dc4ed-120">需求</span><span class="sxs-lookup"><span data-stu-id="dc4ed-120">Requirement</span></span> | <span data-ttu-id="dc4ed-121">值</span><span class="sxs-lookup"><span data-stu-id="dc4ed-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4ed-122">標頭</span><span class="sxs-lookup"><span data-stu-id="dc4ed-122">Header</span></span><br/>  | <dl> <span data-ttu-id="dc4ed-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc4ed-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dc4ed-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="dc4ed-124">Library</span></span><br/> | <dl> <span data-ttu-id="dc4ed-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc4ed-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc4ed-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc4ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4ed-127">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="dc4ed-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




