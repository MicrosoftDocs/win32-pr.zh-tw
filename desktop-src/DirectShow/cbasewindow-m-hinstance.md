---
description: 模組實例的控制碼。
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'CBaseWindow：： m_hInstance 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999141"
---
# <a name="cbasewindowm_hinstance-member"></a><span data-ttu-id="71b2d-103">CBaseWindow：： m \_ hInstance 成員</span><span class="sxs-lookup"><span data-stu-id="71b2d-103">CBaseWindow::m\_hInstance member</span></span>

<span data-ttu-id="71b2d-104">模組實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="71b2d-104">Handle to the module instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="71b2d-105">Syntax</span></span>


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a><span data-ttu-id="71b2d-106">備註</span><span class="sxs-lookup"><span data-stu-id="71b2d-106">Remarks</span></span>

<span data-ttu-id="71b2d-107">DLL 進入點函數會使用模組實例的控制碼來設定全域變數。</span><span class="sxs-lookup"><span data-stu-id="71b2d-107">The DLL entry point function sets a global variable with a handle to the module instance.</span></span> <span data-ttu-id="71b2d-108">**CBaseWindow** 類別會將此控制碼儲存在其函式方法中。</span><span class="sxs-lookup"><span data-stu-id="71b2d-108">The **CBaseWindow** class stores this handle in its constructor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b2d-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="71b2d-109">Requirements</span></span>



| <span data-ttu-id="71b2d-110">需求</span><span class="sxs-lookup"><span data-stu-id="71b2d-110">Requirement</span></span> | <span data-ttu-id="71b2d-111">值</span><span class="sxs-lookup"><span data-stu-id="71b2d-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71b2d-112">標頭</span><span class="sxs-lookup"><span data-stu-id="71b2d-112">Header</span></span><br/>  | <dl> <span data-ttu-id="71b2d-113"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="71b2d-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71b2d-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="71b2d-114">Library</span></span><br/> | <dl> <span data-ttu-id="71b2d-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="71b2d-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b2d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71b2d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b2d-117">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="71b2d-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




