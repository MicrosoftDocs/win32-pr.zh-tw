---
description: Get \_ OffsetX 方法會抓取目標矩形的水準位移。
ms.assetid: a9d8c81b-f978-4b47-9c7f-12cee7c2c40d
title: 'IDxtCompositor：： get_OffsetX 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8e2f21956e67b42158f4e646d33aa6e3e90d9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978474"
---
# <a name="idxtcompositorget_offsetx-method"></a><span data-ttu-id="fa7bf-103">IDxtCompositor：： get \_ OffsetX 方法</span><span class="sxs-lookup"><span data-stu-id="fa7bf-103">IDxtCompositor::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="fa7bf-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fa7bf-104">\[Deprecated.</span></span> <span data-ttu-id="fa7bf-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fa7bf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fa7bf-106">方法會抓取 `get_OffsetX` 目標矩形的水準位移。</span><span class="sxs-lookup"><span data-stu-id="fa7bf-106">The `get_OffsetX` method retrieves the horizontal offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa7bf-107">語法</span><span class="sxs-lookup"><span data-stu-id="fa7bf-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="fa7bf-108">參數</span><span class="sxs-lookup"><span data-stu-id="fa7bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa7bf-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="fa7bf-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fa7bf-110">接收目標矩形的水準位移（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="fa7bf-110">Receives the horizontal offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa7bf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa7bf-111">Return value</span></span>

<span data-ttu-id="fa7bf-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fa7bf-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa7bf-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fa7bf-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa7bf-114">備註</span><span class="sxs-lookup"><span data-stu-id="fa7bf-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa7bf-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="fa7bf-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fa7bf-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fa7bf-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fa7bf-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="fa7bf-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa7bf-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa7bf-118">Requirements</span></span>



| <span data-ttu-id="fa7bf-119">需求</span><span class="sxs-lookup"><span data-stu-id="fa7bf-119">Requirement</span></span> | <span data-ttu-id="fa7bf-120">值</span><span class="sxs-lookup"><span data-stu-id="fa7bf-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7bf-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fa7bf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fa7bf-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa7bf-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fa7bf-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="fa7bf-123">Library</span></span><br/> | <dl> <span data-ttu-id="fa7bf-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa7bf-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa7bf-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa7bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa7bf-126">**IDxtCompositor 介面**</span><span class="sxs-lookup"><span data-stu-id="fa7bf-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




