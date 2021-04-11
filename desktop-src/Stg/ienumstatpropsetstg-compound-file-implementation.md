---
title: IEnumSTATPROPSETSTG-Compound 檔案的執行
description: IEnumSTATPROPSETSTG 介面的複合檔案實作為列舉包含統計屬性資料之 STATPROPSETSTG 結構的陣列。
ms.assetid: 1ce36e40-518c-411b-be5a-835a2dd0995e
keywords:
- IEnumSTATPROPSETSTG Strctd Stg.，複合檔案執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9566af1a1956b3a951a996b6198f4a3161680042
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315334"
---
# <a name="ienumstatpropsetstg-compound-file-implementation"></a><span data-ttu-id="dbc08-104">IEnumSTATPROPSETSTG-Compound 檔案的執行</span><span class="sxs-lookup"><span data-stu-id="dbc08-104">IEnumSTATPROPSETSTG-Compound File Implementation</span></span>

<span data-ttu-id="dbc08-105">[**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)介面的複合檔案實作為列舉包含統計屬性資料之 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="dbc08-105">The compound file implementation of the [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interface is used to enumerate an array of [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures that contain statistical property data.</span></span> <span data-ttu-id="dbc08-106">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)執行會管理統計資料，並與目前的複合檔案儲存物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="dbc08-106">The [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) implementation manages the statistical data and is associated with a current compound file storage object.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="dbc08-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="dbc08-107">When to Use</span></span>

<span data-ttu-id="dbc08-108">呼叫 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 的方法來列舉 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構，其中每一個都提供與複合檔案儲存物件相關聯的其中一個屬性集的相關資料。</span><span class="sxs-lookup"><span data-stu-id="dbc08-108">Call the methods of [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) to enumerate [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures, each of which provide data about one of the property sets associated with the compound file storage object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc08-109">備註</span><span class="sxs-lookup"><span data-stu-id="dbc08-109">Remarks</span></span>

<dl> <dt>

<span data-ttu-id="dbc08-110"><span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span><span class="sxs-lookup"><span data-stu-id="dbc08-110"><span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)</span></span>
</dt> <dd>

<span data-ttu-id="dbc08-111">取得下一個或多個 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構 (*celt* 參數指定的數位) 。</span><span class="sxs-lookup"><span data-stu-id="dbc08-111">Gets the next one or more [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures (the number is specified by the *celt* parameter).</span></span> <span data-ttu-id="dbc08-112">透過呼叫 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)的複合檔案執行所提供的 **STATPROPSETSTG** 元素，請遵循下列規則：</span><span class="sxs-lookup"><span data-stu-id="dbc08-112">The **STATPROPSETSTG** elements provided through a call to the compound file implementation of [**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) follow these rules:</span></span>

-   <span data-ttu-id="dbc08-113">如果 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 無法提供 STATPROPSETSTG. fmtid，則會將零寫入至該成員。</span><span class="sxs-lookup"><span data-stu-id="dbc08-113">If [**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) cannot provide STATPROPSETSTG.fmtid, zeros are written to that member.</span></span> <span data-ttu-id="dbc08-114">當屬性集沒有預先定義的名稱 (（例如 \\ 005SummaryInformation) ，而且不是合法值）時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="dbc08-114">This occurs when the property set does not have a predefined name (such as \\005SummaryInformation) and is not a legal value.</span></span>
-   <span data-ttu-id="dbc08-115">DocumentSummaryInformation 和使用者設定的屬性集是特殊的，因為它可能有兩個屬性集區段。</span><span class="sxs-lookup"><span data-stu-id="dbc08-115">The DocumentSummaryInformation and UserDefined property set is special, in that it may have two property set sections.</span></span> <span data-ttu-id="dbc08-116">這個屬性集的說明位於 [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md)一節中。</span><span class="sxs-lookup"><span data-stu-id="dbc08-116">This property set is described in the section [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).</span></span> <span data-ttu-id="dbc08-117">第二個區段稱為 User-Defined 屬性。</span><span class="sxs-lookup"><span data-stu-id="dbc08-117">The second section is referred to as the User-Defined Properties.</span></span> <span data-ttu-id="dbc08-118">每個區段都會以唯一的格式識別碼來識別 (FMTID) 。</span><span class="sxs-lookup"><span data-stu-id="dbc08-118">Each section is identified with a unique format identifier (FMTID).</span></span> <span data-ttu-id="dbc08-119">當使用 [**IPropertySetStorage：： Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) 來列舉屬性集時，將不會列舉 User-Defined 的屬性集。</span><span class="sxs-lookup"><span data-stu-id="dbc08-119">When [**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) is used to enumerate property sets, the User-Defined property set will not be enumerated.</span></span>

> [!Note]  
> <span data-ttu-id="dbc08-120">如果您一律使用 [**IPropertySetStorage：： create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)來建立屬性集，則因為系統會為儲存體名稱建立「字元 GUID」，所以 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 會傳回非零的有效 FMTID （property set \[ STATPROPSETSTG. FMTID） \] 。</span><span class="sxs-lookup"><span data-stu-id="dbc08-120">If you always create a property set using [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), then, because a "Character GUID" is created for the storage name, [**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) will return a nonzero, valid FMTID for the property set \[STATPROPSETSTG.fmtid\].</span></span>

 

-   <span data-ttu-id="dbc08-121">STATPROPSETSTG. grfFlags 成員不一定會反映屬性集是否為 ANSI。</span><span class="sxs-lookup"><span data-stu-id="dbc08-121">The STATPROPSETSTG.grfFlags member does not necessarily reflect whether the property set is ANSI or not.</span></span> <span data-ttu-id="dbc08-122">如果 \_ 已設定 PROPSETFLAG ANSI，則屬性集絕對是 ANSI。</span><span class="sxs-lookup"><span data-stu-id="dbc08-122">If PROPSETFLAG\_ANSI is set, the property set is definitely ANSI.</span></span> <span data-ttu-id="dbc08-123">如果 PROPSETFLAG \_ ANSI 很清楚，屬性集可以是 unicode 或非 unicode，因為無法判斷它是否為 ANSI 而不需要開啟。</span><span class="sxs-lookup"><span data-stu-id="dbc08-123">If PROPSETFLAG\_ANSI is clear, the property set could be either Unicode or non-Unicode, because it is not possible to tell whether it is ANSI without opening it.</span></span>
-   <span data-ttu-id="dbc08-124">STATPROPSETSTG. grfFlags 成員會反映屬性集是否為簡單的，因此 PROPSETFLAG 簡單旗標的設定 \_ 一律有效。</span><span class="sxs-lookup"><span data-stu-id="dbc08-124">The STATPROPSETSTG.grfFlags member does reflect whether the property set is simple or not, so the setting of the PROPSETFLAG\_NONSIMPLE flag is always valid.</span></span>
-   <span data-ttu-id="dbc08-125">如果 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) 無法提供 STATPROPSETSTG，則會將它設定為所有零 (clsid \_ Null) 。</span><span class="sxs-lookup"><span data-stu-id="dbc08-125">If [**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) cannot provide STATPROPSETSTG.clsid, it is set to all zeroes (CLSID\_NULL).</span></span> <span data-ttu-id="dbc08-126">在 COM 複合檔案執行中，當屬性集很簡單 (PROPSETFLAG 簡單旗標未 \_ 設定) 或簡單，但未明確設定 CLSID 時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="dbc08-126">In the COM compound file implementation, this occurs when the property set is simple (the PROPSETFLAG\_NONSIMPLE flag is not set), or is nonsimple, but the CLSID was not explicitly set.</span></span> <span data-ttu-id="dbc08-127">針對簡單屬性集，所接收的 CLSID 是基礎 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)所維護的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="dbc08-127">For nonsimple property sets, the CLSID that is received is the one that is maintained by the underlying [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).</span></span>
-   <span data-ttu-id="dbc08-128">如果 [**IEnumSTATPROPSETSTG：： Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)無法提供 \[ **ctime**、 **mtime**、 **atime** 的時間欄位 \] ，則每個不支援的時間將會設定為零。</span><span class="sxs-lookup"><span data-stu-id="dbc08-128">If [**IEnumSTATPROPSETSTG::Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) cannot provide the time fields \[**ctime**, **mtime**, **atime**\], each non-supported time will be set to zeroes.</span></span> <span data-ttu-id="dbc08-129">在 COM 複合檔案執行中，取得這些值取決於從基礎 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 執行中取得這些值。</span><span class="sxs-lookup"><span data-stu-id="dbc08-129">In the COM compound file implementation, getting these values depends on retrieving them from the underlying [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) implementation.</span></span>

