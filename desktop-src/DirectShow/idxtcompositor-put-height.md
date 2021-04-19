---
description: Put \_ Height 方法會指定目標矩形的高度。
ms.assetid: 032b5468-bce8-4492-abbe-e442131ebe3a
title: 'IDxtCompositor：:p ut_Height 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_Height
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 883a3261b6322a69e0e1612b724a9f570953dc97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976081"
---
# <a name="idxtcompositorput_height-method"></a><span data-ttu-id="898e1-103">IDxtCompositor：:p 內容 \_ 長的高度方法</span><span class="sxs-lookup"><span data-stu-id="898e1-103">IDxtCompositor::put\_Height method</span></span>

> [!Note]  
> <span data-ttu-id="898e1-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="898e1-104">\[Deprecated.</span></span> <span data-ttu-id="898e1-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="898e1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="898e1-106">`put_Height`方法會指定目標矩形的高度。</span><span class="sxs-lookup"><span data-stu-id="898e1-106">The `put_Height` method specifies the height of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="898e1-107">語法</span><span class="sxs-lookup"><span data-stu-id="898e1-107">Syntax</span></span>


```C++
HRESULT put_Height(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="898e1-108">參數</span><span class="sxs-lookup"><span data-stu-id="898e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="898e1-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="898e1-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="898e1-110">目標矩形的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="898e1-110">The height of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="898e1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="898e1-111">Return value</span></span>

<span data-ttu-id="898e1-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="898e1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="898e1-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="898e1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="898e1-114">備註</span><span class="sxs-lookup"><span data-stu-id="898e1-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="898e1-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="898e1-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="898e1-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="898e1-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="898e1-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="898e1-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="898e1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="898e1-118">Requirements</span></span>



| <span data-ttu-id="898e1-119">需求</span><span class="sxs-lookup"><span data-stu-id="898e1-119">Requirement</span></span> | <span data-ttu-id="898e1-120">值</span><span class="sxs-lookup"><span data-stu-id="898e1-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="898e1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="898e1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="898e1-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="898e1-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="898e1-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="898e1-123">Library</span></span><br/> | <dl> <span data-ttu-id="898e1-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="898e1-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="898e1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="898e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="898e1-126">**IDxtCompositor 介面**</span><span class="sxs-lookup"><span data-stu-id="898e1-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




