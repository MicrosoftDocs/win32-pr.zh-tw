---
description: Microsoft Windows 筆記本 Note Reader 元件提供以程式設計方式讀取日誌格式的檔案。
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: 使用日誌讀取器元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943393"
---
# <a name="using-the-journal-reader-component"></a><span data-ttu-id="51104-103">使用日誌讀取器元件</span><span class="sxs-lookup"><span data-stu-id="51104-103">Using the Journal Reader Component</span></span>

<span data-ttu-id="51104-104">Microsoft Windows 筆記本 Note Reader 元件提供以程式設計方式讀取日誌格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="51104-104">The Microsoft Windows Journal Note Reader component provides programmatic read access to files in the Journal format.</span></span>

## <a name="component-overview"></a><span data-ttu-id="51104-105">元件總覽</span><span class="sxs-lookup"><span data-stu-id="51104-105">Component Overview</span></span>

<span data-ttu-id="51104-106">日誌檔案的副檔名為 .jnt。</span><span class="sxs-lookup"><span data-stu-id="51104-106">Journal files have the .jnt file extension.</span></span> <span data-ttu-id="51104-107">這個簡單的元件接受包含 .jnt 檔案的資料流程，並以 XML 格式傳回包含檔案內容的資料流程。</span><span class="sxs-lookup"><span data-stu-id="51104-107">This simple component takes a stream containing a .jnt file and returns a stream containing the file's content in XML format.</span></span> <span data-ttu-id="51104-108">元件所傳回的 XML 會符合筆記本便箋讀取器架構。</span><span class="sxs-lookup"><span data-stu-id="51104-108">The XML returned by the component conforms to the Journal Note Reader schema.</span></span> <span data-ttu-id="51104-109">此架構記載于 [日誌讀取器架構參考](journal-reader-schema-reference.md)中。</span><span class="sxs-lookup"><span data-stu-id="51104-109">This schema is documented in [Journal Reader Schema Reference](journal-reader-schema-reference.md).</span></span>

<span data-ttu-id="51104-110">元件不提供寫出 .jnt 檔案的能力。</span><span class="sxs-lookup"><span data-stu-id="51104-110">The component does not provide the ability to write out .jnt files.</span></span>

<span data-ttu-id="51104-111">元件可用於非受控和受控版本。</span><span class="sxs-lookup"><span data-stu-id="51104-111">The component is available in unmanaged and managed versions.</span></span> <span data-ttu-id="51104-112">未受管理的元件可在 journal.dll 動態連結程式庫 (DLL) 中取得。</span><span class="sxs-lookup"><span data-stu-id="51104-112">The unmanaged component is available in the journal.dll dynamic link library (DLL).</span></span> <span data-ttu-id="51104-113">受控版本位於 Microsoft.Ink.Journal.dll 元件 (，可轉散發至 Windows XP Tablet PC Edition 或 Windows Vista) ，或 Microsoft.Ink.dll。</span><span class="sxs-lookup"><span data-stu-id="51104-113">The managed version is either in the Microsoft.Ink.Journal.dll assembly (for redistribution to Windows XP Tablet PC Edition or Windows Vista), or Microsoft.Ink.dll.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="51104-114">從 Windows 10 開始，版本1607，journal.dll 不包含在 Windows 作業系統中。</span><span class="sxs-lookup"><span data-stu-id="51104-114">Beginning with Windows 10, version 1607, journal.dll is not included in the Windows operating system.</span></span> <span data-ttu-id="51104-115">該程式庫應視為已淘汰或已淘汰，且不應該使用。</span><span class="sxs-lookup"><span data-stu-id="51104-115">That library should be considered deprecated or obsolete and should not be used.</span></span>

 

### <a name="assembly-changes-of-note"></a><span data-ttu-id="51104-116">注意事項的元件變更</span><span class="sxs-lookup"><span data-stu-id="51104-116">Assembly Changes of Note</span></span>