</dd> <dt>

<span data-ttu-id="dbc08-130"><span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**IEnumSTATPROPSETSTG：： Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)</span><span class="sxs-lookup"><span data-stu-id="dbc08-130"><span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**IEnumSTATPROPSETSTG::Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)</span></span>
</dt> <dd>

<span data-ttu-id="dbc08-131">略過 *celt* 中指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="dbc08-131">Skips the number of elements specified in *celt*.</span></span> <span data-ttu-id="dbc08-132">\_如果略過指定的元素數目，則傳回 s OK， \_ 如果略過要求的元素數目較少，則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="dbc08-132">Returns S\_OK if the specified number of elements are skipped, returns S\_FALSE if fewer elements than requested are skipped.</span></span> <span data-ttu-id="dbc08-133">在其他任何情況下，都會傳回適當的錯誤。</span><span class="sxs-lookup"><span data-stu-id="dbc08-133">In any other case, returns the appropriate error.</span></span>

</dd> <dt>

<span data-ttu-id="dbc08-134"><span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**IEnumSTATPROPSETSTG：： Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)</span><span class="sxs-lookup"><span data-stu-id="dbc08-134"><span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**IEnumSTATPROPSETSTG::Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)</span></span>
</dt> <dd>

<span data-ttu-id="dbc08-135">將資料指標設為列舉的開頭。</span><span class="sxs-lookup"><span data-stu-id="dbc08-135">Sets the cursor to the beginning of the enumeration.</span></span> <span data-ttu-id="dbc08-136">如果成功，則傳回 S \_ OK，否則會傳回 Stg. \_ E \_ INVALIDHANDLE。</span><span class="sxs-lookup"><span data-stu-id="dbc08-136">If successful, returns S\_OK, otherwise, returns STG\_E\_INVALIDHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="dbc08-137"><span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**IEnumSTATPROPSETSTG：： Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)</span><span class="sxs-lookup"><span data-stu-id="dbc08-137"><span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**IEnumSTATPROPSETSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)</span></span>
</dt> <dd>

<span data-ttu-id="dbc08-138">複製這個列舉值的目前列舉狀態。</span><span class="sxs-lookup"><span data-stu-id="dbc08-138">Copies the current enumeration state of this enumerator.</span></span>

</dd> </dl>

 

 