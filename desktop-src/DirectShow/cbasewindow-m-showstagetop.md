---
description: 將視窗樣式設定為 WS \_ EX 最上層的私用訊息 \_ 。
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: 'CBaseWindow：： m_ShowStageTop 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageTop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ed0069c5c65f2bb1a113c899e2d90de0cabcd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992834"
---
# <a name="cbasewindowm_showstagetop-member"></a><span data-ttu-id="03764-103">CBaseWindow：： m \_ ShowStageTop 成員</span><span class="sxs-lookup"><span data-stu-id="03764-103">CBaseWindow::m\_ShowStageTop member</span></span>

<span data-ttu-id="03764-104">將視窗樣式設定為 WS \_ EX 最上層的私用訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="03764-104">Private message that sets the window style to WS\_EX\_TOPMOST.</span></span>

## <a name="syntax"></a><span data-ttu-id="03764-105">語法</span><span class="sxs-lookup"><span data-stu-id="03764-105">Syntax</span></span>


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a><span data-ttu-id="03764-106">備註</span><span class="sxs-lookup"><span data-stu-id="03764-106">Remarks</span></span>

<span data-ttu-id="03764-107">如果影片轉譯器切換至全螢幕模式，則應該將此訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="03764-107">Video renderers should send this message to the window if they switch to full-screen mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="03764-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="03764-108">Requirements</span></span>



| <span data-ttu-id="03764-109">需求</span><span class="sxs-lookup"><span data-stu-id="03764-109">Requirement</span></span> | <span data-ttu-id="03764-110">值</span><span class="sxs-lookup"><span data-stu-id="03764-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03764-111">標頭</span><span class="sxs-lookup"><span data-stu-id="03764-111">Header</span></span><br/>  | <dl> <span data-ttu-id="03764-112"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="03764-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03764-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="03764-113">Library</span></span><br/> | <dl> <span data-ttu-id="03764-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="03764-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03764-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03764-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03764-116">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="03764-116">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




