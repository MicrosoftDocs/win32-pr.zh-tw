---
description: Get \_ OffsetY 方法會抓取目標矩形的垂直位移。
ms.assetid: 78bb3565-7a98-4a64-a2f2-6c34edb47733
title: 'IDxtCompositor：： get_OffsetY 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e3e8cb2e4552aceb53cf447125ddcc42659d575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987113"
---
# <a name="idxtcompositorget_offsety-method"></a><span data-ttu-id="6c8f7-103">IDxtCompositor：： get \_ OffsetY 方法</span><span class="sxs-lookup"><span data-stu-id="6c8f7-103">IDxtCompositor::get\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="6c8f7-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="6c8f7-104">\[Deprecated.</span></span> <span data-ttu-id="6c8f7-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="6c8f7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6c8f7-106">方法會抓取 `get_OffsetY` 目標矩形的垂直位移。</span><span class="sxs-lookup"><span data-stu-id="6c8f7-106">The `get_OffsetY` method retrieves the vertical offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8f7-107">語法</span><span class="sxs-lookup"><span data-stu-id="6c8f7-107">Syntax</span></span>


```C++
HRESULT get_OffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6c8f7-108">參數</span><span class="sxs-lookup"><span data-stu-id="6c8f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8f7-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="6c8f7-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8f7-110">接收目標矩形的垂直位移（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6c8f7-110">Receives the vertical offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8f7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c8f7-111">Return value</span></span>

<span data-ttu-id="6c8f7-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6c8f7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c8f7-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6c8f7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8f7-114">備註</span><span class="sxs-lookup"><span data-stu-id="6c8f7-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6c8f7-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="6c8f7-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6c8f7-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6c8f7-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6c8f7-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="6c8f7-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c8f7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c8f7-118">Requirements</span></span>



| <span data-ttu-id="6c8f7-119">需求</span><span class="sxs-lookup"><span data-stu-id="6c8f7-119">Requirement</span></span> | <span data-ttu-id="6c8f7-120">值</span><span class="sxs-lookup"><span data-stu-id="6c8f7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8f7-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6c8f7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6c8f7-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c8f7-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6c8f7-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c8f7-123">Library</span></span><br/> | <dl> <span data-ttu-id="6c8f7-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c8f7-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8f7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c8f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8f7-126">**IDxtCompositor 介面**</span><span class="sxs-lookup"><span data-stu-id="6c8f7-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




