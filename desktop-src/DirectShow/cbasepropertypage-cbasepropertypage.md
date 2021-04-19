---
description: 函式方法。
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: 'CBasePropertyPage. CBasePropertyPage (Cprop. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 915bc42cfb7f152cc061dab76caede6c998edf8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994580"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="62908-103">CBasePropertyPage. CBasePropertyPage 函數</span><span class="sxs-lookup"><span data-stu-id="62908-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="62908-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="62908-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62908-105">語法</span><span class="sxs-lookup"><span data-stu-id="62908-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="62908-106">參數</span><span class="sxs-lookup"><span data-stu-id="62908-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62908-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="62908-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="62908-108">字串，包含物件的名稱，用於進行調試。</span><span class="sxs-lookup"><span data-stu-id="62908-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="62908-109">如需詳細資訊，請參閱 [**CBaseObject：： CBaseObject**](cbaseobject-cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="62908-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="62908-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="62908-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="62908-111">匯總 **IUnknown** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="62908-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="62908-112">*DialogId*</span><span class="sxs-lookup"><span data-stu-id="62908-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="62908-113">對話方塊的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="62908-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="62908-114">*TitleId*</span><span class="sxs-lookup"><span data-stu-id="62908-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="62908-115">包含對話方塊標題之字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="62908-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="62908-116">範例</span><span class="sxs-lookup"><span data-stu-id="62908-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="62908-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="62908-117">Requirements</span></span>



| <span data-ttu-id="62908-118">需求</span><span class="sxs-lookup"><span data-stu-id="62908-118">Requirement</span></span> | <span data-ttu-id="62908-119">值</span><span class="sxs-lookup"><span data-stu-id="62908-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62908-120">標頭</span><span class="sxs-lookup"><span data-stu-id="62908-120">Header</span></span><br/>  | <dl> <span data-ttu-id="62908-121"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="62908-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="62908-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="62908-122">Library</span></span><br/> | <dl> <span data-ttu-id="62908-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="62908-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62908-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62908-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62908-125">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="62908-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




