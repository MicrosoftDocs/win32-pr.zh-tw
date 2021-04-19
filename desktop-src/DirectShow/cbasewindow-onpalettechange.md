---
description: OnPaletteChange 方法會處理調色板變更訊息。
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: 'CBaseWindow. OnPaletteChange 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994211"
---
# <a name="cbasewindowonpalettechange-method"></a><span data-ttu-id="0758c-103">CBaseWindow. OnPaletteChange 方法</span><span class="sxs-lookup"><span data-stu-id="0758c-103">CBaseWindow.OnPaletteChange method</span></span>

<span data-ttu-id="0758c-104">`OnPaletteChange`方法會處理調色板變更訊息。</span><span class="sxs-lookup"><span data-stu-id="0758c-104">The `OnPaletteChange` method handles palette-change messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="0758c-105">語法</span><span class="sxs-lookup"><span data-stu-id="0758c-105">Syntax</span></span>


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a><span data-ttu-id="0758c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0758c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0758c-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="0758c-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0758c-108">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0758c-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="0758c-109">*訊息*</span><span class="sxs-lookup"><span data-stu-id="0758c-109">*Message*</span></span> 
</dt> <dd>

<span data-ttu-id="0758c-110">訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="0758c-110">Message identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0758c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0758c-111">Return value</span></span>

<span data-ttu-id="0758c-112">如果已處理訊息，則傳回 0; 如果未處理訊息，則傳回1。</span><span class="sxs-lookup"><span data-stu-id="0758c-112">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0758c-113">備註</span><span class="sxs-lookup"><span data-stu-id="0758c-113">Remarks</span></span>

<span data-ttu-id="0758c-114">這個方法會處理 WM \_ PALETTECHANGED 和 wm \_ QUERYNEWPALETTE 訊息。</span><span class="sxs-lookup"><span data-stu-id="0758c-114">This method handles WM\_PALETTECHANGED and WM\_QUERYNEWPALETTE messages.</span></span> <span data-ttu-id="0758c-115">它會呼叫 [**CBaseWindow：:D orealisepalette**](cbasewindow-dorealisepalette.md) 方法，以實現新的調色板。</span><span class="sxs-lookup"><span data-stu-id="0758c-115">It calls the [**CBaseWindow::DoRealisePalette**](cbasewindow-dorealisepalette.md) method to realize the new palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="0758c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0758c-116">Requirements</span></span>



| <span data-ttu-id="0758c-117">需求</span><span class="sxs-lookup"><span data-stu-id="0758c-117">Requirement</span></span> | <span data-ttu-id="0758c-118">值</span><span class="sxs-lookup"><span data-stu-id="0758c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0758c-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0758c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0758c-120"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0758c-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0758c-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="0758c-121">Library</span></span><br/> | <dl> <span data-ttu-id="0758c-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0758c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0758c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0758c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0758c-124">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="0758c-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




