---
description: 取得邊框 \_ 距離方法會抓取抹除模式邊緣周圍的框線色彩。
ms.assetid: 9d36cc49-c174-4b93-a030-ca8d2890c624
title: 'IDxtJpeg：： get_BorderColor 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f37c37865caf76839733ada376ec637747977ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978458"
---
# <a name="idxtjpegget_bordercolor-method"></a><span data-ttu-id="a2424-103">IDxtJpeg：：取得 \_ 邊框方法</span><span class="sxs-lookup"><span data-stu-id="a2424-103">IDxtJpeg::get\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="a2424-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="a2424-104">\[Deprecated.</span></span> <span data-ttu-id="a2424-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="a2424-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a2424-106">方法會抓取抹除 `get_BorderColor` 模式邊緣周圍的框線色彩。</span><span class="sxs-lookup"><span data-stu-id="a2424-106">The `get_BorderColor` method retrieves the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2424-107">語法</span><span class="sxs-lookup"><span data-stu-id="a2424-107">Syntax</span></span>


```C++
HRESULT get_BorderColor(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a2424-108">參數</span><span class="sxs-lookup"><span data-stu-id="a2424-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2424-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="a2424-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a2424-110">接收色彩。</span><span class="sxs-lookup"><span data-stu-id="a2424-110">Receives the color.</span></span> <span data-ttu-id="a2424-111">傳回的值是0xRRGGBB 格式的十六進位數位，其中 RR 是紅色值，GG 是綠色值，而 BB 是藍色值。</span><span class="sxs-lookup"><span data-stu-id="a2424-111">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2424-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2424-112">Return value</span></span>

<span data-ttu-id="a2424-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a2424-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2424-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a2424-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2424-115">備註</span><span class="sxs-lookup"><span data-stu-id="a2424-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2424-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="a2424-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a2424-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a2424-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a2424-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="a2424-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2424-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2424-119">Requirements</span></span>



| <span data-ttu-id="a2424-120">需求</span><span class="sxs-lookup"><span data-stu-id="a2424-120">Requirement</span></span> | <span data-ttu-id="a2424-121">值</span><span class="sxs-lookup"><span data-stu-id="a2424-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2424-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a2424-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a2424-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2424-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a2424-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2424-124">Library</span></span><br/> | <dl> <span data-ttu-id="a2424-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2424-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2424-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2424-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2424-127">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="a2424-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




