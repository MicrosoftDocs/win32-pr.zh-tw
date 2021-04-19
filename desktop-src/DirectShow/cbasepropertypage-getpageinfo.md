---
description: GetPageInfo 方法會抓取屬性頁的相關資訊。 這個方法會實 IPropertyPage：： GetPageInfo 方法。
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: 'CBasePropertyPage. GetPageInfo 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995388"
---
# <a name="cbasepropertypagegetpageinfo-method"></a><span data-ttu-id="6563f-104">CBasePropertyPage. GetPageInfo 方法</span><span class="sxs-lookup"><span data-stu-id="6563f-104">CBasePropertyPage.GetPageInfo method</span></span>

<span data-ttu-id="6563f-105">方法會抓取 `GetPageInfo` 屬性頁的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6563f-105">The `GetPageInfo` method retrieves information about the property page.</span></span> <span data-ttu-id="6563f-106">這個方法會實 **IPropertyPage：： GetPageInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="6563f-106">This method implements the **IPropertyPage::GetPageInfo** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6563f-107">語法</span><span class="sxs-lookup"><span data-stu-id="6563f-107">Syntax</span></span>


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6563f-108">參數</span><span class="sxs-lookup"><span data-stu-id="6563f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6563f-109">*pPageInfo*</span><span class="sxs-lookup"><span data-stu-id="6563f-109">*pPageInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6563f-110">呼叫端配置之 **PROPPAGEINFO** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6563f-110">Pointer to a caller-allocated **PROPPAGEINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6563f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6563f-111">Return value</span></span>

<span data-ttu-id="6563f-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6563f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6563f-113">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="6563f-113">Possible values include the following.</span></span>



| <span data-ttu-id="6563f-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6563f-114">Return code</span></span>                                                                                   | <span data-ttu-id="6563f-115">Description</span><span class="sxs-lookup"><span data-stu-id="6563f-115">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="6563f-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6563f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6563f-117">成功。</span><span class="sxs-lookup"><span data-stu-id="6563f-117">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="6563f-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6563f-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6563f-119">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="6563f-119">Insufficient memory.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6563f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6563f-120">Requirements</span></span>



| <span data-ttu-id="6563f-121">需求</span><span class="sxs-lookup"><span data-stu-id="6563f-121">Requirement</span></span> | <span data-ttu-id="6563f-122">值</span><span class="sxs-lookup"><span data-stu-id="6563f-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6563f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6563f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6563f-124"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6563f-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6563f-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6563f-125">Library</span></span><br/> | <dl> <span data-ttu-id="6563f-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6563f-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6563f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6563f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6563f-128">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="6563f-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




