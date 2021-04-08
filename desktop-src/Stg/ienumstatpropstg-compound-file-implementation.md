---
title: IEnumSTATPROPSTG-Compound 檔案的執行
description: IEnumSTATPROPSTG 介面的複合檔案實作為用來列舉屬性（property），這會產生包含統計屬性資料的 STATPROPSTG 結構。
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933513"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a><span data-ttu-id="c7e71-104">IEnumSTATPROPSTG-Compound 檔案的執行</span><span class="sxs-lookup"><span data-stu-id="c7e71-104">IEnumSTATPROPSTG-Compound File Implementation</span></span>

<span data-ttu-id="c7e71-105">[**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)介面的複合檔案實作為用來列舉屬性（property），這會產生包含統計屬性資料的 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)結構。</span><span class="sxs-lookup"><span data-stu-id="c7e71-105">The compound file implementation of the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) interface is used to enumerate properties, resulting in [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures, which contain statistical property data.</span></span> <span data-ttu-id="c7e71-106">[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)的執行會管理統計資料，並與目前的複合檔案儲存物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="c7e71-106">The implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) manages the statistical data and is associated with a current compound file storage object.</span></span>

<span data-ttu-id="c7e71-107">[**IENUMSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) COM 的函式中的函式會建立一個類別，該類別會讀取整個屬性集，並建立可在呼叫 **IEnumSTATPROPSTG：： Clone** 時共用的靜態陣列。</span><span class="sxs-lookup"><span data-stu-id="c7e71-107">The constructor in the COM implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) creates a class that reads the entire property set, and creates a static array which can be shared when **IEnumSTATPROPSTG::Clone** is called.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c7e71-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="c7e71-108">When to Use</span></span>

<span data-ttu-id="c7e71-109">呼叫 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 的複合檔案執行，以列舉 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 結構，其中包含目前屬性集內屬性的相關資料。</span><span class="sxs-lookup"><span data-stu-id="c7e71-109">Call the compound file implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that contain data about the properties within the current property set.</span></span> <span data-ttu-id="c7e71-110">使用屬性儲存介面的複合檔案執行時，請呼叫 [**IPropertyStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) 來傳回 **IEnumSTATPROPSTG** 的指標，以管理屬性儲存物件和其中的元素。</span><span class="sxs-lookup"><span data-stu-id="c7e71-110">When using the compound file implementation of the property storage interfaces, call [**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) to return a pointer to **IEnumSTATPROPSTG** to manage the property storage object and the elements within it.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e71-111">備註</span><span class="sxs-lookup"><span data-stu-id="c7e71-111">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="c7e71-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="c7e71-112"><span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="c7e71-113">取得下一個或多個 [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 結構 (*celt* 參數指定的數位) 。</span><span class="sxs-lookup"><span data-stu-id="c7e71-113">Gets the next one or more [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures (the number is specified by the *celt* parameter).</span></span> <span data-ttu-id="c7e71-114">\_如果成功，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="c7e71-114">Returns S\_OK if successful.</span></span>

</dd> <dt>

<span data-ttu-id="c7e71-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG：： Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="c7e71-115"><span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="c7e71-116">略過 *celt* 中指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c7e71-116">Skips the number of elements specified in *celt*.</span></span> <span data-ttu-id="c7e71-117">接下來要透過呼叫來列舉的下一個專案，會成為略過專案之後的元素。</span><span class="sxs-lookup"><span data-stu-id="c7e71-117">The next element to be enumerated through a call to Next then becomes the element after the skipped elements.</span></span> <span data-ttu-id="c7e71-118">\_如果略過 *celt* 元素，則傳回 s OK; \_ 如果略過小於 *celt* 的元素，則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="c7e71-118">Returns S\_OK if *celt* elements were skipped; returns S\_FALSE if fewer than *celt* elements were skipped.</span></span>

</dd> <dt>

<span data-ttu-id="c7e71-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG：： Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="c7e71-119"><span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="c7e71-120">將資料指標設為列舉的開頭。</span><span class="sxs-lookup"><span data-stu-id="c7e71-120">Sets the cursor to the beginning of the enumeration.</span></span> <span data-ttu-id="c7e71-121">如果成功，則傳回 S \_ OK，否則會傳回 Stg. \_ E \_ INVALIDHANDLE。</span><span class="sxs-lookup"><span data-stu-id="c7e71-121">If successful, returns S\_OK, otherwise, returns STG\_E\_INVALIDHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="c7e71-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG：： Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="c7e71-122"><span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="c7e71-123">使用 [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 的函式來建立陣列的複本。</span><span class="sxs-lookup"><span data-stu-id="c7e71-123">Uses the constructor for the [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) to create a copy of the array.</span></span> <span data-ttu-id="c7e71-124">由於構成靜態陣列的類別實際上包含物件，因此這個函式主要會加入至參考計數。</span><span class="sxs-lookup"><span data-stu-id="c7e71-124">Because the class that constructs the static array actually contains the object, this function mainly adds to the reference count.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c7e71-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7e71-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7e71-126">**STATPROPSTG**</span><span class="sxs-lookup"><span data-stu-id="c7e71-126">**STATPROPSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[<span data-ttu-id="c7e71-127">**IPropertyStorage：： Enum**</span><span class="sxs-lookup"><span data-stu-id="c7e71-127">**IPropertyStorage::Enum**</span></span>](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 