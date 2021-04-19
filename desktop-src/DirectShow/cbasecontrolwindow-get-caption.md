---
description: 取得 \_ 標題方法會抓取目前的視窗標題。
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: 'CBaseControlWindow.get_Caption 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997650"
---
# <a name="cbasecontrolwindowget_caption-method"></a><span data-ttu-id="49fe1-103">CBaseControlWindow. 取得 \_ Caption 方法</span><span class="sxs-lookup"><span data-stu-id="49fe1-103">CBaseControlWindow.get\_Caption method</span></span>

<span data-ttu-id="49fe1-104">方法會抓取 `get_Caption` 目前的視窗標題。</span><span class="sxs-lookup"><span data-stu-id="49fe1-104">The `get_Caption` method retrieves the current window caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="49fe1-105">語法</span><span class="sxs-lookup"><span data-stu-id="49fe1-105">Syntax</span></span>


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a><span data-ttu-id="49fe1-106">參數</span><span class="sxs-lookup"><span data-stu-id="49fe1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49fe1-107">*pstrCaption*</span><span class="sxs-lookup"><span data-stu-id="49fe1-107">*pstrCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="49fe1-108">目前視窗標題的指標。</span><span class="sxs-lookup"><span data-stu-id="49fe1-108">Pointer to the current window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49fe1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="49fe1-109">Return value</span></span>

<span data-ttu-id="49fe1-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="49fe1-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49fe1-111">備註</span><span class="sxs-lookup"><span data-stu-id="49fe1-111">Remarks</span></span>

<span data-ttu-id="49fe1-112">Windows 桌上型電腦上大部分的最上層視窗都有標題 (標題) 與其相關聯。</span><span class="sxs-lookup"><span data-stu-id="49fe1-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="49fe1-113">您可以透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面來查詢和設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="49fe1-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="49fe1-114">只有在視窗已套用 WS 標題樣式時，才會顯示任何標題集 \_ 。</span><span class="sxs-lookup"><span data-stu-id="49fe1-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="49fe1-115">如果沒有，標題仍可 (設定，並) 抓取，但使用者看不到它。</span><span class="sxs-lookup"><span data-stu-id="49fe1-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="49fe1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="49fe1-116">Requirements</span></span>



| <span data-ttu-id="49fe1-117">需求</span><span class="sxs-lookup"><span data-stu-id="49fe1-117">Requirement</span></span> | <span data-ttu-id="49fe1-118">值</span><span class="sxs-lookup"><span data-stu-id="49fe1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49fe1-119">標頭</span><span class="sxs-lookup"><span data-stu-id="49fe1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="49fe1-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="49fe1-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49fe1-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="49fe1-121">Library</span></span><br/> | <dl> <span data-ttu-id="49fe1-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="49fe1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49fe1-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49fe1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49fe1-124">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="49fe1-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




