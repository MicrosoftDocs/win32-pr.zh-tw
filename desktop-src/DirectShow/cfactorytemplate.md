---
description: 提供用來建立 class factory 的範本。
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: 'CFactoryTemplate 類別 (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000866"
---
# <a name="cfactorytemplate-class"></a><span data-ttu-id="b07fe-103">CFactoryTemplate 類別</span><span class="sxs-lookup"><span data-stu-id="b07fe-103">CFactoryTemplate class</span></span>

<span data-ttu-id="b07fe-104">提供用來建立 class factory 的範本。</span><span class="sxs-lookup"><span data-stu-id="b07fe-104">Provides a template for creating class factories.</span></span>

<span data-ttu-id="b07fe-105">在 DirectShow 中，會使用 **CFactoryTemplate** 類別（也稱為 *factory 範本*）來特製化類別 factory。</span><span class="sxs-lookup"><span data-stu-id="b07fe-105">In DirectShow, class factories are specialized using the **CFactoryTemplate** class, also called the *factory template*.</span></span> <span data-ttu-id="b07fe-106">每個 class factory 都會保留一個指向 factory 範本的指標。</span><span class="sxs-lookup"><span data-stu-id="b07fe-106">Each class factory holds a pointer to a factory template.</span></span> <span data-ttu-id="b07fe-107">Factory 範本包含 COM 物件的相關資訊，包括物件的類別識別碼 (CLSID) 和函式的指標，該函式會建立物件。</span><span class="sxs-lookup"><span data-stu-id="b07fe-107">The factory template contains information about a COM object, including the object's class identifier (CLSID) and a pointer to a function that creates the object.</span></span>

<span data-ttu-id="b07fe-108">在您的 DLL 中，宣告名為 *g \_ templates* 的原廠範本的全域陣列。</span><span class="sxs-lookup"><span data-stu-id="b07fe-108">In your DLL, declare a global array of factory templates named *g\_Templates*.</span></span> <span data-ttu-id="b07fe-109">針對 DLL 中的每個物件，各包含一個 factory 範本。</span><span class="sxs-lookup"><span data-stu-id="b07fe-109">Include one factory template for each object in the DLL.</span></span> <span data-ttu-id="b07fe-110">當 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式建立新的 class factory 時，它會在陣列中搜尋具有相符 CLSID 的範本。</span><span class="sxs-lookup"><span data-stu-id="b07fe-110">When the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function makes a new class factory, it searches the array for a template with a matching CLSID.</span></span> <span data-ttu-id="b07fe-111">假設找到一個，它會建立一個持有相符範本指標的 class factory。</span><span class="sxs-lookup"><span data-stu-id="b07fe-111">Assuming it finds one, it creates a class factory that holds a pointer to the matching template.</span></span> <span data-ttu-id="b07fe-112">當用戶端呼叫 **IClassFactory：： CreateInstance** 時，class factory 會呼叫範本中定義的具現化函數。</span><span class="sxs-lookup"><span data-stu-id="b07fe-112">When the client calls **IClassFactory::CreateInstance**, the class factory calls the instantiation function defined in the template.</span></span>

<span data-ttu-id="b07fe-113">如需詳細資訊，請參閱 [如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="b07fe-113">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>



| <span data-ttu-id="b07fe-114">Public 成員變數</span><span class="sxs-lookup"><span data-stu-id="b07fe-114">Public Member Variables</span></span>                                                   | <span data-ttu-id="b07fe-115">Description</span><span class="sxs-lookup"><span data-stu-id="b07fe-115">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="b07fe-116">**m \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="b07fe-116">**m\_Name**</span></span>](cfactorytemplate-m-name.md)                                | <span data-ttu-id="b07fe-117">篩選的名稱。</span><span class="sxs-lookup"><span data-stu-id="b07fe-117">Name of the filter.</span></span>                                                        |
| [<span data-ttu-id="b07fe-118">**m \_ ClsID**</span><span class="sxs-lookup"><span data-stu-id="b07fe-118">**m\_ClsID**</span></span>](cfactorytemplate-m-clsid.md)                              | <span data-ttu-id="b07fe-119">物件之 CLSID 的指標。</span><span class="sxs-lookup"><span data-stu-id="b07fe-119">Pointer to the CLSID of the object.</span></span>                                        |
| [<span data-ttu-id="b07fe-120">**m \_ lpfnNew**</span><span class="sxs-lookup"><span data-stu-id="b07fe-120">**m\_lpfnNew**</span></span>](cfactorytemplate-m-lpfnnew.md)                          | <span data-ttu-id="b07fe-121">函數的指標，該函式會建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="b07fe-121">Pointer to a function that creates an instance of the object.</span></span>              |
| [<span data-ttu-id="b07fe-122">**m \_ lpfnInit**</span><span class="sxs-lookup"><span data-stu-id="b07fe-122">**m\_lpfnInit**</span></span>](cfactorytemplate-m-lpfninit.md)                        | <span data-ttu-id="b07fe-123">從 DLL 進入點呼叫之函式的指標。</span><span class="sxs-lookup"><span data-stu-id="b07fe-123">Pointer to a function that gets called from the DLL entry point.</span></span>           |
| [<span data-ttu-id="b07fe-124">**m \_ pAMovieSetup \_ 篩選**</span><span class="sxs-lookup"><span data-stu-id="b07fe-124">**m\_pAMovieSetup\_Filter**</span></span>](cfactorytemplate-m-pamoviesetup-filter.md) | <span data-ttu-id="b07fe-125">[**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b07fe-125">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span> |
| <span data-ttu-id="b07fe-126">公用方法</span><span class="sxs-lookup"><span data-stu-id="b07fe-126">Public Methods</span></span>                                                            | <span data-ttu-id="b07fe-127">Description</span><span class="sxs-lookup"><span data-stu-id="b07fe-127">Description</span></span>                                                                |
| [<span data-ttu-id="b07fe-128">**IsClassID**</span><span class="sxs-lookup"><span data-stu-id="b07fe-128">**IsClassID**</span></span>](cfactorytemplate-isclassid.md)                           | <span data-ttu-id="b07fe-129">判斷 CLSID 是否符合這個類別範本。</span><span class="sxs-lookup"><span data-stu-id="b07fe-129">Determines whether a CLSID matches this class template.</span></span>                    |
| [<span data-ttu-id="b07fe-130">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="b07fe-130">**CreateInstance**</span></span>](cfactorytemplate-createinstance.md)                 | <span data-ttu-id="b07fe-131">呼叫類別的物件建立函數。</span><span class="sxs-lookup"><span data-stu-id="b07fe-131">Calls the object-creation function for the class.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="b07fe-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b07fe-132">Requirements</span></span>



| <span data-ttu-id="b07fe-133">需求</span><span class="sxs-lookup"><span data-stu-id="b07fe-133">Requirement</span></span> | <span data-ttu-id="b07fe-134">值</span><span class="sxs-lookup"><span data-stu-id="b07fe-134">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b07fe-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b07fe-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b07fe-136"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b07fe-136"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b07fe-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="b07fe-137">Library</span></span><br/> | <dl> <span data-ttu-id="b07fe-138"><dt>Strmbase .lib;</dt><dt>Strmbasd .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b07fe-138"><dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b07fe-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b07fe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b07fe-140">基類參考</span><span class="sxs-lookup"><span data-stu-id="b07fe-140">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

