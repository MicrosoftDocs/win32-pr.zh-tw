---
description: Get \_ FullScreenMode 方法會抓取目前的全螢幕模式。
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: 'CBaseControlWindow.get_FullScreenMode 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978776"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a><span data-ttu-id="58fe7-103">CBaseControlWindow. 取得 \_ FullScreenMode 方法</span><span class="sxs-lookup"><span data-stu-id="58fe7-103">CBaseControlWindow.get\_FullScreenMode method</span></span>

<span data-ttu-id="58fe7-104">方法會抓取 `get_FullScreenMode` 目前的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="58fe7-104">The `get_FullScreenMode` method retrieves the current full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="58fe7-105">語法</span><span class="sxs-lookup"><span data-stu-id="58fe7-105">Syntax</span></span>


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="58fe7-106">參數</span><span class="sxs-lookup"><span data-stu-id="58fe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58fe7-107">*FullScreenMode*</span><span class="sxs-lookup"><span data-stu-id="58fe7-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="58fe7-108">目前全螢幕模式的指標。</span><span class="sxs-lookup"><span data-stu-id="58fe7-108">Pointer to the current full-screen mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58fe7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="58fe7-109">Return value</span></span>

<span data-ttu-id="58fe7-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="58fe7-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58fe7-111">備註</span><span class="sxs-lookup"><span data-stu-id="58fe7-111">Remarks</span></span>

<span data-ttu-id="58fe7-112">依預設，此成員函式會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="58fe7-112">This member function returns E\_NOTIMPL by default.</span></span> <span data-ttu-id="58fe7-113">這會通知 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 外掛程式散發者，此轉譯器不會執行全螢幕轉譯器。</span><span class="sxs-lookup"><span data-stu-id="58fe7-113">This informs the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor that this renderer does not implement a full-screen renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="58fe7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="58fe7-114">Requirements</span></span>



| <span data-ttu-id="58fe7-115">需求</span><span class="sxs-lookup"><span data-stu-id="58fe7-115">Requirement</span></span> | <span data-ttu-id="58fe7-116">值</span><span class="sxs-lookup"><span data-stu-id="58fe7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58fe7-117">標頭</span><span class="sxs-lookup"><span data-stu-id="58fe7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="58fe7-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="58fe7-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="58fe7-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="58fe7-119">Library</span></span><br/> | <dl> <span data-ttu-id="58fe7-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="58fe7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58fe7-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58fe7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58fe7-122">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="58fe7-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




