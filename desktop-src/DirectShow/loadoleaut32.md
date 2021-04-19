---
description: LoadOLEAut32 函式會將 Automation 動態連結程式庫 (OleAut32.dll) 載入。
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: 'LoadOLEAut32 函式 (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986179"
---
# <a name="loadoleaut32-function"></a><span data-ttu-id="c4626-103">LoadOLEAut32 函式</span><span class="sxs-lookup"><span data-stu-id="c4626-103">LoadOLEAut32 function</span></span>

<span data-ttu-id="c4626-104">**LoadOLEAut32** 函式會將 Automation 動態連結程式庫 (OleAut32.dll) 載入。</span><span class="sxs-lookup"><span data-stu-id="c4626-104">The **LoadOLEAut32** function loads the Automation dynamic-link library (OleAut32.dll).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4626-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4626-105">Syntax</span></span>


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a><span data-ttu-id="c4626-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4626-106">Parameters</span></span>

<span data-ttu-id="c4626-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="c4626-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4626-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4626-108">Return value</span></span>

<span data-ttu-id="c4626-109">傳回 Automation DLL 實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c4626-109">Returns a handle to an Automation DLL instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4626-110">備註</span><span class="sxs-lookup"><span data-stu-id="c4626-110">Remarks</span></span>

<span data-ttu-id="c4626-111">當 [**CBaseObject**](cbaseobject.md) 的函式終結 OleAut32.dll 載入的物件時，它會卸載程式庫（如果仍載入）。</span><span class="sxs-lookup"><span data-stu-id="c4626-111">When the [**CBaseObject**](cbaseobject.md) destructor destroys the object that loaded OleAut32.dll, it will unload the library if it is still loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4626-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4626-112">Requirements</span></span>



| <span data-ttu-id="c4626-113">需求</span><span class="sxs-lookup"><span data-stu-id="c4626-113">Requirement</span></span> | <span data-ttu-id="c4626-114">值</span><span class="sxs-lookup"><span data-stu-id="c4626-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4626-115">標頭</span><span class="sxs-lookup"><span data-stu-id="c4626-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c4626-116"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c4626-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c4626-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="c4626-117">Library</span></span><br/> | <dl> <span data-ttu-id="c4626-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c4626-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4626-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4626-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4626-120">**COM Helper 函數**</span><span class="sxs-lookup"><span data-stu-id="c4626-120">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




