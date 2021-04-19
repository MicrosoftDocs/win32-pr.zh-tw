---
description: ApplyChanges 方法會套用已變更的任何屬性。
ms.assetid: dece1e61-7fe1-40f1-8d1d-89b5a334d04e
title: 'IDxtJpeg：： ApplyChanges 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.ApplyChanges
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 522df2fc362b0332d4eb41e9a2f10201bfcdec9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987040"
---
# <a name="idxtjpegapplychanges-method"></a><span data-ttu-id="38d2e-103">IDxtJpeg：： ApplyChanges 方法</span><span class="sxs-lookup"><span data-stu-id="38d2e-103">IDxtJpeg::ApplyChanges method</span></span>

> [!Note]  
> <span data-ttu-id="38d2e-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="38d2e-104">\[Deprecated.</span></span> <span data-ttu-id="38d2e-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="38d2e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="38d2e-106">`ApplyChanges`方法會套用已變更的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="38d2e-106">The `ApplyChanges` method applies any properties that have changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d2e-107">語法</span><span class="sxs-lookup"><span data-stu-id="38d2e-107">Syntax</span></span>


```C++
HRESULT ApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="38d2e-108">參數</span><span class="sxs-lookup"><span data-stu-id="38d2e-108">Parameters</span></span>

<span data-ttu-id="38d2e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="38d2e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38d2e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="38d2e-110">Return value</span></span>

<span data-ttu-id="38d2e-111">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="38d2e-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38d2e-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="38d2e-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="38d2e-113">備註</span><span class="sxs-lookup"><span data-stu-id="38d2e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="38d2e-114">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="38d2e-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="38d2e-115">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="38d2e-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="38d2e-116">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="38d2e-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="38d2e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="38d2e-117">Requirements</span></span>



| <span data-ttu-id="38d2e-118">需求</span><span class="sxs-lookup"><span data-stu-id="38d2e-118">Requirement</span></span> | <span data-ttu-id="38d2e-119">值</span><span class="sxs-lookup"><span data-stu-id="38d2e-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38d2e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="38d2e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="38d2e-121"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="38d2e-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="38d2e-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="38d2e-122">Library</span></span><br/> | <dl> <span data-ttu-id="38d2e-123"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="38d2e-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d2e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38d2e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d2e-125">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="38d2e-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




