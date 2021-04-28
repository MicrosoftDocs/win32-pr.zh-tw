---
description: CBasePropertyPage。 CBasePropertyPage 函式-函數方法。
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
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119946"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="f08a6-103">CBasePropertyPage. CBasePropertyPage 函數</span><span class="sxs-lookup"><span data-stu-id="f08a6-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="f08a6-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="f08a6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f08a6-105">語法</span><span class="sxs-lookup"><span data-stu-id="f08a6-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="f08a6-106">參數</span><span class="sxs-lookup"><span data-stu-id="f08a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f08a6-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f08a6-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f08a6-108">字串，包含物件的名稱，用於進行調試。</span><span class="sxs-lookup"><span data-stu-id="f08a6-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="f08a6-109">如需詳細資訊，請參閱 [**CBaseObject：： CBaseObject**](cbaseobject-cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="f08a6-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f08a6-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="f08a6-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f08a6-111">匯總 **IUnknown** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f08a6-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="f08a6-112">*DialogId*</span><span class="sxs-lookup"><span data-stu-id="f08a6-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="f08a6-113">對話方塊的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f08a6-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="f08a6-114">*TitleId*</span><span class="sxs-lookup"><span data-stu-id="f08a6-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="f08a6-115">包含對話方塊標題之字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f08a6-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f08a6-116">範例</span><span class="sxs-lookup"><span data-stu-id="f08a6-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="f08a6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f08a6-117">Requirements</span></span>



| <span data-ttu-id="f08a6-118">需求</span><span class="sxs-lookup"><span data-stu-id="f08a6-118">Requirement</span></span> | <span data-ttu-id="f08a6-119">值</span><span class="sxs-lookup"><span data-stu-id="f08a6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08a6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f08a6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f08a6-121"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f08a6-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f08a6-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="f08a6-122">Library</span></span><br/> | <dl> <span data-ttu-id="f08a6-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f08a6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f08a6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f08a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08a6-125">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="f08a6-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




