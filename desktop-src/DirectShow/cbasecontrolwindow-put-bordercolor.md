---
description: Put 邊框 \_ 型方法會變更框線色彩。
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: 'CBaseControlWindow.put_BorderColor 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000814"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a><span data-ttu-id="12301-103">CBaseControlWindow。 put \_ 邊框方法</span><span class="sxs-lookup"><span data-stu-id="12301-103">CBaseControlWindow.put\_BorderColor method</span></span>

<span data-ttu-id="12301-104">`put_BorderColor`方法會變更框線色彩。</span><span class="sxs-lookup"><span data-stu-id="12301-104">The `put_BorderColor` method changes the border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="12301-105">語法</span><span class="sxs-lookup"><span data-stu-id="12301-105">Syntax</span></span>


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a><span data-ttu-id="12301-106">參數</span><span class="sxs-lookup"><span data-stu-id="12301-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12301-107">*色彩*</span><span class="sxs-lookup"><span data-stu-id="12301-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="12301-108">新的框線色彩。</span><span class="sxs-lookup"><span data-stu-id="12301-108">New border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12301-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="12301-109">Return value</span></span>

<span data-ttu-id="12301-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="12301-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12301-111">備註</span><span class="sxs-lookup"><span data-stu-id="12301-111">Remarks</span></span>

<span data-ttu-id="12301-112">應用程式可以建立應顯示影片的目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="12301-112">An application can establish a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="12301-113">這個矩形相對於視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="12301-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="12301-114">如果這樣做 (預設為一律繪製整個視窗) ，則會在影片周圍加上框線。</span><span class="sxs-lookup"><span data-stu-id="12301-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="12301-115">這個屬性會影響框線所使用的色彩。</span><span class="sxs-lookup"><span data-stu-id="12301-115">This property affects the color used by the border.</span></span> <span data-ttu-id="12301-116">雖然參數指定為 **LONG** 類型，但其實是 **COLORREF** 值。</span><span class="sxs-lookup"><span data-stu-id="12301-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="12301-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="12301-117">Requirements</span></span>



| <span data-ttu-id="12301-118">需求</span><span class="sxs-lookup"><span data-stu-id="12301-118">Requirement</span></span> | <span data-ttu-id="12301-119">值</span><span class="sxs-lookup"><span data-stu-id="12301-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12301-120">標頭</span><span class="sxs-lookup"><span data-stu-id="12301-120">Header</span></span><br/>  | <dl> <span data-ttu-id="12301-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="12301-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12301-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="12301-122">Library</span></span><br/> | <dl> <span data-ttu-id="12301-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="12301-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12301-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12301-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12301-125">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="12301-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




