---
description: Put \_ 邊框型方法會指定抹除模式邊緣周圍的框線色彩。
ms.assetid: d6a49956-8fc9-4ba2-8485-a49175da3cf7
title: 'IDxtJpeg：:p ut_BorderColor 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: faacc76eaa120467aa6cfb6c318aac0d9baec334
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994622"
---
# <a name="idxtjpegput_bordercolor-method"></a><span data-ttu-id="67e0f-103">IDxtJpeg：:p 的 ui \_ 邊框出方法</span><span class="sxs-lookup"><span data-stu-id="67e0f-103">IDxtJpeg::put\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="67e0f-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="67e0f-104">\[Deprecated.</span></span> <span data-ttu-id="67e0f-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="67e0f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="67e0f-106">`put_BorderColor`方法會指定抹除模式邊緣周圍的框線色彩。</span><span class="sxs-lookup"><span data-stu-id="67e0f-106">The `put_BorderColor` method specifies the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="67e0f-107">語法</span><span class="sxs-lookup"><span data-stu-id="67e0f-107">Syntax</span></span>


```C++
HRESULT put_BorderColor(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="67e0f-108">參數</span><span class="sxs-lookup"><span data-stu-id="67e0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67e0f-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67e0f-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67e0f-110">使用0xRRGGBB 格式將色彩指定為十六進位數位，其中 RR 是紅色值、GG 為綠色值，而 BB 為藍色值。</span><span class="sxs-lookup"><span data-stu-id="67e0f-110">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67e0f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="67e0f-111">Return value</span></span>

<span data-ttu-id="67e0f-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="67e0f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67e0f-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="67e0f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67e0f-114">備註</span><span class="sxs-lookup"><span data-stu-id="67e0f-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="67e0f-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="67e0f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="67e0f-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="67e0f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="67e0f-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="67e0f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67e0f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="67e0f-118">Requirements</span></span>



| <span data-ttu-id="67e0f-119">需求</span><span class="sxs-lookup"><span data-stu-id="67e0f-119">Requirement</span></span> | <span data-ttu-id="67e0f-120">值</span><span class="sxs-lookup"><span data-stu-id="67e0f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67e0f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="67e0f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="67e0f-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="67e0f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="67e0f-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="67e0f-123">Library</span></span><br/> | <dl> <span data-ttu-id="67e0f-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="67e0f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67e0f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67e0f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e0f-126">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="67e0f-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




