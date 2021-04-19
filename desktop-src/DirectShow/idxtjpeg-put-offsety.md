---
description: Put \_ OffsetY 方法會指定抹除來源的垂直位移。
ms.assetid: 1dfd18cf-06ae-46eb-80d7-078efc243bb1
title: 'IDxtJpeg：:p ut_OffsetY 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f68a18d01acf519032bce31c28515bc7ac81c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990979"
---
# <a name="idxtjpegput_offsety-method"></a><span data-ttu-id="b9d49-103">IDxtJpeg：:p 的 \_ OffsetY 方法</span><span class="sxs-lookup"><span data-stu-id="b9d49-103">IDxtJpeg::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="b9d49-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b9d49-104">\[Deprecated.</span></span> <span data-ttu-id="b9d49-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b9d49-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b9d49-106">`put_OffsetY`方法會指定抹除來源的垂直位移。</span><span class="sxs-lookup"><span data-stu-id="b9d49-106">The `put_OffsetY` method specifies the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9d49-107">語法</span><span class="sxs-lookup"><span data-stu-id="b9d49-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b9d49-108">參數</span><span class="sxs-lookup"><span data-stu-id="b9d49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9d49-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9d49-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9d49-110">抹除來源的垂直位移（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b9d49-110">The vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="b9d49-111">抹除的中心會以此數量來位移。</span><span class="sxs-lookup"><span data-stu-id="b9d49-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9d49-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9d49-112">Return value</span></span>

<span data-ttu-id="b9d49-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b9d49-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9d49-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b9d49-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9d49-115">備註</span><span class="sxs-lookup"><span data-stu-id="b9d49-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b9d49-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b9d49-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b9d49-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b9d49-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b9d49-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b9d49-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b9d49-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9d49-119">Requirements</span></span>



| <span data-ttu-id="b9d49-120">需求</span><span class="sxs-lookup"><span data-stu-id="b9d49-120">Requirement</span></span> | <span data-ttu-id="b9d49-121">值</span><span class="sxs-lookup"><span data-stu-id="b9d49-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d49-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b9d49-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b9d49-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9d49-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b9d49-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="b9d49-124">Library</span></span><br/> | <dl> <span data-ttu-id="b9d49-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9d49-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9d49-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9d49-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d49-127">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="b9d49-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




