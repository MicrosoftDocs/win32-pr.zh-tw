---
description: SetWindowForeground 方法會將影片視窗移至前景，並選擇性地提供焦點。
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: 'CBaseControlWindow. SetWindowForeground 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997748"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a><span data-ttu-id="fded9-103">CBaseControlWindow. SetWindowForeground 方法</span><span class="sxs-lookup"><span data-stu-id="fded9-103">CBaseControlWindow.SetWindowForeground method</span></span>

<span data-ttu-id="fded9-104">`SetWindowForeground`方法會將影片視窗移至前景，並選擇性地提供焦點。</span><span class="sxs-lookup"><span data-stu-id="fded9-104">The `SetWindowForeground` method moves the video window to the foreground and optionally gives it focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="fded9-105">語法</span><span class="sxs-lookup"><span data-stu-id="fded9-105">Syntax</span></span>


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a><span data-ttu-id="fded9-106">參數</span><span class="sxs-lookup"><span data-stu-id="fded9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fded9-107">*重點*</span><span class="sxs-lookup"><span data-stu-id="fded9-107">*Focus*</span></span> 
</dt> <dd>

<span data-ttu-id="fded9-108">值，指定影片視窗是否將取得焦點。</span><span class="sxs-lookup"><span data-stu-id="fded9-108">Value that specifies whether the video window will get focus.</span></span> <span data-ttu-id="fded9-109">值為1會提供視窗焦點，0則否。</span><span class="sxs-lookup"><span data-stu-id="fded9-109">A value of  1 gives the window focus and 0 does not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fded9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fded9-110">Return value</span></span>

<span data-ttu-id="fded9-111">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fded9-111">Returns one of the following values.</span></span>



| <span data-ttu-id="fded9-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fded9-112">Return code</span></span>                                                                                           | <span data-ttu-id="fded9-113">Description</span><span class="sxs-lookup"><span data-stu-id="fded9-113">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fded9-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="fded9-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="fded9-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="fded9-115">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="fded9-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fded9-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="fded9-117">焦點不等於1或0。</span><span class="sxs-lookup"><span data-stu-id="fded9-117">Focus doesn't equal  1 or 0.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fded9-118"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="fded9-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="fded9-119">目前的篩選未連接到完整的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="fded9-119">The current filter isn't connected to a complete filter graph.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fded9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="fded9-120">Requirements</span></span>



| <span data-ttu-id="fded9-121">需求</span><span class="sxs-lookup"><span data-stu-id="fded9-121">Requirement</span></span> | <span data-ttu-id="fded9-122">值</span><span class="sxs-lookup"><span data-stu-id="fded9-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fded9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fded9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fded9-124"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fded9-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fded9-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="fded9-125">Library</span></span><br/> | <dl> <span data-ttu-id="fded9-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fded9-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fded9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fded9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fded9-128">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="fded9-128">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




