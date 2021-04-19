---
description: Put BorderWidth 方法會在抹除 \_ 模式的邊緣指定實線框線的寬度。
ms.assetid: a618926a-efa4-47a2-9ce9-ae298ed41083
title: 'IDxtJpeg：:p ut_BorderWidth 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df7435b8a516b818b6d7c86e907ba75cce86f6c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990797"
---
# <a name="idxtjpegput_borderwidth-method"></a><span data-ttu-id="88e0e-103">IDxtJpeg：:p 的 \_ BorderWidth 方法</span><span class="sxs-lookup"><span data-stu-id="88e0e-103">IDxtJpeg::put\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="88e0e-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="88e0e-104">\[Deprecated.</span></span> <span data-ttu-id="88e0e-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="88e0e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="88e0e-106">方法會在抹除 `put_BorderWidth` 模式的邊緣指定實線框線的寬度。</span><span class="sxs-lookup"><span data-stu-id="88e0e-106">The `put_BorderWidth` method specifies the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="88e0e-107">語法</span><span class="sxs-lookup"><span data-stu-id="88e0e-107">Syntax</span></span>


```C++
HRESULT put_BorderWidth(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="88e0e-108">參數</span><span class="sxs-lookup"><span data-stu-id="88e0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88e0e-109">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="88e0e-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88e0e-110">框線的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="88e0e-110">The width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88e0e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="88e0e-111">Return value</span></span>

<span data-ttu-id="88e0e-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="88e0e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88e0e-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="88e0e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88e0e-114">備註</span><span class="sxs-lookup"><span data-stu-id="88e0e-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="88e0e-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="88e0e-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="88e0e-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="88e0e-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="88e0e-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="88e0e-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88e0e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="88e0e-118">Requirements</span></span>



| <span data-ttu-id="88e0e-119">需求</span><span class="sxs-lookup"><span data-stu-id="88e0e-119">Requirement</span></span> | <span data-ttu-id="88e0e-120">值</span><span class="sxs-lookup"><span data-stu-id="88e0e-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88e0e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="88e0e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="88e0e-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="88e0e-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="88e0e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="88e0e-123">Library</span></span><br/> | <dl> <span data-ttu-id="88e0e-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="88e0e-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88e0e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88e0e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e0e-126">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="88e0e-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




