---
description: 重要區段，用來序列化物件的存取權。
ms.assetid: 24a5b1b2-209e-4262-aa48-fd4534b2da57
title: 'CBaseWindow：： m_WindowLock 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_WindowLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38227e505f2e05e024c8cecf12ab3cb8c336bfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989727"
---
# <a name="cbasewindowm_windowlock-member"></a><span data-ttu-id="febe0-103">CBaseWindow：： m \_ WindowLock 成員</span><span class="sxs-lookup"><span data-stu-id="febe0-103">CBaseWindow::m\_WindowLock member</span></span>

<span data-ttu-id="febe0-104">重要區段，用來序列化物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="febe0-104">Critical section, to serialize access to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="febe0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="febe0-105">Syntax</span></span>


```C++
CCritSec m_WindowLock;
```



## <a name="requirements"></a><span data-ttu-id="febe0-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="febe0-106">Requirements</span></span>



| <span data-ttu-id="febe0-107">需求</span><span class="sxs-lookup"><span data-stu-id="febe0-107">Requirement</span></span> | <span data-ttu-id="febe0-108">值</span><span class="sxs-lookup"><span data-stu-id="febe0-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="febe0-109">標頭</span><span class="sxs-lookup"><span data-stu-id="febe0-109">Header</span></span><br/>  | <dl> <span data-ttu-id="febe0-110"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="febe0-110"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="febe0-111">程式庫</span><span class="sxs-lookup"><span data-stu-id="febe0-111">Library</span></span><br/> | <dl> <span data-ttu-id="febe0-112"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="febe0-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="febe0-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="febe0-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="febe0-114">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="febe0-114">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




