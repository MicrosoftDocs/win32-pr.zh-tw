---
description: SetControlWindowPin 方法會設定要與之同步處理的 pin。
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: 'CBaseControlWindow. SetControlWindowPin 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976267"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a><span data-ttu-id="08c79-103">CBaseControlWindow. SetControlWindowPin 方法</span><span class="sxs-lookup"><span data-stu-id="08c79-103">CBaseControlWindow.SetControlWindowPin method</span></span>

<span data-ttu-id="08c79-104">`SetControlWindowPin`方法會設定要與之同步處理的 pin。</span><span class="sxs-lookup"><span data-stu-id="08c79-104">The `SetControlWindowPin` method sets the pin with which to synchronize.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c79-105">語法</span><span class="sxs-lookup"><span data-stu-id="08c79-105">Syntax</span></span>


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="08c79-106">參數</span><span class="sxs-lookup"><span data-stu-id="08c79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c79-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="08c79-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="08c79-108">用來同步處理介面之 pin 的指標。</span><span class="sxs-lookup"><span data-stu-id="08c79-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c79-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="08c79-109">Return value</span></span>

<span data-ttu-id="08c79-110">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="08c79-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08c79-111">備註</span><span class="sxs-lookup"><span data-stu-id="08c79-111">Remarks</span></span>

<span data-ttu-id="08c79-112">此成員函式會將 m \_ pPin 成員變數設定為等於 pPin 參數。</span><span class="sxs-lookup"><span data-stu-id="08c79-112">This member function sets the m\_pPin member variable equal to the pPin parameter.</span></span> <span data-ttu-id="08c79-113">如同在函式中所述，只有在已成功連接篩選器時，才能呼叫介面。</span><span class="sxs-lookup"><span data-stu-id="08c79-113">As described in the constructor, the interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="08c79-114">物件會透過這個成員函式傳遞給它應該同步處理的 pin;在大部分的情況下，它會判斷 pin 是否在有介面方法的情況下連線，並會在失敗時傳回 VFW \_ E \_ 未 \_ 連接。</span><span class="sxs-lookup"><span data-stu-id="08c79-114">The object is passed in through this member function to the pin with which it should synchronize; in most cases, it will determine if the pin is connected whenever it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="08c79-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="08c79-115">Requirements</span></span>



| <span data-ttu-id="08c79-116">需求</span><span class="sxs-lookup"><span data-stu-id="08c79-116">Requirement</span></span> | <span data-ttu-id="08c79-117">值</span><span class="sxs-lookup"><span data-stu-id="08c79-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08c79-118">標頭</span><span class="sxs-lookup"><span data-stu-id="08c79-118">Header</span></span><br/>  | <dl> <span data-ttu-id="08c79-119"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="08c79-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08c79-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="08c79-120">Library</span></span><br/> | <dl> <span data-ttu-id="08c79-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="08c79-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c79-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08c79-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c79-123">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="08c79-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




