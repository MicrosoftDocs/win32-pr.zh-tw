---
description: Get \_ Height 方法會抓取目標矩形的高度。
ms.assetid: af555a7b-de0a-4c44-9623-f1ec8b44969a
title: 'IDxtCompositor：： get_Height 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_Height
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1901264572f0deb3453738789f3d2cf2413fb401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978791"
---
# <a name="idxtcompositorget_height-method"></a><span data-ttu-id="5054f-103">IDxtCompositor：： get \_ Height 方法</span><span class="sxs-lookup"><span data-stu-id="5054f-103">IDxtCompositor::get\_Height method</span></span>

> [!Note]  
> <span data-ttu-id="5054f-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5054f-104">\[Deprecated.</span></span> <span data-ttu-id="5054f-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5054f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5054f-106">方法會抓取 `get_Height` 目標矩形的高度。</span><span class="sxs-lookup"><span data-stu-id="5054f-106">The `get_Height` method retrieves the height of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="5054f-107">語法</span><span class="sxs-lookup"><span data-stu-id="5054f-107">Syntax</span></span>


```C++
HRESULT get_Height(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5054f-108">參數</span><span class="sxs-lookup"><span data-stu-id="5054f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5054f-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="5054f-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5054f-110">接收目標矩形的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5054f-110">Receives the height of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5054f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5054f-111">Return value</span></span>

<span data-ttu-id="5054f-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5054f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5054f-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5054f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5054f-114">備註</span><span class="sxs-lookup"><span data-stu-id="5054f-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5054f-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5054f-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5054f-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5054f-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5054f-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5054f-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5054f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5054f-118">Requirements</span></span>



| <span data-ttu-id="5054f-119">需求</span><span class="sxs-lookup"><span data-stu-id="5054f-119">Requirement</span></span> | <span data-ttu-id="5054f-120">值</span><span class="sxs-lookup"><span data-stu-id="5054f-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5054f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5054f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5054f-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5054f-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5054f-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="5054f-123">Library</span></span><br/> | <dl> <span data-ttu-id="5054f-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5054f-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5054f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5054f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5054f-126">**IDxtCompositor 介面**</span><span class="sxs-lookup"><span data-stu-id="5054f-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




