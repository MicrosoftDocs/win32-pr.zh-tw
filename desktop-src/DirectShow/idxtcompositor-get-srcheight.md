---
description: Get \_ SrcHeight 方法會抓取來源矩形的高度。
ms.assetid: 3c6647b3-dfca-490d-a3d5-9aa6988e387d
title: 'IDxtCompositor：： get_SrcHeight 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcHeight
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b3ad874d7c02a9c9300af7fe3dbc69f6d351bba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976170"
---
# <a name="idxtcompositorget_srcheight-method"></a><span data-ttu-id="c541d-103">IDxtCompositor：： get \_ SrcHeight 方法</span><span class="sxs-lookup"><span data-stu-id="c541d-103">IDxtCompositor::get\_SrcHeight method</span></span>

> [!Note]  
> <span data-ttu-id="c541d-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="c541d-104">\[Deprecated.</span></span> <span data-ttu-id="c541d-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="c541d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c541d-106">方法會抓取 `get_SrcHeight` 來源矩形的高度。</span><span class="sxs-lookup"><span data-stu-id="c541d-106">The `get_SrcHeight` method retrieves the height of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c541d-107">語法</span><span class="sxs-lookup"><span data-stu-id="c541d-107">Syntax</span></span>


```C++
HRESULT get_SrcHeight(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c541d-108">參數</span><span class="sxs-lookup"><span data-stu-id="c541d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c541d-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="c541d-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c541d-110">接收來源矩形的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c541d-110">Receives the height of the source rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c541d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c541d-111">Return value</span></span>

<span data-ttu-id="c541d-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c541d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c541d-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c541d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c541d-114">備註</span><span class="sxs-lookup"><span data-stu-id="c541d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c541d-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="c541d-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c541d-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="c541d-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c541d-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="c541d-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c541d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c541d-118">Requirements</span></span>



| <span data-ttu-id="c541d-119">需求</span><span class="sxs-lookup"><span data-stu-id="c541d-119">Requirement</span></span> | <span data-ttu-id="c541d-120">值</span><span class="sxs-lookup"><span data-stu-id="c541d-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c541d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c541d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c541d-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c541d-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c541d-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="c541d-123">Library</span></span><br/> | <dl> <span data-ttu-id="c541d-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c541d-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c541d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c541d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c541d-126">**IDxtCompositor 介面**</span><span class="sxs-lookup"><span data-stu-id="c541d-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




