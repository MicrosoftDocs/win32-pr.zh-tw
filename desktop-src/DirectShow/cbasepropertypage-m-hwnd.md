---
description: M \_ hwnd 成員變數包含交談視窗的控制碼。 當 CreateDialogParam 函式傳回時，這個成員變數就會在物件建立對話方塊視窗之後初始化。
ms.assetid: f985c06f-a1f9-458b-b9f3-cabe9f583313
title: 'CBasePropertyPage：： m_hwnd 成員 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hwnd
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a249d9b8f887750360ceb83f876f315d4fd43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999214"
---
# <a name="cbasepropertypagem_hwnd-member"></a><span data-ttu-id="4ea82-104">CBasePropertyPage：： m \_ hwnd 成員</span><span class="sxs-lookup"><span data-stu-id="4ea82-104">CBasePropertyPage::m\_hwnd member</span></span>

<span data-ttu-id="4ea82-105">`m_hwnd`成員變數包含交談視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4ea82-105">The `m_hwnd` member variable contains a handle to the dialog window.</span></span> <span data-ttu-id="4ea82-106">當 **CreateDialogParam** 函式傳回時，這個成員變數就會在物件建立對話方塊視窗之後初始化。</span><span class="sxs-lookup"><span data-stu-id="4ea82-106">This member variable is initialized after the object creates the dialog window, when the **CreateDialogParam** function returns.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea82-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ea82-107">Syntax</span></span>


```C++
HWND m_hwnd;
```



## <a name="requirements"></a><span data-ttu-id="4ea82-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ea82-108">Requirements</span></span>



| <span data-ttu-id="4ea82-109">需求</span><span class="sxs-lookup"><span data-stu-id="4ea82-109">Requirement</span></span> | <span data-ttu-id="4ea82-110">值</span><span class="sxs-lookup"><span data-stu-id="4ea82-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea82-111">標頭</span><span class="sxs-lookup"><span data-stu-id="4ea82-111">Header</span></span><br/>  | <dl> <span data-ttu-id="4ea82-112"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4ea82-112"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="4ea82-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ea82-113">Library</span></span><br/> | <dl> <span data-ttu-id="4ea82-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4ea82-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea82-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ea82-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea82-116">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="4ea82-116">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




