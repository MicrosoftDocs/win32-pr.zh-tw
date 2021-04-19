---
description: Put \_ FullScreenMode 方法會設定轉譯器的全螢幕模式。
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: 'CBaseControlWindow.put_FullScreenMode 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999356"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a><span data-ttu-id="0bc84-103">CBaseControlWindow. put \_ FullScreenMode 方法</span><span class="sxs-lookup"><span data-stu-id="0bc84-103">CBaseControlWindow.put\_FullScreenMode method</span></span>

<span data-ttu-id="0bc84-104">方法會設定轉譯器 `put_FullScreenMode` 的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="0bc84-104">The `put_FullScreenMode` method sets the full-screen mode of the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc84-105">語法</span><span class="sxs-lookup"><span data-stu-id="0bc84-105">Syntax</span></span>


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="0bc84-106">參數</span><span class="sxs-lookup"><span data-stu-id="0bc84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc84-107">*FullScreenMode*</span><span class="sxs-lookup"><span data-stu-id="0bc84-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="0bc84-108">要套用的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="0bc84-108">Full-screen mode to apply.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc84-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0bc84-109">Return value</span></span>

<span data-ttu-id="0bc84-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0bc84-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0bc84-111">目前的執行會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0bc84-111">The current implementation returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc84-112">備註</span><span class="sxs-lookup"><span data-stu-id="0bc84-112">Remarks</span></span>

<span data-ttu-id="0bc84-113">執行全螢幕模式的影片轉譯器應該覆寫這個成員函式，並執行它所支援的任何模式。</span><span class="sxs-lookup"><span data-stu-id="0bc84-113">A video renderer that implements a full-screen mode should override this member function and implement whatever modes it supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bc84-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bc84-114">Requirements</span></span>



| <span data-ttu-id="0bc84-115">需求</span><span class="sxs-lookup"><span data-stu-id="0bc84-115">Requirement</span></span> | <span data-ttu-id="0bc84-116">值</span><span class="sxs-lookup"><span data-stu-id="0bc84-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc84-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0bc84-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0bc84-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0bc84-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0bc84-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0bc84-119">Library</span></span><br/> | <dl> <span data-ttu-id="0bc84-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0bc84-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bc84-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bc84-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc84-122">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="0bc84-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




