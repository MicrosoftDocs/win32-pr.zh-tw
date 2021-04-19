---
description: IAMTimelineSplittable 介面會將 DirectShow 編輯服務中的時間軸物件分割 (DES) 。 來源、效果、轉換和追蹤都會執行這個介面。
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: 'IAMTimelineSplittable 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981264"
---
# <a name="iamtimelinesplittable-interface"></a><span data-ttu-id="ec872-104">IAMTimelineSplittable 介面</span><span class="sxs-lookup"><span data-stu-id="ec872-104">IAMTimelineSplittable interface</span></span>

> [!Note]  
> <span data-ttu-id="ec872-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ec872-105">\[Deprecated.</span></span> <span data-ttu-id="ec872-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ec872-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ec872-107">介面會將 `IAMTimelineSplittable` [DirectShow 編輯服務](directshow-editing-services.md) 中的時間軸物件分割 (DES) 。</span><span class="sxs-lookup"><span data-stu-id="ec872-107">The `IAMTimelineSplittable` interface splits a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="ec872-108">來源、效果、轉換和追蹤都會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="ec872-108">Sources, effects, transitions, and tracks implement this interface.</span></span>

## <a name="members"></a><span data-ttu-id="ec872-109">成員</span><span class="sxs-lookup"><span data-stu-id="ec872-109">Members</span></span>

<span data-ttu-id="ec872-110">**IAMTimelineSplittable** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="ec872-110">The **IAMTimelineSplittable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ec872-111">**IAMTimelineSplittable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ec872-111">**IAMTimelineSplittable** also has these types of members:</span></span>

-   [<span data-ttu-id="ec872-112">方法</span><span class="sxs-lookup"><span data-stu-id="ec872-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ec872-113">方法</span><span class="sxs-lookup"><span data-stu-id="ec872-113">Methods</span></span>

<span data-ttu-id="ec872-114">**IAMTimelineSplittable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ec872-114">The **IAMTimelineSplittable** interface has these methods.</span></span>



| <span data-ttu-id="ec872-115">方法</span><span class="sxs-lookup"><span data-stu-id="ec872-115">Method</span></span>                                             | <span data-ttu-id="ec872-116">描述</span><span class="sxs-lookup"><span data-stu-id="ec872-116">Description</span></span>                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec872-117">**SplitAt**</span><span class="sxs-lookup"><span data-stu-id="ec872-117">**SplitAt**</span></span>](iamtimelinesplittable-splitat.md)   | <span data-ttu-id="ec872-118">在指定的時間分割物件。</span><span class="sxs-lookup"><span data-stu-id="ec872-118">Splits the object at the specified time.</span></span><br/>                                                  |
| [<span data-ttu-id="ec872-119">**SplitAt2**</span><span class="sxs-lookup"><span data-stu-id="ec872-119">**SplitAt2**</span></span>](iamtimelinesplittable-splitat2.md) | <span data-ttu-id="ec872-120">在指定的時間分割物件，指定為 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="ec872-120">Splits the object at the specified time, specified as a [**REFTIME**](reftime.md) value.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec872-121">備註</span><span class="sxs-lookup"><span data-stu-id="ec872-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ec872-122">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ec872-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ec872-123">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ec872-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ec872-124">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ec872-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec872-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec872-125">Requirements</span></span>



| <span data-ttu-id="ec872-126">需求</span><span class="sxs-lookup"><span data-stu-id="ec872-126">Requirement</span></span> | <span data-ttu-id="ec872-127">值</span><span class="sxs-lookup"><span data-stu-id="ec872-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec872-128">標頭</span><span class="sxs-lookup"><span data-stu-id="ec872-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ec872-129"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec872-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ec872-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="ec872-130">Library</span></span><br/> | <dl> <span data-ttu-id="ec872-131"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec872-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
