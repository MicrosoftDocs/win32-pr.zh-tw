---
title: 結構化儲存體
description: 結構化儲存區藉由將單一檔案作為結構化的物件集合（稱為儲存和資料流程）來處理，以提供 COM 中的檔案和資料持續性。
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- 結構化儲存體 Strctd Stg。
- 結構化儲存體 Strctd Stg.，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315706"
---
# <a name="structured-storage"></a><span data-ttu-id="5b997-105">結構化儲存體</span><span class="sxs-lookup"><span data-stu-id="5b997-105">Structured Storage</span></span>

## <a name="purpose"></a><span data-ttu-id="5b997-106">目的</span><span class="sxs-lookup"><span data-stu-id="5b997-106">Purpose</span></span>

<span data-ttu-id="5b997-107">結構化儲存區藉由將單一檔案作為結構化的物件集合（稱為儲存和資料流程）來處理，以提供 COM 中的檔案和資料持續性。</span><span class="sxs-lookup"><span data-stu-id="5b997-107">Structured Storage provides file and data persistence in COM by handling a single file as a structured collection of objects known as storages and streams.</span></span>

<span data-ttu-id="5b997-108">結構化儲存區的目的是要降低在單一檔案中儲存個別物件的效能損失和負擔。</span><span class="sxs-lookup"><span data-stu-id="5b997-108">The purpose of Structured Storage is to reduce the performance penalties and overhead associated with storing separate objects in a single file.</span></span> <span data-ttu-id="5b997-109">結構化儲存體提供方案，方法是定義如何將單一檔案實體處理為兩種類型之物件的結構化集合，以及透過標準的實作為（稱為複合檔案）進行串流處理。</span><span class="sxs-lookup"><span data-stu-id="5b997-109">Structured Storage provides a solution by defining how to handle a single file entity as a structured collection of two types of objects storages and streams through a standard implementation called Compound Files.</span></span> <span data-ttu-id="5b997-110">這可讓使用者與複合檔案進行互動及管理，就像是單一檔案，而不是個別物件的嵌套階層一樣。</span><span class="sxs-lookup"><span data-stu-id="5b997-110">This enables the user to interact with, and manage, a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5b997-111">適用時</span><span class="sxs-lookup"><span data-stu-id="5b997-111">Where applicable</span></span>

<span data-ttu-id="5b997-112">結構化儲存體可用於以 Microsoft COM 為基礎的作業系統上。</span><span class="sxs-lookup"><span data-stu-id="5b997-112">Structured Storage can be used on Microsoft COM-based operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5b997-113">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="5b997-113">Developer audience</span></span>

<span data-ttu-id="5b997-114">結構化儲存體檔適用于有經驗的 C 和 c + + 程式設計人員，以及以 COM 為基礎的系統開發人員。</span><span class="sxs-lookup"><span data-stu-id="5b997-114">The Structured Storage documentation is intended for experienced C and C++ programmers and COM-based system developers.</span></span>

<span data-ttu-id="5b997-115">結構化儲存體主要支援 C 和 c + + 程式設計語言，但任何以 COM 為基礎的技術也會支援任何使用介面指標的程式設計語言。</span><span class="sxs-lookup"><span data-stu-id="5b997-115">Structured Storage primarily supports C and C++ programming languages, however any COM-based technology will also support any programming language that utilizes interface pointers.</span></span>

<span data-ttu-id="5b997-116">強烈瞭解 COM 技術是開發使用結構化儲存體的必要條件。</span><span class="sxs-lookup"><span data-stu-id="5b997-116">A solid understanding of COM technologies is prerequisite to the developmental use of Structured Storage.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5b997-117">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="5b997-117">Run-time requirements</span></span>

<span data-ttu-id="5b997-118">如需有關使用特定 API 專案所需之作業系統的詳細資訊，請參閱元素檔集的需求一節。</span><span class="sxs-lookup"><span data-stu-id="5b997-118">For more information about which operating systems are required to use a particular API element, see the Requirements section of the documentation for the element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5b997-119">本節內容</span><span class="sxs-lookup"><span data-stu-id="5b997-119">In this section</span></span>



| <span data-ttu-id="5b997-120">主題</span><span class="sxs-lookup"><span data-stu-id="5b997-120">Topic</span></span>                                                               | <span data-ttu-id="5b997-121">描述</span><span class="sxs-lookup"><span data-stu-id="5b997-121">Description</span></span>                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b997-122">概觀</span><span class="sxs-lookup"><span data-stu-id="5b997-122">Overview</span></span>](about-structured-storage.md)<br/>                 | <span data-ttu-id="5b997-123">結構化儲存體的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="5b997-123">General information about Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="5b997-124">使用結構化儲存體</span><span class="sxs-lookup"><span data-stu-id="5b997-124">Using Structured Storage</span></span>](using-structured-storage.md)<br/> | <span data-ttu-id="5b997-125">使用結構化儲存體的資訊。</span><span class="sxs-lookup"><span data-stu-id="5b997-125">Using information for Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="5b997-126">參考</span><span class="sxs-lookup"><span data-stu-id="5b997-126">Reference</span></span>](structured-storage-reference.md)<br/>            | <span data-ttu-id="5b997-127">結構化儲存體特定介面、函數、結構和列舉的檔。</span><span class="sxs-lookup"><span data-stu-id="5b997-127">Documentation of Structured Storage specific interfaces, functions, structures, and enumerations.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="5b997-128">範例</span><span class="sxs-lookup"><span data-stu-id="5b997-128">Samples</span></span>](samples.md)<br/>                                   | <span data-ttu-id="5b997-129">以 c + + 撰寫的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="5b997-129">Code examples written in C++.</span></span> <span data-ttu-id="5b997-130">如需詳細資訊，請參閱 [IStorage](names-in-istorage.md)中的名稱、 [屬性集標頭](property-set-header.md)、 [區段](section.md)、 [儲存屬性集](storing-property-sets.md)，以及 [使用結構化儲存體](using-structured-storage.md)。</span><span class="sxs-lookup"><span data-stu-id="5b997-130">For more information, see [Names in IStorage](names-in-istorage.md), [Property Set Header](property-set-header.md), [Section](section.md), [Storing Property Sets](storing-property-sets.md), and [Using Structured Storage](using-structured-storage.md).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5b997-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b997-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b997-132">元件物件模型</span><span class="sxs-lookup"><span data-stu-id="5b997-132">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> </dl>

 

