---
description: 這些函式提供在 DirectShow 中執行 IUnknown 介面的支援。
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: 'COM Helper 函數 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996505"
---
# <a name="com-helper-functions"></a><span data-ttu-id="961de-103">COM Helper 函數</span><span class="sxs-lookup"><span data-stu-id="961de-103">COM Helper Functions</span></span>

<span data-ttu-id="961de-104">這些函式提供在 DirectShow 中執行 **IUnknown** 介面的支援。</span><span class="sxs-lookup"><span data-stu-id="961de-104">These functions provide support for implementing the **IUnknown** interface in DirectShow.</span></span>



| <span data-ttu-id="961de-105">函式</span><span class="sxs-lookup"><span data-stu-id="961de-105">Function</span></span>                                               | <span data-ttu-id="961de-106">描述</span><span class="sxs-lookup"><span data-stu-id="961de-106">Description</span></span>                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="961de-107">**宣告 \_ IUNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="961de-107">**DECLARE\_IUNKNOWN**</span></span>](declare-iunknown.md)          | <span data-ttu-id="961de-108">針對新介面宣告基底介面的三種方法。</span><span class="sxs-lookup"><span data-stu-id="961de-108">Declares the three methods of the base interface for a new interface.</span></span> |
| [<span data-ttu-id="961de-109">**GetInterface**</span><span class="sxs-lookup"><span data-stu-id="961de-109">**GetInterface**</span></span>](getinterface.md)                   | <span data-ttu-id="961de-110">抓取所要求用戶端的介面指標。</span><span class="sxs-lookup"><span data-stu-id="961de-110">Retrieves an interface pointer to the requested client.</span></span>               |
| [<span data-ttu-id="961de-111">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="961de-111">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md) | <span data-ttu-id="961de-112">**IUnknown** 介面的 Nondelegating 版本。</span><span class="sxs-lookup"><span data-stu-id="961de-112">Nondelegating version of the **IUnknown** interface.</span></span>                  |
| [<span data-ttu-id="961de-113">**LoadOLEAut32**</span><span class="sxs-lookup"><span data-stu-id="961de-113">**LoadOLEAut32**</span></span>](loadoleaut32.md)                   | <span data-ttu-id="961de-114">載入 Automation DLL (OleAut32.dll) 。</span><span class="sxs-lookup"><span data-stu-id="961de-114">Loads the Automation DLL (OleAut32.dll).</span></span>                              |



 

## <a name="requirements"></a><span data-ttu-id="961de-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="961de-115">Requirements</span></span>



| <span data-ttu-id="961de-116">需求</span><span class="sxs-lookup"><span data-stu-id="961de-116">Requirement</span></span> | <span data-ttu-id="961de-117">值</span><span class="sxs-lookup"><span data-stu-id="961de-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="961de-118">標頭</span><span class="sxs-lookup"><span data-stu-id="961de-118">Header</span></span><br/>  | <dl> <span data-ttu-id="961de-119"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="961de-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="961de-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="961de-120">Library</span></span><br/> | <dl> <span data-ttu-id="961de-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="961de-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="961de-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="961de-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="961de-123">公用程式函數</span><span class="sxs-lookup"><span data-stu-id="961de-123">Utility Functions</span></span>](utility-functions.md)
</dt> </dl>

 

 




