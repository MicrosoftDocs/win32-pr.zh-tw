---
description: 指定視窗是否張貼或傳送其損毀訊息的旗標。
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'CBaseWindow：： m_bDoPostToDestroy 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993444"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a><span data-ttu-id="03554-103">CBaseWindow：： m \_ bDoPostToDestroy 成員</span><span class="sxs-lookup"><span data-stu-id="03554-103">CBaseWindow::m\_bDoPostToDestroy member</span></span>

<span data-ttu-id="03554-104">指定視窗是否張貼或傳送其損毀訊息的旗標。</span><span class="sxs-lookup"><span data-stu-id="03554-104">Flag that specifies whether the window posts or sends its destruction message.</span></span> <span data-ttu-id="03554-105">若 **為 TRUE**， [**CBaseWindow：:D onewithwindow**](cbasewindow-donewithwindow.md) 方法會使用 **PostMessage** 函式，將私用的終結訊息傳送給自己。</span><span class="sxs-lookup"><span data-stu-id="03554-105">If **TRUE**, the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method uses the **PostMessage** function to send itself a private destruction message.</span></span> <span data-ttu-id="03554-106">如果 **為 FALSE**，則 **DoneWithWindow** 會使用 **SendMessage** 函數來傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="03554-106">If **FALSE**, **DoneWithWindow** uses the **SendMessage** function to send the message.</span></span> <span data-ttu-id="03554-107">依預設，此值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="03554-107">By default, the value is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="03554-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="03554-108">Syntax</span></span>


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a><span data-ttu-id="03554-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="03554-109">Requirements</span></span>



| <span data-ttu-id="03554-110">需求</span><span class="sxs-lookup"><span data-stu-id="03554-110">Requirement</span></span> | <span data-ttu-id="03554-111">值</span><span class="sxs-lookup"><span data-stu-id="03554-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03554-112">標頭</span><span class="sxs-lookup"><span data-stu-id="03554-112">Header</span></span><br/>  | <dl> <span data-ttu-id="03554-113"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="03554-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03554-114">程式庫</span><span class="sxs-lookup"><span data-stu-id="03554-114">Library</span></span><br/> | <dl> <span data-ttu-id="03554-115"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="03554-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03554-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03554-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03554-117">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="03554-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




