---
description: TranslateAccelerator 方法會指示屬性頁處理按鍵。 這個方法會實 IPropertyPage：： TranslateAccelerator 方法。
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: 'CBasePropertyPage. TranslateAccelerator 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986795"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a><span data-ttu-id="7b829-104">CBasePropertyPage. TranslateAccelerator 方法</span><span class="sxs-lookup"><span data-stu-id="7b829-104">CBasePropertyPage.TranslateAccelerator method</span></span>

<span data-ttu-id="7b829-105">`TranslateAccelerator`方法會指示屬性頁處理按鍵。</span><span class="sxs-lookup"><span data-stu-id="7b829-105">The `TranslateAccelerator` method instructs the property page to process a keystroke.</span></span> <span data-ttu-id="7b829-106">這個方法會實 **IPropertyPage：： TranslateAccelerator** 方法。</span><span class="sxs-lookup"><span data-stu-id="7b829-106">This method implements the **IPropertyPage::TranslateAccelerator** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b829-107">語法</span><span class="sxs-lookup"><span data-stu-id="7b829-107">Syntax</span></span>


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a><span data-ttu-id="7b829-108">參數</span><span class="sxs-lookup"><span data-stu-id="7b829-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b829-109">*lpMsg*</span><span class="sxs-lookup"><span data-stu-id="7b829-109">*lpMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="7b829-110">訊息 **結構的** 指標，描述要處理的按鍵。</span><span class="sxs-lookup"><span data-stu-id="7b829-110">Pointer to a **MSG** structure describing the keystroke to process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b829-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b829-111">Return value</span></span>

<span data-ttu-id="7b829-112">傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="7b829-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b829-113">備註</span><span class="sxs-lookup"><span data-stu-id="7b829-113">Remarks</span></span>

<span data-ttu-id="7b829-114">如果您想要提供屬性頁的鍵盤快速鍵，請覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7b829-114">Override this method if you want to provide keyboard accelerators for the property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b829-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b829-115">Requirements</span></span>



| <span data-ttu-id="7b829-116">需求</span><span class="sxs-lookup"><span data-stu-id="7b829-116">Requirement</span></span> | <span data-ttu-id="7b829-117">值</span><span class="sxs-lookup"><span data-stu-id="7b829-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b829-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7b829-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7b829-119"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7b829-119"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="7b829-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="7b829-120">Library</span></span><br/> | <dl> <span data-ttu-id="7b829-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7b829-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b829-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b829-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b829-123">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="7b829-123">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




