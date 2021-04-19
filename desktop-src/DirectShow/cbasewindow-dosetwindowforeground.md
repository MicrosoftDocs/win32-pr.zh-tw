---
description: DoSetWindowForeground 方法會將視窗帶入前景。
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: 'CBaseWindow. DoSetWindowForeground 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16a4c8bf41c042c99624289fa26fe252dee62747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987011"
---
# <a name="cbasewindowdosetwindowforeground-method"></a><span data-ttu-id="97312-103">CBaseWindow. DoSetWindowForeground 方法</span><span class="sxs-lookup"><span data-stu-id="97312-103">CBaseWindow.DoSetWindowForeground method</span></span>

<span data-ttu-id="97312-104">方法會將 `DoSetWindowForeground` 視窗帶到前景。</span><span class="sxs-lookup"><span data-stu-id="97312-104">The `DoSetWindowForeground` method brings the window to the foreground.</span></span>

## <a name="syntax"></a><span data-ttu-id="97312-105">語法</span><span class="sxs-lookup"><span data-stu-id="97312-105">Syntax</span></span>


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a><span data-ttu-id="97312-106">參數</span><span class="sxs-lookup"><span data-stu-id="97312-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97312-107">*bFocus*</span><span class="sxs-lookup"><span data-stu-id="97312-107">*bFocus*</span></span> 
</dt> <dd>

<span data-ttu-id="97312-108">指定是否要提供視窗焦點的布林值。</span><span class="sxs-lookup"><span data-stu-id="97312-108">Boolean value that specifies whether to give the window focus.</span></span> <span data-ttu-id="97312-109">如果值為 **TRUE**，則視窗會取得焦點。</span><span class="sxs-lookup"><span data-stu-id="97312-109">If the value is **TRUE**, the window gains focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97312-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="97312-110">Return value</span></span>

<span data-ttu-id="97312-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="97312-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="97312-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="97312-112">Requirements</span></span>



| <span data-ttu-id="97312-113">需求</span><span class="sxs-lookup"><span data-stu-id="97312-113">Requirement</span></span> | <span data-ttu-id="97312-114">值</span><span class="sxs-lookup"><span data-stu-id="97312-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97312-115">標頭</span><span class="sxs-lookup"><span data-stu-id="97312-115">Header</span></span><br/>  | <dl> <span data-ttu-id="97312-116"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="97312-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="97312-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="97312-117">Library</span></span><br/> | <dl> <span data-ttu-id="97312-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="97312-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97312-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97312-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97312-120">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="97312-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