<span data-ttu-id="51104-117">請務必留意元件的一些變更，其中包含與平板電腦開發人員套件1.7 版和 Windows Vista 作業系統隨附的版本之間所發行的「筆記本便箋讀取器」元件。</span><span class="sxs-lookup"><span data-stu-id="51104-117">It is important to be aware of some changes to the assembly containing the Journal Note Reader component that occurred between the version released in conjunction with version 1.7 of the Tablet Developers Kit and the version that ships in the Windows Vista operating system.</span></span>

<span data-ttu-id="51104-118">可以轉散發至 Windows XP 或 Windows Vista 的讀取器元件1.7 版本，包含在名為 Microsoft.Ink.Journal.dll 的元件中。</span><span class="sxs-lookup"><span data-stu-id="51104-118">The 1.7 version of the reader component, which can be redistributed to either Windows XP or Windows Vista, is contained in an assembly called Microsoft.Ink.Journal.dll.</span></span> <span data-ttu-id="51104-119">讀取器元件隨附于 Windows Vista 中，但已整合至核心 Microsoft.Ink.dll 元件。</span><span class="sxs-lookup"><span data-stu-id="51104-119">The reader component ships in Windows Vista, but has been integrated into the core Microsoft.Ink.dll assembly.</span></span> <span data-ttu-id="51104-120">這表示使用1.7 元件的應用程式必須將該元件重新發佈到其設定。</span><span class="sxs-lookup"><span data-stu-id="51104-120">This means that applications that make use of the 1.7 assembly need to redistribute that assembly with their setup.</span></span>

## <a name="using-the-component"></a><span data-ttu-id="51104-121">使用元件</span><span class="sxs-lookup"><span data-stu-id="51104-121">Using the Component</span></span>

<span data-ttu-id="51104-122">筆記本便箋讀取器元件適合用來從日誌檔案中解壓縮筆墨資料和檔案的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="51104-122">The Journal Note Reader component is useful for extracting the ink data and other information about the file from a Journal file.</span></span>

### <a name="com"></a><span data-ttu-id="51104-123">COM</span><span class="sxs-lookup"><span data-stu-id="51104-123">COM</span></span>

<span data-ttu-id="51104-124">筆記本便箋讀取器 COM 元件位於檔案 Journal.dll 中，當您下載並執行筆記本便箋讀取器安裝檔案時，會安裝並註冊此元件。</span><span class="sxs-lookup"><span data-stu-id="51104-124">The Journal Note Reader COM component is in the file Journal.dll, which is installed and registered when you download and run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="51104-125">COM 元件不支援 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面。</span><span class="sxs-lookup"><span data-stu-id="51104-125">The COM component does not support the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

### <a name="managed"></a><span data-ttu-id="51104-126">受控</span><span class="sxs-lookup"><span data-stu-id="51104-126">Managed</span></span>

<span data-ttu-id="51104-127">筆記本便箋讀取器管理的元件位於 Microsoft.Ink.JournalReader.dll 元件中。</span><span class="sxs-lookup"><span data-stu-id="51104-127">The Journal Note Reader managed component is in the Microsoft.Ink.JournalReader.dll assembly.</span></span> <span data-ttu-id="51104-128">當您執行筆記本便箋讀取器安裝檔案時，會在全域組件快取中安裝並註冊此元件。</span><span class="sxs-lookup"><span data-stu-id="51104-128">This assembly is installed and registered in the global assembly cache when you run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="51104-129">加入元件的參考，以便在您的 managed 專案中使用它。</span><span class="sxs-lookup"><span data-stu-id="51104-129">Add a reference to the assembly to use it in your managed project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51104-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="51104-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51104-131">**IJournalReader 介面**</span><span class="sxs-lookup"><span data-stu-id="51104-131">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="51104-132">日誌讀取器架構參考</span><span class="sxs-lookup"><span data-stu-id="51104-132">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

 
