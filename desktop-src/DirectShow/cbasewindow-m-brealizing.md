---
description: 旗標，指定是否要實現新的調色板。 在「偵錯工具組建」中，當選擇區變更時，此值為 TRUE，否則為 FALSE。 零售組建中不會使用此變數。
ms.assetid: 3aba880d-fa22-4745-a2b3-6701c808c4e3
title: 'CBaseWindow：： m_bRealizing 成員 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRealizing
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1eee652d310ca786b7a732fd4de2b23f0dd088fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980128"
---
# <a name="cbasewindowm_brealizing-member"></a><span data-ttu-id="88cac-105">CBaseWindow：： m \_ bRealizing 成員</span><span class="sxs-lookup"><span data-stu-id="88cac-105">CBaseWindow::m\_bRealizing member</span></span>

<span data-ttu-id="88cac-106">旗標，指定是否要實現新的調色板。</span><span class="sxs-lookup"><span data-stu-id="88cac-106">Flag that specifies whether a new palette is being realized.</span></span> <span data-ttu-id="88cac-107">在「偵錯工具組建」中，當選擇區變更時，此值為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="88cac-107">In debug builds, the value is **TRUE** while the palette is changing and **FALSE** otherwise.</span></span> <span data-ttu-id="88cac-108">零售組建中不會使用此變數。</span><span class="sxs-lookup"><span data-stu-id="88cac-108">This variable is not used in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="88cac-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="88cac-109">Syntax</span></span>


```C++
BYTE m_bRealizing;
```



## <a name="requirements"></a><span data-ttu-id="88cac-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="88cac-110">Requirements</span></span>



| <span data-ttu-id="88cac-111">需求</span><span class="sxs-lookup"><span data-stu-id="88cac-111">Requirement</span></span> | <span data-ttu-id="88cac-112">值</span><span class="sxs-lookup"><span data-stu-id="88cac-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88cac-113">標頭</span><span class="sxs-lookup"><span data-stu-id="88cac-113">Header</span></span><br/>  | <dl> <span data-ttu-id="88cac-114"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="88cac-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88cac-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="88cac-115">Library</span></span><br/> | <dl> <span data-ttu-id="88cac-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="88cac-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88cac-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88cac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cac-118">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="88cac-118">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




