---
description: Help 方法會叫用屬性頁說明。 這個方法會實 IPropertyPage：： Help 方法。
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: 'CBasePropertyPage： Help 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999376"
---
# <a name="cbasepropertypagehelp-method"></a><span data-ttu-id="f820d-104">CBasePropertyPage. Help 方法</span><span class="sxs-lookup"><span data-stu-id="f820d-104">CBasePropertyPage.Help method</span></span>

<span data-ttu-id="f820d-105">方法會叫用 `Help` 屬性頁說明。</span><span class="sxs-lookup"><span data-stu-id="f820d-105">The `Help` method invokes the property page help.</span></span> <span data-ttu-id="f820d-106">這個方法會實 **IPropertyPage：： Help** 方法。</span><span class="sxs-lookup"><span data-stu-id="f820d-106">This method implements the **IPropertyPage::Help** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f820d-107">語法</span><span class="sxs-lookup"><span data-stu-id="f820d-107">Syntax</span></span>


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a><span data-ttu-id="f820d-108">參數</span><span class="sxs-lookup"><span data-stu-id="f820d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f820d-109">*lpszHelpDir*</span><span class="sxs-lookup"><span data-stu-id="f820d-109">*lpszHelpDir*</span></span> 
</dt> <dd>

<span data-ttu-id="f820d-110">在登錄中屬性頁的 CLSID 資訊中， **HelpDir** 索引鍵下之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="f820d-110">Pointer to the string under the **HelpDir** key in the property page's CLSID information in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f820d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f820d-111">Return value</span></span>

<span data-ttu-id="f820d-112">傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="f820d-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f820d-113">備註</span><span class="sxs-lookup"><span data-stu-id="f820d-113">Remarks</span></span>

<span data-ttu-id="f820d-114">在基類中，方法一律會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="f820d-114">In the base class, the method always returns E\_NOTIMPL.</span></span> <span data-ttu-id="f820d-115">當方法失敗時，框架會呼叫 **IPropertyPage：： GetPageInfo** 來取得說明檔和內容識別碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="f820d-115">When the method fails, the frame calls **IPropertyPage::GetPageInfo** to get the name of the help file and context identifier.</span></span> <span data-ttu-id="f820d-116">根據預設，這些都是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f820d-116">By default, these are **NULL**.</span></span> <span data-ttu-id="f820d-117">為了提供協助，衍生類別可以覆寫 `Help` 方法或 [**CBasePropertyPage：： GetPageInfo**](cbasepropertypage-getpageinfo.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f820d-117">To provide help, therefore, the derived class can override either the `Help` method or the [**CBasePropertyPage::GetPageInfo**](cbasepropertypage-getpageinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f820d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f820d-118">Requirements</span></span>



| <span data-ttu-id="f820d-119">需求</span><span class="sxs-lookup"><span data-stu-id="f820d-119">Requirement</span></span> | <span data-ttu-id="f820d-120">值</span><span class="sxs-lookup"><span data-stu-id="f820d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f820d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f820d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f820d-122"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f820d-122"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f820d-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f820d-123">Library</span></span><br/> | <dl> <span data-ttu-id="f820d-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f820d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f820d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f820d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f820d-126">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="f820d-126">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




