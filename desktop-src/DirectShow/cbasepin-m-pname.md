---
description: Pin 名稱。
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'CBasePin：： m_pName 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996012"
---
# <a name="cbasepinm_pname-member"></a><span data-ttu-id="d6032-103">CBasePin：： m \_ pName 成員</span><span class="sxs-lookup"><span data-stu-id="d6032-103">CBasePin::m\_pName member</span></span>

<span data-ttu-id="d6032-104">Pin 名稱。</span><span class="sxs-lookup"><span data-stu-id="d6032-104">Pin name.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6032-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6032-105">Syntax</span></span>


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a><span data-ttu-id="d6032-106">備註</span><span class="sxs-lookup"><span data-stu-id="d6032-106">Remarks</span></span>

<span data-ttu-id="d6032-107">[**CBasePin：： QueryPinInfo**](cbasepin-querypininfo.md)方法會將此字串傳回為 pin 名稱，而 [**CBasePin：： QueryId**](cbasepin-queryid.md)方法會將其傳回做為 pin 識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6032-107">The [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) method returns this string as the pin name, and the [**CBasePin::QueryId**](cbasepin-queryid.md) method returns it as the pin identifier.</span></span> <span data-ttu-id="d6032-108">但一般而言，pin 名稱和 pin 識別碼不需要相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6032-108">In general, however, the pin name and the pin identifier are not required to be the same.</span></span> <span data-ttu-id="d6032-109">Pin 識別碼會用於圖形持續性。</span><span class="sxs-lookup"><span data-stu-id="d6032-109">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="d6032-110">如需詳細資訊，請參閱 [**IBaseFilter：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)。</span><span class="sxs-lookup"><span data-stu-id="d6032-110">For more information, see [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6032-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6032-111">Requirements</span></span>



| <span data-ttu-id="d6032-112">需求</span><span class="sxs-lookup"><span data-stu-id="d6032-112">Requirement</span></span> | <span data-ttu-id="d6032-113">值</span><span class="sxs-lookup"><span data-stu-id="d6032-113">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6032-114">標頭</span><span class="sxs-lookup"><span data-stu-id="d6032-114">Header</span></span><br/> | <dl> <span data-ttu-id="d6032-115"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d6032-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6032-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6032-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6032-117">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="d6032-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




