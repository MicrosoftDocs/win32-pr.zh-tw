---
description: 移動方法會放置並調整對話方塊的大小。 這個方法會實 IPropertyPage：： Move 方法。
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: 'CBasePropertyPage： Move 方法 (Cprop. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987178"
---
# <a name="cbasepropertypagemove-method"></a><span data-ttu-id="908d0-104">CBasePropertyPage. Move 方法</span><span class="sxs-lookup"><span data-stu-id="908d0-104">CBasePropertyPage.Move method</span></span>

<span data-ttu-id="908d0-105">`Move`方法會放置並調整對話方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="908d0-105">The `Move` method positions and resizes the dialog box.</span></span> <span data-ttu-id="908d0-106">這個方法會實 **IPropertyPage：： Move** 方法。</span><span class="sxs-lookup"><span data-stu-id="908d0-106">This method implements the **IPropertyPage::Move** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="908d0-107">語法</span><span class="sxs-lookup"><span data-stu-id="908d0-107">Syntax</span></span>


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a><span data-ttu-id="908d0-108">參數</span><span class="sxs-lookup"><span data-stu-id="908d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="908d0-109">*prect*</span><span class="sxs-lookup"><span data-stu-id="908d0-109">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="908d0-110">**矩形** 結構的指標，其中包含位置資訊。</span><span class="sxs-lookup"><span data-stu-id="908d0-110">Pointer to a **RECT** structure containing the positioning information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="908d0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="908d0-111">Return value</span></span>

<span data-ttu-id="908d0-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="908d0-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="908d0-113">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="908d0-113">Possible values include the following.</span></span>



| <span data-ttu-id="908d0-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="908d0-114">Return code</span></span>                                                                                  | <span data-ttu-id="908d0-115">Description</span><span class="sxs-lookup"><span data-stu-id="908d0-115">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="908d0-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="908d0-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="908d0-117">成功。</span><span class="sxs-lookup"><span data-stu-id="908d0-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="908d0-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="908d0-118"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="908d0-119">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="908d0-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="908d0-120"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="908d0-120"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="908d0-121">發生非預期的失敗。</span><span class="sxs-lookup"><span data-stu-id="908d0-121">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="908d0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="908d0-122">Requirements</span></span>



| <span data-ttu-id="908d0-123">需求</span><span class="sxs-lookup"><span data-stu-id="908d0-123">Requirement</span></span> | <span data-ttu-id="908d0-124">值</span><span class="sxs-lookup"><span data-stu-id="908d0-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="908d0-125">標頭</span><span class="sxs-lookup"><span data-stu-id="908d0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="908d0-126"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="908d0-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="908d0-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="908d0-127">Library</span></span><br/> | <dl> <span data-ttu-id="908d0-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="908d0-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="908d0-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="908d0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908d0-130">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="908d0-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




