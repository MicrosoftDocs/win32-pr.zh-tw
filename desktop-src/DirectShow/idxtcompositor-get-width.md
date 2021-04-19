---
description: 取得 \_ 寬度方法會抓取目標矩形的寬度。
ms.assetid: 023c976e-279e-489c-ada5-ae33144c6358
title: 'IDxtCompositor：： get_Width 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_Width
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8f7b18e4cc02b28284f8ce680a7de04eaf8c9b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995385"
---
# <a name="idxtcompositorget_width-method"></a><span data-ttu-id="6a427-103">IDxtCompositor：： get \_ Width 方法</span><span class="sxs-lookup"><span data-stu-id="6a427-103">IDxtCompositor::get\_Width method</span></span>

> [!Note]  
> <span data-ttu-id="6a427-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="6a427-104">\[Deprecated.</span></span> <span data-ttu-id="6a427-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="6a427-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6a427-106">方法會抓取 `get_Width` 目標矩形的寬度。</span><span class="sxs-lookup"><span data-stu-id="6a427-106">The `get_Width` method retrieves the width of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a427-107">語法</span><span class="sxs-lookup"><span data-stu-id="6a427-107">Syntax</span></span>


```C++
HRESULT get_Width(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6a427-108">參數</span><span class="sxs-lookup"><span data-stu-id="6a427-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a427-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="6a427-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6a427-110">接收目標矩形的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6a427-110">Receives the width of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a427-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a427-111">Return value</span></span>

<span data-ttu-id="6a427-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6a427-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a427-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6a427-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a427-114">備註</span><span class="sxs-lookup"><span data-stu-id="6a427-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a427-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="6a427-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6a427-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6a427-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6a427-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="6a427-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a427-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a427-118">Requirements</span></span>



| <span data-ttu-id="6a427-119">需求</span><span class="sxs-lookup"><span data-stu-id="6a427-119">Requirement</span></span> | <span data-ttu-id="6a427-120">值</span><span class="sxs-lookup"><span data-stu-id="6a427-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a427-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6a427-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6a427-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a427-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6a427-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a427-123">Library</span></span><br/> | <dl> <span data-ttu-id="6a427-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a427-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a427-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a427-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a427-126">**IDxtCompositor 介面**</span><span class="sxs-lookup"><span data-stu-id="6a427-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




