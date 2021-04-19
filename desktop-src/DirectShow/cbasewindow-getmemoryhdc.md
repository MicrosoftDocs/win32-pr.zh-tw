---
description: GetMemoryHDC 方法會抓取 (DC) 的記憶體裝置內容控制碼。
ms.assetid: 2c22015f-5948-4e1a-92c7-36f232816175
title: 'CBaseWindow. GetMemoryHDC 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetMemoryHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c255ac8734f364597c09fc15b4aa543b1ec0a0da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977514"
---
# <a name="cbasewindowgetmemoryhdc-method"></a><span data-ttu-id="f2e53-103">CBaseWindow. GetMemoryHDC 方法</span><span class="sxs-lookup"><span data-stu-id="f2e53-103">CBaseWindow.GetMemoryHDC method</span></span>

<span data-ttu-id="f2e53-104">方法會抓取 `GetMemoryHDC` (DC) 的記憶體裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="f2e53-104">The `GetMemoryHDC` method retrieves a handle to the memory device context (DC).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e53-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2e53-105">Syntax</span></span>


```C++
virtual HDC GetMemoryHDC();
```



## <a name="parameters"></a><span data-ttu-id="f2e53-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2e53-106">Parameters</span></span>

<span data-ttu-id="f2e53-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f2e53-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2e53-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2e53-108">Return value</span></span>

<span data-ttu-id="f2e53-109">傳回記憶體 DC 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f2e53-109">Returns a handle to the memory DC.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e53-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2e53-110">Requirements</span></span>



| <span data-ttu-id="f2e53-111">需求</span><span class="sxs-lookup"><span data-stu-id="f2e53-111">Requirement</span></span> | <span data-ttu-id="f2e53-112">值</span><span class="sxs-lookup"><span data-stu-id="f2e53-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e53-113">標頭</span><span class="sxs-lookup"><span data-stu-id="f2e53-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f2e53-114"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f2e53-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2e53-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="f2e53-115">Library</span></span><br/> | <dl> <span data-ttu-id="f2e53-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f2e53-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e53-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2e53-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e53-118">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="f2e53-118">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




