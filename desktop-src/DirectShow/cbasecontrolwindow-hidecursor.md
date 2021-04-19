---
description: HideCursor 方法會隱藏或顯示資料指標。
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: 'CBaseControlWindow. HideCursor 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999266"
---
# <a name="cbasecontrolwindowhidecursor-method"></a><span data-ttu-id="685ec-103">CBaseControlWindow. HideCursor 方法</span><span class="sxs-lookup"><span data-stu-id="685ec-103">CBaseControlWindow.HideCursor method</span></span>

<span data-ttu-id="685ec-104">`HideCursor`方法會隱藏或顯示資料指標。</span><span class="sxs-lookup"><span data-stu-id="685ec-104">The `HideCursor` method hides or displays the cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="685ec-105">語法</span><span class="sxs-lookup"><span data-stu-id="685ec-105">Syntax</span></span>


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a><span data-ttu-id="685ec-106">參數</span><span class="sxs-lookup"><span data-stu-id="685ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685ec-107">*HideCursor*</span><span class="sxs-lookup"><span data-stu-id="685ec-107">*HideCursor*</span></span> 
</dt> <dd>

<span data-ttu-id="685ec-108">值，指定是否要顯示資料指標。</span><span class="sxs-lookup"><span data-stu-id="685ec-108">Value specifying whether to show the cursor.</span></span> <span data-ttu-id="685ec-109">設定為 [OATRUE] 可隱藏資料指標，或設定為 [OAFALSE] 以顯示資料指標。</span><span class="sxs-lookup"><span data-stu-id="685ec-109">Set to OATRUE to hide the cursor, or OAFALSE to display the cursor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685ec-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="685ec-110">Return value</span></span>

<span data-ttu-id="685ec-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="685ec-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="685ec-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="685ec-112">Requirements</span></span>



| <span data-ttu-id="685ec-113">需求</span><span class="sxs-lookup"><span data-stu-id="685ec-113">Requirement</span></span> | <span data-ttu-id="685ec-114">值</span><span class="sxs-lookup"><span data-stu-id="685ec-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685ec-115">標頭</span><span class="sxs-lookup"><span data-stu-id="685ec-115">Header</span></span><br/>  | <dl> <span data-ttu-id="685ec-116"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="685ec-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="685ec-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="685ec-117">Library</span></span><br/> | <dl> <span data-ttu-id="685ec-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="685ec-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="685ec-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="685ec-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685ec-120">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="685ec-120">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




