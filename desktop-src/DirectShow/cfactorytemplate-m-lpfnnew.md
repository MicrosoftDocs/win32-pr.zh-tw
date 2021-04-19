---
description: 函數的指標，該函式會建立物件的實例。
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'CFactoryTemplate：： m_lpfnNew 成員 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994361"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="09f8b-103">CFactoryTemplate：： m \_ lpfnNew 成員</span><span class="sxs-lookup"><span data-stu-id="09f8b-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="09f8b-104">函數的指標，該函式會建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="09f8b-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f8b-105">語法</span><span class="sxs-lookup"><span data-stu-id="09f8b-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="09f8b-106">備註</span><span class="sxs-lookup"><span data-stu-id="09f8b-106">Remarks</span></span>

<span data-ttu-id="09f8b-107">在您的 DLL 中，宣告會傳回物件新實例指標的靜態函式。</span><span class="sxs-lookup"><span data-stu-id="09f8b-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="09f8b-108">在 factory 範本中，將 **m \_ lpfnNew** 成員變數設定為這個靜態函式的位址。</span><span class="sxs-lookup"><span data-stu-id="09f8b-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="09f8b-109">函數指標型別為 [**LPFNNewCOMObject**](lpfnnewcomobject.md)。</span><span class="sxs-lookup"><span data-stu-id="09f8b-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="09f8b-110">下列範例顯示 **m \_ lpfnNew** 的一般函數：</span><span class="sxs-lookup"><span data-stu-id="09f8b-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a><span data-ttu-id="09f8b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="09f8b-111">Requirements</span></span>



| <span data-ttu-id="09f8b-112">需求</span><span class="sxs-lookup"><span data-stu-id="09f8b-112">Requirement</span></span> | <span data-ttu-id="09f8b-113">值</span><span class="sxs-lookup"><span data-stu-id="09f8b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09f8b-114">標頭</span><span class="sxs-lookup"><span data-stu-id="09f8b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="09f8b-115"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="09f8b-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09f8b-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="09f8b-116">Library</span></span><br/> | <dl> <span data-ttu-id="09f8b-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="09f8b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09f8b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09f8b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f8b-119">**CFactoryTemplate 類別**</span><span class="sxs-lookup"><span data-stu-id="09f8b-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




