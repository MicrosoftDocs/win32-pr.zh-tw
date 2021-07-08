---
description: 屬性是由稱為屬性識別碼 (Pid) 的識別碼來表示。
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: 瞭解屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b44d0a3a6d0a1b6c929eb151551155d0b5435a0
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481933"
---
# <a name="understanding-property-handlers"></a><span data-ttu-id="a9449-103">瞭解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="a9449-103">Understanding Property Handlers</span></span>

<span data-ttu-id="a9449-104">屬性是由稱為屬性識別碼 (Pid) 的識別碼來表示。</span><span class="sxs-lookup"><span data-stu-id="a9449-104">Properties are represented by IDs known as property identifiers (PIDs).</span></span> <span data-ttu-id="a9449-105">每個屬性都必須有全域唯一識別碼 (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="a9449-105">Each property MUST have a globally unique identifier (GUID).</span></span> <span data-ttu-id="a9449-106">此識別碼是由 GUID 所組成，表示稱為屬性集的屬性集合，加上字串或32位整數，以識別集合中的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9449-106">This identifier consists of a GUID, representing a collection of properties called a property set plus either a string or a 32-bit integer to identify the property within the set.</span></span> <span data-ttu-id="a9449-107">如果使用整數形式的識別碼，則會將0x00000000、0xFFFFFFFF 和0xFFFFFFFE 值視為無效。</span><span class="sxs-lookup"><span data-stu-id="a9449-107">If the integer form of ID is used, the values 0x00000000, 0xFFFFFFFF, and 0xFFFFFFFE are considered invalid.</span></span> <span data-ttu-id="a9449-108">廠商可以將屬性放在自己的 Guid 所定義的屬性集中，以保證其屬性是唯一的定義。</span><span class="sxs-lookup"><span data-stu-id="a9449-108">Vendors can guarantee that their properties are uniquely defined by placing them in a property set defined by their own GUIDs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9449-109">您必須謹慎且策略性地定義第一版架構的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9449-109">It is critical that you define properties carefully and strategically for the first release of the schema.</span></span> <span data-ttu-id="a9449-110">自訂屬性的任何變更 (例如資料行寬度或屬性類型) ，在架構註冊之後，將不會反映在資料庫中。</span><span class="sxs-lookup"><span data-stu-id="a9449-110">Any changes to custom properties (such as column width or property type) will not be reflected in the database after a schema has been registered.</span></span> <span data-ttu-id="a9449-111">在系統上註冊架構一次之後，可辨識這些變更的唯一方法就是重建索引，然後註冊新的架構，或註冊架構，然後建立新的屬性 (，其中包含每個 subequent 版本的正式名稱和 PKEY) 。例如 `PKEY_GroupName_PropertyNameV2` ，等 `PKEY_GroupName_PropertyNameV3`) 。</span><span class="sxs-lookup"><span data-stu-id="a9449-111">The only way to have these changes recognized after the schema has been registered once on a system would be either to rebuild the index and then register the new schema, or to register the schema and then create a new property (which consists of a canonical name and a PKEY) for each subequent release; for example `PKEY_GroupName_PropertyNameV2`, `PKEY_GroupName_PropertyNameV3`, and so forth).</span></span> <span data-ttu-id="a9449-112">我們不建議以這種方式建立新的屬性，因為多個額外的資料行可能會影響系統效能。</span><span class="sxs-lookup"><span data-stu-id="a9449-112">We do not recommend creating new properties in this manner, because multiple extraneous columns may impact system performance.</span></span>

 

<span data-ttu-id="a9449-113">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="a9449-113">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a9449-114">中繼資料</span><span class="sxs-lookup"><span data-stu-id="a9449-114">Metadata</span></span>](#metadata)
    -   [<span data-ttu-id="a9449-115">開啟中繼資料</span><span class="sxs-lookup"><span data-stu-id="a9449-115">Open Metadata</span></span>](#open-metadata)
-   [<span data-ttu-id="a9449-116">關於屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="a9449-116">About Property Handlers</span></span>](#about-property-handlers)
-   [<span data-ttu-id="a9449-117">舊版技術</span><span class="sxs-lookup"><span data-stu-id="a9449-117">Legacy Technology</span></span>](#legacy-technology)
-   [<span data-ttu-id="a9449-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9449-118">Related topics</span></span>](#related-topics)

## <a name="metadata"></a><span data-ttu-id="a9449-119">中繼資料</span><span class="sxs-lookup"><span data-stu-id="a9449-119">Metadata</span></span>

<span data-ttu-id="a9449-120">在 Windows Vista 和更新版本中，以中繼資料為基礎的新屬性系統是組織專案（例如檔案、電子郵件和連絡人）的核心。</span><span class="sxs-lookup"><span data-stu-id="a9449-120">In Windows Vista and later, a new property system based on metadata is central to organizing items such as files, e-mail, and contacts.</span></span> <span data-ttu-id="a9449-121">在這個新的屬性系統中，可以根據專案的中繼資料來搜尋專案，而且使用者可以讀取或寫入該中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a9449-121">In this new property system, items can be searched based on their metadata, and users can read or write that metadata.</span></span> <span data-ttu-id="a9449-122">這個系統中的中繼資料是以實作為名稱/值組的可延伸 *屬性* 集來表示。</span><span class="sxs-lookup"><span data-stu-id="a9449-122">Metadata in this system is represented by an extensible set of *properties* implemented as name/value pairs.</span></span>

<span data-ttu-id="a9449-123">在 Windows Vista 和更新版本中，有一組廣泛的屬性涵蓋了相片、音樂、檔、郵件、連絡人和檔案等專案的細節。</span><span class="sxs-lookup"><span data-stu-id="a9449-123">In Windows Vista and later, an extensive set of properties covers the specifics of items such as photos, music, documents, messages, contacts, and files.</span></span> <span data-ttu-id="a9449-124">獨立軟體廠商 (Isv) 如果沒有任何現有的屬性符合需求，就可以將自己的屬性引入平臺。</span><span class="sxs-lookup"><span data-stu-id="a9449-124">Independent software vendors (ISVs) can introduce their own properties to the platform if no existing property meets their needs.</span></span>

### <a name="open-metadata"></a><span data-ttu-id="a9449-125">開啟中繼資料</span><span class="sxs-lookup"><span data-stu-id="a9449-125">Open Metadata</span></span>

<span data-ttu-id="a9449-126">Windows Vista 和更新版本中的屬性系統是開放式中繼資料系統。</span><span class="sxs-lookup"><span data-stu-id="a9449-126">The property system in Windows Vista and later is an open metadata system.</span></span> <span data-ttu-id="a9449-127">檔案格式會儲存任何指派給它的屬性，並在查詢時公開該值，無論相關性或意義為何。</span><span class="sxs-lookup"><span data-stu-id="a9449-127">A file format stores any property assigned to it and exposes that value when queried, regardless of relevance or meaning.</span></span> <span data-ttu-id="a9449-128">這可讓協力廠商開發人員將額外的屬性附加至檔案，而不需要變更與其相關聯的屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="a9449-128">This enables third-party developers to attach extra properties to the file without requiring a change in the property handler associated with it.</span></span> <span data-ttu-id="a9449-129">開放式中繼資料是一種強大的概念。</span><span class="sxs-lookup"><span data-stu-id="a9449-129">Open metadata is a powerful concept.</span></span> <span data-ttu-id="a9449-130">如需有關如何支援以 XML 為基礎的檔案格式開啟中繼資料的詳細資訊，請參閱 [初始化屬性處理常式](./building-property-handlers-property-handlers.md)中的「支援開放中繼資料」。</span><span class="sxs-lookup"><span data-stu-id="a9449-130">For more information about how to support open metadata for an XML-based file format, see "Supporting Open Metadata" in [Initializing Property Handlers](./building-property-handlers-property-handlers.md).</span></span>

> [!Note]  
> <span data-ttu-id="a9449-131">屬性處理常式一律會與特定檔案類型相關聯;因此，如果您的檔案格式包含需要自訂屬性處理常式的屬性，您應該一律為每個檔案格式註冊唯一的副檔名。</span><span class="sxs-lookup"><span data-stu-id="a9449-131">Property handlers are always associated with specific file types; thus, if your file format contains properties that require a custom property handler, you should always register a unique file name extension for each file format.</span></span>

 

## <a name="about-property-handlers"></a><span data-ttu-id="a9449-132">關於屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="a9449-132">About Property Handlers</span></span>

<span data-ttu-id="a9449-133">在 Windows Vista 和更新版本中，Windows 具有可延伸的屬性系統，可在您存取的檔案和資料項目中儲存和取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a9449-133">In Windows Vista and later, Windows has an extensible property system for storing and retrieving metadata in the files and data items that you access.</span></span> <span data-ttu-id="a9449-134">WindowsExplorer 和 Windows Search 系統，以及其他應用程式，請使用屬性處理常式來讀取和修改此中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a9449-134">Windows Explorer and the Windows Search system, along with other applications, use property handlers to read and modify this metadata.</span></span> <span data-ttu-id="a9449-135">如果您是擁有特定檔案類型的開發人員，您應該註冊屬性處理常式，以授與屬性系統對您檔案中中繼資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="a9449-135">If you are a developer who owns a specific file type, you should register a property handler to give the property system access to the metadata in your files.</span></span> <span data-ttu-id="a9449-136">在某些情況下，您可以使用現有的屬性處理常式，該處理常式可以讀取及瞭解您的檔案格式及其屬性;在其他情況下，您可能需要為您的檔案類型開發新的屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="a9449-136">In some cases, you might be able to use an existing property handler that can read and understand your file format and its properties; in other cases, you might need to develop a new property handler for your file type.</span></span>

<span data-ttu-id="a9449-137">撰寫屬性處理常式的第一步是考慮您的檔案類型所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9449-137">The first step in writing a property handler is to consider what properties your file type supports.</span></span> <span data-ttu-id="a9449-138">屬性值會儲存在檔案資料流程中，主要是用來啟用可傳送性。</span><span class="sxs-lookup"><span data-stu-id="a9449-138">Property values are stored in the file stream, primarily to enable transportability.</span></span> <span data-ttu-id="a9449-139">當屬性值儲存在檔案本身時（如同在此系統中），使用者可以將檔案複製到另一部電腦、USB 快閃磁片磁碟機或其他檔案系統，或以電子郵件附件的形式傳送檔案，這些屬性會隨著檔案移動，且永遠不會遺失或遺失。</span><span class="sxs-lookup"><span data-stu-id="a9449-139">When the property values are stored in the file itself, as they are in this system, a user can copy a file to another computer, a USB flash drive, or another file system, or sends the file as an e-mail attachment, the properties travel with the file and never get out of sync or lost.</span></span> <span data-ttu-id="a9449-140">因此，如果檔案格式支援儲存額外的資訊，最好將屬性儲存在檔案本身。</span><span class="sxs-lookup"><span data-stu-id="a9449-140">Therefore, if the file format supports storing extra information, it is best to store the properties in the file itself.</span></span>

<span data-ttu-id="a9449-141">下一步是判斷檔案應提供哪些屬性。</span><span class="sxs-lookup"><span data-stu-id="a9449-141">The next step is to determine which properties the file should provide.</span></span> <span data-ttu-id="a9449-142">您可能一開始會認為一組有限的屬性已足夠。</span><span class="sxs-lookup"><span data-stu-id="a9449-142">You might initially think that a limited set of properties is adequate.</span></span> <span data-ttu-id="a9449-143">音訊檔案只能支援音訊相關屬性，並在該處結束。</span><span class="sxs-lookup"><span data-stu-id="a9449-143">An audio file could support only audio-related properties and end there.</span></span> <span data-ttu-id="a9449-144">不過，該音訊檔案可能是由法律事務所所封存之法院的會話記錄。</span><span class="sxs-lookup"><span data-stu-id="a9449-144">However, that audio file could be a recording of a session of a court of law, archived by a law firm.</span></span> <span data-ttu-id="a9449-145">在這種情況下，法律事務所肯定會想要將其他非音訊屬性與這個檔案相關聯，例如案例號碼。</span><span class="sxs-lookup"><span data-stu-id="a9449-145">In that case, the law firm would certainly want to associate other non-audio properties with this file, such as the case number.</span></span> <span data-ttu-id="a9449-146">音訊檔案格式的提供者不可能決定將使用其格式的所有案例。</span><span class="sxs-lookup"><span data-stu-id="a9449-146">The provider of the audio file format cannot possibly determine all of the scenarios in which their format will ever be used.</span></span> <span data-ttu-id="a9449-147">因此，它們應該考慮啟用屬性系統所支援之任何任意屬性的總儲存體。</span><span class="sxs-lookup"><span data-stu-id="a9449-147">They should therefore consider enabling blanket storage of any arbitrary property supported by the property system.</span></span>

## <a name="legacy-technology"></a><span data-ttu-id="a9449-148">舊版技術</span><span class="sxs-lookup"><span data-stu-id="a9449-148">Legacy Technology</span></span>

<span data-ttu-id="a9449-149">Microsoft Windows NT 檔案系統 (NTFS) 次要串流技術的開發目的，是為了支援透過檔案系統層上的替代資料流程設定，在檔案中保存額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="a9449-149">Microsoft Windows NT File System (NTFS) secondary stream technology was developed to support the persistence of extra information with the file through an alternate stream set at the file system layer.</span></span> <span data-ttu-id="a9449-150">您可能會想知道為何這些次要資料流程不是用來儲存屬性的主要方法，尤其是開啟的中繼資料支援。</span><span class="sxs-lookup"><span data-stu-id="a9449-150">One might wonder why those secondary streams are not used as the main method to store properties, especially with open metadata support.</span></span> <span data-ttu-id="a9449-151">主要原因是此額外資訊的可傳送性。</span><span class="sxs-lookup"><span data-stu-id="a9449-151">The primary reason is the transportability of this extra information.</span></span> <span data-ttu-id="a9449-152">可惜的是，在許多情況下都會移除這些替代資料流程，包括用戶端快取支援 (CSC) 、將檔案當作附件傳送，以及將檔案複製到非 NTFS 存放區。</span><span class="sxs-lookup"><span data-stu-id="a9449-152">Unfortunately, these alternate streams are removed in many scenarios including client-side caching support (CSC), sending files as attachments, and copying files to a non-NTFS store.</span></span>

<span data-ttu-id="a9449-153">次要資料流程不提供健全的解決方案，可保證屬性與檔案一起移動，因此 Windows Vista 屬性系統不會提供可利用次要 NTFS 資料流程進行屬性儲存的內建機制。</span><span class="sxs-lookup"><span data-stu-id="a9449-153">Secondary streams do not provide a robust solution in which properties are guaranteed to travel with the file, and hence, the Windows Vista property system does not provide a built-in mechanism that exploits the secondary NTFS streams for property storage.</span></span> <span data-ttu-id="a9449-154">Isv 也不建議您建立屬性處理常式，以使用次要串流來儲存屬性。</span><span class="sxs-lookup"><span data-stu-id="a9449-154">ISVs are also highly discouraged from building property handlers that use secondary streams for the storage of properties.</span></span> <span data-ttu-id="a9449-155">當然，在某些情況下，NTFS 次要資料流程是適當的，特別是當應用程式可保證其處理的檔案一律儲存在 NTFS 磁片區中，而且不會因為使用者互動而移動。</span><span class="sxs-lookup"><span data-stu-id="a9449-155">Of course there are scenarios where NTFS secondary streams are appropriate, particularly when applications can guarantee that the file they are dealing with is always stored in an NTFS volume and will not travel as a result of end user interaction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9449-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9449-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9449-157">使用種類名稱</span><span class="sxs-lookup"><span data-stu-id="a9449-157">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="a9449-158">使用屬性清單</span><span class="sxs-lookup"><span data-stu-id="a9449-158">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="a9449-159">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="a9449-159">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="a9449-160">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="a9449-160">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="a9449-161">屬性處理常式的最佳作法和常見問題</span><span class="sxs-lookup"><span data-stu-id="a9449-161">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
