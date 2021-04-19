---
description: 測試寫入器是一種公用程式，可讓您用來測試 VSS 要求者應用程式。
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: VSS 測試編寫器工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ffdbb513697a701866be5ceeb40168e8c28368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973646"
---
# <a name="vss-test-writer-tool"></a><span data-ttu-id="8d31e-103">VSS 測試編寫器工具</span><span class="sxs-lookup"><span data-stu-id="8d31e-103">VSS Test Writer Tool</span></span>

<span data-ttu-id="8d31e-104">測試寫入器是一種公用程式，可讓您用來測試 VSS 要求者應用程式。</span><span class="sxs-lookup"><span data-stu-id="8d31e-104">The Test Writer is a utility that you can use to test VSS requester applications.</span></span> <span data-ttu-id="8d31e-105">此寫入器可以設定為執行 VSS 寫入器可執行檔幾乎所有動作。</span><span class="sxs-lookup"><span data-stu-id="8d31e-105">This writer can be configured to perform almost all of the actions that a VSS writer can perform.</span></span> <span data-ttu-id="8d31e-106">此外，測試寫入器會執行大量檢查，以確保要求者已正確處理這些寫入器動作。</span><span class="sxs-lookup"><span data-stu-id="8d31e-106">In addition, the Test Writer performs extensive checks to ensure that the requester has dealt with these writer actions correctly.</span></span>

<span data-ttu-id="8d31e-107">寫入器的每個實例都是使用 XML 設定檔來初始化，此檔案描述寫入器將報告的元件，以及寫入器的運作方式。</span><span class="sxs-lookup"><span data-stu-id="8d31e-107">Each instance of the writer is initialized with an XML configuration file that describes exactly what components the writer will report on, and how the writer behaves.</span></span> <span data-ttu-id="8d31e-108">您可以設定寫入器來報告各種類型的案例，包括使用累加和差異介面的更複雜案例。</span><span class="sxs-lookup"><span data-stu-id="8d31e-108">The writer can be configured to report on various types of scenarios, including more complicated scenarios using the incremental and differential interfaces.</span></span> <span data-ttu-id="8d31e-109">寫入器會在程式期間的各種時間點執行檢查，以確保要求者的行為正確。</span><span class="sxs-lookup"><span data-stu-id="8d31e-109">The writer will perform checks at various points during the process to ensure that the requester is behaving in a proper manner.</span></span> <span data-ttu-id="8d31e-110">還原完成之後，寫入器會檢查所有必要的檔案是否已還原，而不會損毀。</span><span class="sxs-lookup"><span data-stu-id="8d31e-110">After the restore is completed, the writer will check that all necessary files have been restored without corruption.</span></span> <span data-ttu-id="8d31e-111">寫入器也可以設定為執行其他作業，例如失敗的特定事件。</span><span class="sxs-lookup"><span data-stu-id="8d31e-111">The writer can also be configured to perform other operations such as failing specific events.</span></span>

> [!Note]  
> <span data-ttu-id="8d31e-112">這項工具組含在適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 中。</span><span class="sxs-lookup"><span data-stu-id="8d31e-112">This tool is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="8d31e-113">您可以從下載 Windows SDK [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="8d31e-113">You can download the Windows SDK from [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx).</span></span>

 

<span data-ttu-id="8d31e-114">在 Windows SDK 安裝中，可在 `%Program Files(x86)%\Windows Kits\8.1\bin\x64` 64 位 Windows) 和 (中找到 VssSampleProvider 工具 `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 。</span><span class="sxs-lookup"><span data-stu-id="8d31e-114">In the Windows SDK installation, the VssSampleProvider tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86`.</span></span>

## <a name="running-the-test-writer-tool"></a><span data-ttu-id="8d31e-115">執行測試編寫器工具</span><span class="sxs-lookup"><span data-stu-id="8d31e-115">Running the Test Writer Tool</span></span>

<span data-ttu-id="8d31e-116">若要啟動測試寫入器，請在命令提示字元中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="8d31e-116">To start the Test Writer, type the following at the command prompt:</span></span>

<span data-ttu-id="8d31e-117">**vswriter.exe** *設定檔*</span><span class="sxs-lookup"><span data-stu-id="8d31e-117">**vswriter.exe** *config-file*</span></span>

<span data-ttu-id="8d31e-118">其中 *設定檔是* 設定檔案的路徑，此設定檔會指定此寫入器的行為。</span><span class="sxs-lookup"><span data-stu-id="8d31e-118">where *config-file* is the path to a configuration file that specifies the behavior of this writer.</span></span>

<span data-ttu-id="8d31e-119">若要停止測試寫入器，請按 CTRL + C。</span><span class="sxs-lookup"><span data-stu-id="8d31e-119">To stop the Test Writer, press CTRL+C.</span></span>

<span data-ttu-id="8d31e-120">您可以同時執行多個測試寫入器實例。</span><span class="sxs-lookup"><span data-stu-id="8d31e-120">Multiple instances of the Test Writer can be run at the same time.</span></span> <span data-ttu-id="8d31e-121">不過，每個寫入器的實例將會報告相同的寫入器類別識別碼 (但) 不同的寫入器實例識別碼，因此邏輯路徑和元件名稱在所有同時執行的寫入器實例之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8d31e-121">However, each instance of the writer will report the same writer class ID (though a different writer instance ID), so logical paths and component names must be unique across all simultaneously running instances of the writer.</span></span>

<span data-ttu-id="8d31e-122">為了確保寫入器能夠正確檢查要求者是否已遵守排除檔案規格，所有備份的檔案都應該先從原始磁片區中刪除，再嘗試還原它們。</span><span class="sxs-lookup"><span data-stu-id="8d31e-122">To ensure that the writer can properly check that the requester has honored the exclude file specifications, all files that were backed up should be deleted from the original volume before attempting to restore them.</span></span> <span data-ttu-id="8d31e-123">建議您儲存每個寫入器案例的範本，以便可以輕鬆地重新建立案例。</span><span class="sxs-lookup"><span data-stu-id="8d31e-123">It is recommended that a template of each writer scenario be stored, so the scenario can be easily recreated.</span></span>

## <a name="using-a-configuration-file"></a><span data-ttu-id="8d31e-124">使用組態檔</span><span class="sxs-lookup"><span data-stu-id="8d31e-124">Using a Configuration File</span></span>

<span data-ttu-id="8d31e-125">下列範例設定檔（vswriter \_config.xml）可以在 `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` x86 平臺和 x64 平臺上找到 `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` 。</span><span class="sxs-lookup"><span data-stu-id="8d31e-125">The following sample configuration file, vswriter\_config.xml, can be found in `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` on x86 platforms and `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` on x64 platforms.</span></span>

``` syntax
<TestWriter usage="USER_DATA">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED"
                   writerRestore="always"
                   rebootRequired="no" />

    <ExcludeFile path="c:\writerData\notTheseFiles" 
                 filespec="excludeThisFile.txt" 
                 recursive="no"/>

    <Component componentType="filegroup"
               componentName="TestFiles">
        <ComponentFile path="c:\writerData\myFilesHere" 
                       filespec="*"
                       recursive="no" />
    </Component>

</TestWriter>
```

<span data-ttu-id="8d31e-126">此設定檔中的根項目命名為 TestWriter。</span><span class="sxs-lookup"><span data-stu-id="8d31e-126">The root element in this configuration file is named TestWriter.</span></span> <span data-ttu-id="8d31e-127">所有其他專案會排列在 TestWriter 元素之下。</span><span class="sxs-lookup"><span data-stu-id="8d31e-127">All other elements are arranged under the TestWriter element.</span></span>

<span data-ttu-id="8d31e-128">其中一個與 TestWriter 相關聯的屬性是 usage 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d31e-128">One of the attributes associated with TestWriter is the usage attribute.</span></span> <span data-ttu-id="8d31e-129">這個屬性會指定透過 [**IVssExamineWriterMetadata：： GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity)報告的使用類型。</span><span class="sxs-lookup"><span data-stu-id="8d31e-129">This attribute specifies the usage type reported through [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity).</span></span> <span data-ttu-id="8d31e-130">此屬性的其中一個可能值為使用者 \_ 資料。</span><span class="sxs-lookup"><span data-stu-id="8d31e-130">One of the possible values for this attribute is USER\_DATA.</span></span>

<span data-ttu-id="8d31e-131">根項目的第一個子項目必須一律為 RestoreMethod 元素。</span><span class="sxs-lookup"><span data-stu-id="8d31e-131">The first child element of the root element must always be a RestoreMethod element.</span></span> <span data-ttu-id="8d31e-132">這個元素會指定下列專案：</span><span class="sxs-lookup"><span data-stu-id="8d31e-132">This element specifies the following:</span></span>

-   <span data-ttu-id="8d31e-133">在此情況下，restore 方法 (， \_ 如果 \_ 可以 \_ 取代則還原 \_) </span><span class="sxs-lookup"><span data-stu-id="8d31e-133">The restore method (in this case, RESTORE\_IF\_CAN\_BE\_REPLACED)</span></span>
-   <span data-ttu-id="8d31e-134">寫入器是否需要還原事件 (在此情況下，一律) </span><span class="sxs-lookup"><span data-stu-id="8d31e-134">Whether the writer requires restore events (in this case, always)</span></span>
-   <span data-ttu-id="8d31e-135">還原寫入器之後是否需要重新開機 (在此案例中為否) </span><span class="sxs-lookup"><span data-stu-id="8d31e-135">Whether a reboot is required after the writer is restored (in this case, no)</span></span>

<span data-ttu-id="8d31e-136">這個元素可以選擇性地指定替代位置對應。</span><span class="sxs-lookup"><span data-stu-id="8d31e-136">This element can optionally specify an alternate-location mapping.</span></span> <span data-ttu-id="8d31e-137"> (在此案例中，未指定替代位置。 ) </span><span class="sxs-lookup"><span data-stu-id="8d31e-137">(In this case, no alternate location is specified.)</span></span>

<span data-ttu-id="8d31e-138">第二個子項目是 ExcludeFile 元素。</span><span class="sxs-lookup"><span data-stu-id="8d31e-138">The second child element is an ExcludeFile element.</span></span> <span data-ttu-id="8d31e-139">此元素會導致寫入器從備份中排除檔案或一組檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-139">This element causes the writer to exclude a file or a set of files from backup.</span></span>

<span data-ttu-id="8d31e-140">第三個子項目是元件元素。</span><span class="sxs-lookup"><span data-stu-id="8d31e-140">The third child element is a Component element.</span></span> <span data-ttu-id="8d31e-141">此元素會導致寫入器將元件新增至其中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8d31e-141">This element causes the writer to add a component to its metadata.</span></span> <span data-ttu-id="8d31e-142">元件專案包含屬性，用來描述元件和子項目，以描述元件的內容，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8d31e-142">A Component element contains attributes to describe the component and child elements to describe the content of the component, such as the following:</span></span>

-   <span data-ttu-id="8d31e-143">componentType，指出這是否為檔案群組或資料庫</span><span class="sxs-lookup"><span data-stu-id="8d31e-143">componentType to indicate whether this is a filegroup or a database</span></span>
-   <span data-ttu-id="8d31e-144">元件邏輯路徑的 logicalPath</span><span class="sxs-lookup"><span data-stu-id="8d31e-144">logicalPath for the component logical path</span></span>
-   <span data-ttu-id="8d31e-145">元件名稱的 componentName</span><span class="sxs-lookup"><span data-stu-id="8d31e-145">componentName for the name of the component</span></span>
-   <span data-ttu-id="8d31e-146">可選取以指出可選取的備份狀態</span><span class="sxs-lookup"><span data-stu-id="8d31e-146">selectable to indicate selectable-for-backup status</span></span>

<span data-ttu-id="8d31e-147">Component 元素也有一個名為 ComponentFile 的子專案，可將檔案規格新增至此元件。</span><span class="sxs-lookup"><span data-stu-id="8d31e-147">The Component element also has a child element named ComponentFile to add a file specification to this component.</span></span> <span data-ttu-id="8d31e-148"> (元件元素可以有任意數目的 ComponentFile 元素，可為每個元件指定。 ) 此 ComponentFile 元素具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="8d31e-148">(A Component element can have an arbitrary number of ComponentFile elements that can be specified for each component.) This ComponentFile element has the following attributes:</span></span>

-   <span data-ttu-id="8d31e-149">path = "c： \\ writerData \\ myFilesHere"</span><span class="sxs-lookup"><span data-stu-id="8d31e-149">path="c:\\writerData\\myFilesHere"</span></span>
-   <span data-ttu-id="8d31e-150">filespec = " \* "</span><span class="sxs-lookup"><span data-stu-id="8d31e-150">filespec="\*"</span></span>
-   <span data-ttu-id="8d31e-151">遞迴 = "no"</span><span class="sxs-lookup"><span data-stu-id="8d31e-151">recursive="no"</span></span>

<span data-ttu-id="8d31e-152">雖然測試寫入器會驗證要求者的行為，但並不會驗證設定檔是否一律為寫入器維護記載的語法。</span><span class="sxs-lookup"><span data-stu-id="8d31e-152">Although the Test Writer verifies requester behavior, it does not verify that the configuration file always maintains the documented semantics for a writer.</span></span> <span data-ttu-id="8d31e-153">良好的寫入器應該不會進行許多作業 (例如在多個元件中報告相同的檔案) ，而且是由 XML 設定檔的作者負責維護這些語義。</span><span class="sxs-lookup"><span data-stu-id="8d31e-153">There are many operations that a well-behaved writer should not do (such as report the same file in multiple components), and it is up to the author of the XML configuration file to maintain these semantics.</span></span>

## <a name="configuring-writer-attributes"></a><span data-ttu-id="8d31e-154">設定寫入器屬性</span><span class="sxs-lookup"><span data-stu-id="8d31e-154">Configuring Writer Attributes</span></span>

<span data-ttu-id="8d31e-155">TestWriter 根項目包含的屬性，可決定寫入器的各種行為。</span><span class="sxs-lookup"><span data-stu-id="8d31e-155">The TestWriter root element contains attributes that determine various behaviors of the writer.</span></span> <span data-ttu-id="8d31e-156">以下是一些可以改變的行為：</span><span class="sxs-lookup"><span data-stu-id="8d31e-156">Some of the behaviors that can be altered are the following:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d31e-157">屬性</span><span class="sxs-lookup"><span data-stu-id="8d31e-157">Attribute</span></span></th>
<th><span data-ttu-id="8d31e-158">描述</span><span class="sxs-lookup"><span data-stu-id="8d31e-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8d31e-159"><span id="verbosity"></span><span id="VERBOSITY"></span>冗長</span><span class="sxs-lookup"><span data-stu-id="8d31e-159"><span id="verbosity"></span><span id="VERBOSITY"></span>verbosity</span></span><br/></td>
<td><span data-ttu-id="8d31e-160">寫入器會將狀態列印到主控台，因為它會接收事件並進行處理。</span><span class="sxs-lookup"><span data-stu-id="8d31e-160">The writer prints the status to the console as it receives events and processes them.</span></span> <span data-ttu-id="8d31e-161">所顯示的詳細程度層級是由詳細資訊屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="8d31e-161">The level of verbosity displayed is specified by the verbosity attribute.</span></span> <span data-ttu-id="8d31e-162">有三個詳細等級可供選擇：</span><span class="sxs-lookup"><span data-stu-id="8d31e-162">There are three verbosity levels to choose from:</span></span><br/> <dl> <span data-ttu-id="8d31e-163"><dt><span id="low"></span><span id="LOW"></span>低</dt> </span><span class="sxs-lookup"><span data-stu-id="8d31e-163"><dt><span id="low"></span><span id="LOW"></span>low</dt> </span></span><dd> <span data-ttu-id="8d31e-164">只會列印寫入器中的失敗或要求者的不正確行為。</span><span class="sxs-lookup"><span data-stu-id="8d31e-164">Only failures in the writer or incorrect behavior from the requester will be printed.</span></span><br/> </dd> <span data-ttu-id="8d31e-165"><dt><span id="medium"></span><span id="MEDIUM"></span>中</dt> </span><span class="sxs-lookup"><span data-stu-id="8d31e-165"><dt><span id="medium"></span><span id="MEDIUM"></span>medium</dt> </span></span><dd> <span data-ttu-id="8d31e-166">除了額外的狀態資訊（例如接收事件時），也會列印低詳細資訊層級的所有專案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-166">Everything at the low verbosity level is printed in addition to extra status information such as when events are received.</span></span> <span data-ttu-id="8d31e-167">這是預設層級。</span><span class="sxs-lookup"><span data-stu-id="8d31e-167">This is the default level.</span></span><br/> </dd> <span data-ttu-id="8d31e-168"><dt><span id="high"></span><span id="HIGH"></span>高</dt> </span><span class="sxs-lookup"><span data-stu-id="8d31e-168"><dt><span id="high"></span><span id="HIGH"></span>high</dt> </span></span><dd> <span data-ttu-id="8d31e-169">報告寫入器操作的詳細狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="8d31e-169">Detailed status information about the operation of the writer is reported.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d31e-170"><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles</span><span class="sxs-lookup"><span data-stu-id="8d31e-170"><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles</span></span><br/></td>
<td><span data-ttu-id="8d31e-171">若要執行額外的驗證，請將此屬性設定為 &quot; [是]， &quot; 讓寫入器在建立磁片區陰影複製後立即刪除其所有檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-171">To perform extra verification, set this attribute to &quot;yes&quot; to cause the writer to delete all of its files immediately after the volume shadow copy is created.</span></span> <span data-ttu-id="8d31e-172">接著，要求者必須複製陰影複製中的檔案，因為它們已不存在於原始磁片區上。</span><span class="sxs-lookup"><span data-stu-id="8d31e-172">The requester must then copy the files from the shadow copy, because they no longer exist on the original volume.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8d31e-173">在算寫入器的情況下，會在算之後，但在建立陰影複製之前，從原始位置刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-173">In the case of spit writers, the files are deleted from the original location after the spit but before the shadow copy is created.</span></span> <span data-ttu-id="8d31e-174">建立陰影複製之後，就會從算目錄中刪除這些檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-174">After the shadow copy is created, the files are deleted from the spit directory.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d31e-175"><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles</span><span class="sxs-lookup"><span data-stu-id="8d31e-175"><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles</span></span><br/></td>
<td><span data-ttu-id="8d31e-176">若要刪除部分檔案，請將此屬性設定為 &quot; [是] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="8d31e-176">To delete partial files, set this attribute to &quot;yes&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d31e-177"><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles</span><span class="sxs-lookup"><span data-stu-id="8d31e-177"><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles</span></span><br/></td>
<td><span data-ttu-id="8d31e-178">若要刪除差異的檔案，請將此屬性設定為 &quot; [是] &quot; 。</span><span class="sxs-lookup"><span data-stu-id="8d31e-178">To delete differenced files, set this attribute to &quot;yes&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8d31e-179"><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes</span><span class="sxs-lookup"><span data-stu-id="8d31e-179"><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes</span></span><br/></td>
<td><span data-ttu-id="8d31e-180">將此屬性設定為 &quot; [是]， &quot; 讓寫入器檢查已備份的每個檔案都已還原到適當的位置，而且檔案未損毀。</span><span class="sxs-lookup"><span data-stu-id="8d31e-180">Set this attribute to &quot;yes&quot; to cause the writer to check that every file that has been backed up has been restored to an appropriate location, and that the file has not been corrupted.</span></span> <span data-ttu-id="8d31e-181">部分檔案和差異檔案也會正確處理。</span><span class="sxs-lookup"><span data-stu-id="8d31e-181">Partial files and differenced files are also correctly handled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8d31e-182"><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes</span><span class="sxs-lookup"><span data-stu-id="8d31e-182"><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes</span></span><br/></td>
<td><span data-ttu-id="8d31e-183">將此屬性設定為 &quot; [是] &quot; ，會導致寫入器檢查是否有符合排除清單中檔案規格的檔案不會還原。</span><span class="sxs-lookup"><span data-stu-id="8d31e-183">Set this attribute to &quot;yes&quot; to cause the writer to check that files matching a file specification in the exclude list are not restored.</span></span> <span data-ttu-id="8d31e-184">為了讓此功能正常運作，必須先清空還原目錄，再進行還原。</span><span class="sxs-lookup"><span data-stu-id="8d31e-184">For this to function correctly, the restore directories must be emptied prior to restore.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-alternate-location-mappings"></a><span data-ttu-id="8d31e-185">指定替代位置對應</span><span class="sxs-lookup"><span data-stu-id="8d31e-185">Specifying Alternate Location Mappings</span></span>

<span data-ttu-id="8d31e-186">如果還原方法是 VSS \_ WRE \_ 還原 \_ 至 \_ 替代 \_ 位置，或元件正常還原失敗，則替代位置對應會指定要還原的位置。</span><span class="sxs-lookup"><span data-stu-id="8d31e-186">An alternate location mapping specifies a location to restore to if the restore method is VSS\_WRE\_RESTORE\_TO\_ALTERNATE\_LOCATION or if normal restore of a component fails.</span></span> <span data-ttu-id="8d31e-187">寫入器可以使用 [**IVssExamineWriterMetadata：： GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) 方法，向要求者報告其替代位置對應。</span><span class="sxs-lookup"><span data-stu-id="8d31e-187">A writer can report its alternate location mappings to the requester by using the [**IVssExamineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) method.</span></span> <span data-ttu-id="8d31e-188">您可以藉由將 AlternateLocationMapping 子項目新增至 RestoreMethod 專案，將替代位置對應加入至測試寫入器設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d31e-188">You can add alternate location mappings to the Test Writer configuration file by adding AlternateLocationMapping subelements to the RestoreMethod element.</span></span>

<span data-ttu-id="8d31e-189">下列 RestoreMethod 專案包含 AlternateLocationMapping 子項目。</span><span class="sxs-lookup"><span data-stu-id="8d31e-189">The following RestoreMethod element contains a AlternateLocationMapping subelement.</span></span>

``` syntax
<RestoreMethod method="RESTORE_IF_CAN_REPLACE"
              writerRestore="always"
              rebootRequired="no">
    <AlternateLocationMapping path="c:\files"
                              filespec="*.txt"
                              recursive="no"
                              alternatePath="c:\altfiles"/>
</RestoreMethod>
```

<span data-ttu-id="8d31e-190">這個範例會指定要求者應先嘗試將所有符合 c： files 的檔案還原 \\ \\ \* 至 c： \\ files 目錄。</span><span class="sxs-lookup"><span data-stu-id="8d31e-190">This example specifies that the requester should first attempt to restore all of the files matching c:\\files\\\*.txt to the c:\\files directory.</span></span> <span data-ttu-id="8d31e-191">如果無法取代這些檔案的其中一個，要求者應該改為將所有檔案還原至 c： \\ altfiles 目錄。</span><span class="sxs-lookup"><span data-stu-id="8d31e-191">If one of these files cannot be replaced, the requester should restore all the files to the c:\\altfiles directory instead.</span></span> <span data-ttu-id="8d31e-192">要求者應該使用 [**>ivssbackupcomponents：： AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) 方法來儲存這個替代位置對應。</span><span class="sxs-lookup"><span data-stu-id="8d31e-192">The requester should save this alternate location mapping by using the [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) method.</span></span> <span data-ttu-id="8d31e-193">如果測試寫入器設定為檢查是否已還原檔案，它也會檢查要求者是否已呼叫 **AddAlternativeLocationMapping**。</span><span class="sxs-lookup"><span data-stu-id="8d31e-193">If the Test Writer is configured to check whether files have been restored, it will also check whether the requester has called **AddAlternativeLocationMapping**.</span></span>

## <a name="specifying-files-to-be-excluded"></a><span data-ttu-id="8d31e-194">指定要排除的檔案</span><span class="sxs-lookup"><span data-stu-id="8d31e-194">Specifying Files to Be Excluded</span></span>

<span data-ttu-id="8d31e-195">每個寫入器都可以指定檔案規格清單，以指定要從備份中排除的要求者檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-195">Every writer can specify a list of file specifications that specify files for the requester to exclude from backup.</span></span> <span data-ttu-id="8d31e-196">您可以藉由將 ExcludeFile 子項目新增至 TestWriter 根項目，將這些檔案規格新增至測試寫入器設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d31e-196">You can add these file specifications to the Test Writer configuration file by adding ExcludeFile subelements to the TestWriter root element.</span></span>

<span data-ttu-id="8d31e-197">以下是 ExcludeFile 子項目的範例，它會排除 C： \\ files 目錄中符合 c： temp 的所有 \\ 檔案 \* \* 。</span><span class="sxs-lookup"><span data-stu-id="8d31e-197">Here is an example of an ExcludeFile subelement that excludes all files in the C:\\files directory that match C:\\temp\*.\*.</span></span>

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a><span data-ttu-id="8d31e-198">備份算寫入器</span><span class="sxs-lookup"><span data-stu-id="8d31e-198">Backing Up Spit Writers</span></span>

<span data-ttu-id="8d31e-199">許多寫入器可作為「算寫入器」。</span><span class="sxs-lookup"><span data-stu-id="8d31e-199">Many writers act as "spit writers."</span></span> <span data-ttu-id="8d31e-200">算寫入器會根據一組原始的檔案建立中繼檔案或「算檔案」，並在備份時將算檔案放在替代位置。</span><span class="sxs-lookup"><span data-stu-id="8d31e-200">A spit writer creates intermediate files, or "spit files," based on an original set of files, and puts the spit files in an alternate location at backup time.</span></span> <span data-ttu-id="8d31e-201">寫入器會使用 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) 方法，通知要求者應該從替代位置將這些檔案還原。</span><span class="sxs-lookup"><span data-stu-id="8d31e-201">The writer uses the [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) method to notify the requester that it should back these files up from the alternate location.</span></span> <span data-ttu-id="8d31e-202">不過，這些檔案仍應還原至原始檔案的使用中位置。</span><span class="sxs-lookup"><span data-stu-id="8d31e-202">However, these files should still be restored to the active location of the original files.</span></span> <span data-ttu-id="8d31e-203">測試寫入器可以設定為特定檔案規格的算寫入器。</span><span class="sxs-lookup"><span data-stu-id="8d31e-203">The Test Writer can be configured to act as a spit writer for a particular file specification.</span></span>

<span data-ttu-id="8d31e-204">下列 ComponentFile 元素包含 alternatePath 屬性：</span><span class="sxs-lookup"><span data-stu-id="8d31e-204">The following ComponentFile element contains an alternatePath attribute:</span></span>

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

<span data-ttu-id="8d31e-205">此範例會將測試編寫器設定為在建立磁片區陰影複製之前，立即將符合 c： files 的所有檔案複製 \\ \\ \* 到 c： \\ files \\ 算目錄。</span><span class="sxs-lookup"><span data-stu-id="8d31e-205">This example configures the Test Writer to copy all files matching c:\\files\\\*.txt to the c:\\files\\spit directory immediately before the volume shadow copy is created.</span></span> <span data-ttu-id="8d31e-206">要求者必須從 c： \\ files \\ 算目錄備份檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-206">The requester must back up the files from the c:\\files\\spit directory.</span></span> <span data-ttu-id="8d31e-207">如果測試寫入器設定為刪除檔案，它會在建立陰影複製之前先刪除原始檔案，因此它們不會出現在陰影複製磁片區的 c： \\ files 目錄中。</span><span class="sxs-lookup"><span data-stu-id="8d31e-207">If the Test Writer is configured to delete files, it deletes the original files before the shadow copy is created, so they do not appear in the c:\\files directory on the shadow copy volume.</span></span> <span data-ttu-id="8d31e-208">在此情況下，會在 \\ \\ 建立陰影複製後刪除 c： files 算中的檔案，因此必須從 \\ 陰影複製磁片區上的 c： files \\ 算目錄進行備份。</span><span class="sxs-lookup"><span data-stu-id="8d31e-208">In this case, the files in c:\\files\\spit are deleted after the shadow copy is created, so they must be backed up from the c:\\files\\spit directory on the shadow copy volume.</span></span>

## <a name="reporting-component-dependencies"></a><span data-ttu-id="8d31e-209">報告元件相依性</span><span class="sxs-lookup"><span data-stu-id="8d31e-209">Reporting Component Dependencies</span></span>

<span data-ttu-id="8d31e-210">寫入器可以指定本機組件與存在於其他寫入器中的元件之間的相依性。</span><span class="sxs-lookup"><span data-stu-id="8d31e-210">Writers can specify a dependency between a local component and a component that exists in another writer.</span></span> <span data-ttu-id="8d31e-211">這些相依性會使用 [**IVssWMComponent：： GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)回報給要求者。</span><span class="sxs-lookup"><span data-stu-id="8d31e-211">These dependencies are reported to the requester using [**IVssWMComponent::GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency).</span></span> <span data-ttu-id="8d31e-212">您可以將一或多個相依性子項目新增至 Component 專案，以設定測試寫入器來報告這些相依性。</span><span class="sxs-lookup"><span data-stu-id="8d31e-212">The Test Writer can be configured to report these dependencies by adding one or more Dependency subelements to the Component element.</span></span>

<span data-ttu-id="8d31e-213">下列元件專案包含相依性子項目：</span><span class="sxs-lookup"><span data-stu-id="8d31e-213">The following Component element contains a Dependency subelement:</span></span>

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
         <Dependency writerId="<GUID of target writer>"
                     logicalPath="ComponentPath"
                     componentName="Writer2Component" />
    </Component>
```

<span data-ttu-id="8d31e-214">相依性會指定為相依性專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="8d31e-214">The dependency is specified as attributes of the Dependency element.</span></span> <span data-ttu-id="8d31e-215">writerId 是包含相依性目標的寫入器類別識別碼，logicalPath 是該寫入器中元件的邏輯路徑，而 componentName 是元件的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d31e-215">writerId is the class id of the writer containing the target of the dependency, logicalPath is the logical path to the component in that writer, and componentName is the name of the component.</span></span> <span data-ttu-id="8d31e-216">在此情況下，如果要求者在目前的寫入器中備份 "WriterComponent"，則也應該 \\ 在目標寫入器中備份元件 "ComponentPath Writer2Component"。</span><span class="sxs-lookup"><span data-stu-id="8d31e-216">In this case, if the requester is backing up "WriterComponent" in the current writer, it should also back up the component "ComponentPath\\Writer2Component" in the target writer.</span></span>

> [!Note]  
> <span data-ttu-id="8d31e-217">測試寫入器不會執行檢查，以確保會遵守相依性。</span><span class="sxs-lookup"><span data-stu-id="8d31e-217">The Test Writer performs no checking to ensure dependencies are honored.</span></span>

 

## <a name="failing-events"></a><span data-ttu-id="8d31e-218">失敗的事件</span><span class="sxs-lookup"><span data-stu-id="8d31e-218">Failing Events</span></span>

<span data-ttu-id="8d31e-219">測試寫入器可以設定為使寫入器所收到的任何一般事件失敗。</span><span class="sxs-lookup"><span data-stu-id="8d31e-219">The Test Writer can be configured to fail any of the normal events that a writer receives.</span></span> <span data-ttu-id="8d31e-220">這些事件如下所示：</span><span class="sxs-lookup"><span data-stu-id="8d31e-220">These events are as follows:</span></span>



| <span data-ttu-id="8d31e-221">事件</span><span class="sxs-lookup"><span data-stu-id="8d31e-221">Event</span></span>                                                                                                                                    | <span data-ttu-id="8d31e-222">描述</span><span class="sxs-lookup"><span data-stu-id="8d31e-222">Description</span></span>                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d31e-223"><span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>識別</span><span class="sxs-lookup"><span data-stu-id="8d31e-223"><span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Identify</span></span><br/>                                     | <span data-ttu-id="8d31e-224">收到 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 呼叫的回應。</span><span class="sxs-lookup"><span data-stu-id="8d31e-224">Received as a response to a [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) call.</span></span> <span data-ttu-id="8d31e-225">此處的失敗會導致無法報告寫入器。</span><span class="sxs-lookup"><span data-stu-id="8d31e-225">Failure here will cause the writer to not be reported.</span></span><br/>                                                                 |
| <span data-ttu-id="8d31e-226"><span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup</span><span class="sxs-lookup"><span data-stu-id="8d31e-226"><span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup</span></span><br/>     | <span data-ttu-id="8d31e-227">收到的回應是呼叫 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)的要求者。</span><span class="sxs-lookup"><span data-stu-id="8d31e-227">Received as a response to the requester calling [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).</span></span><br/>                                                                                                                 |
| <span data-ttu-id="8d31e-228"><span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot</span><span class="sxs-lookup"><span data-stu-id="8d31e-228"><span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot</span></span><br/> | <span data-ttu-id="8d31e-229">當要求者呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)，但在建立陰影複製之前收到。</span><span class="sxs-lookup"><span data-stu-id="8d31e-229">Received when the requester calls [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), but before the shadow copy is created.</span></span><br/>                                                                                              |
| <span data-ttu-id="8d31e-230"><span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>凍結</span><span class="sxs-lookup"><span data-stu-id="8d31e-230"><span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Freeze</span></span><br/>                                             | <span data-ttu-id="8d31e-231">在 [*PrepareForSnapshot*](vssgloss-p.md)之後立即收到，但在建立陰影複製之前。</span><span class="sxs-lookup"><span data-stu-id="8d31e-231">Received immediately after [*PrepareForSnapshot*](vssgloss-p.md), but still before the shadow copy is created.</span></span><br/>                                                                                                      |
| <span data-ttu-id="8d31e-232"><span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>解凍</span><span class="sxs-lookup"><span data-stu-id="8d31e-232"><span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Thaw</span></span><br/>                                                     | <span data-ttu-id="8d31e-233">陰影複製建立完成之後收到。</span><span class="sxs-lookup"><span data-stu-id="8d31e-233">Received after the shadow copy creation is finished.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="8d31e-234"><span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot</span><span class="sxs-lookup"><span data-stu-id="8d31e-234"><span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot</span></span><br/>                     | <span data-ttu-id="8d31e-235">在解凍完成之後但在 >ivssbackupcomponents 之前收到 [**：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 完成。</span><span class="sxs-lookup"><span data-stu-id="8d31e-235">Received after Thaw completes, but before [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) completes.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="8d31e-236"><span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>中止</span><span class="sxs-lookup"><span data-stu-id="8d31e-236"><span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Abort</span></span><br/>                                                 | <span data-ttu-id="8d31e-237">在 [*凍結*](vssgloss-f.md) 和 [*解除*](vssgloss-t.md) 凍結之間的時間過久，或要求者呼叫 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)時收到。</span><span class="sxs-lookup"><span data-stu-id="8d31e-237">Received if too much time elapses between [*Freeze*](vssgloss-f.md) and [*Thaw*](vssgloss-t.md) or if the requester calls [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).</span></span><br/> |
| <span data-ttu-id="8d31e-238"><span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete</span><span class="sxs-lookup"><span data-stu-id="8d31e-238"><span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete</span></span><br/>             | <span data-ttu-id="8d31e-239">當要求者結束時收到。</span><span class="sxs-lookup"><span data-stu-id="8d31e-239">Received when the requester exits.</span></span> <span data-ttu-id="8d31e-240">絕不會回報此處的失敗。</span><span class="sxs-lookup"><span data-stu-id="8d31e-240">Failures here will never be reported.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="8d31e-241"><span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>PreRestore</span><span class="sxs-lookup"><span data-stu-id="8d31e-241"><span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>PreRestore</span></span><br/>                             | <span data-ttu-id="8d31e-242">當要求者呼叫 >ivssbackupcomponents 時收到 [**：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)。</span><span class="sxs-lookup"><span data-stu-id="8d31e-242">Received when the requester calls [**IVssBackupComponents::PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="8d31e-243"><span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>PostRestore</span><span class="sxs-lookup"><span data-stu-id="8d31e-243"><span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>PostRestore</span></span><br/>                         | <span data-ttu-id="8d31e-244">當要求者呼叫 >ivssbackupcomponents 時收到 [**：:P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)。</span><span class="sxs-lookup"><span data-stu-id="8d31e-244">Received when the requester calls [**IVssBackupComponents::PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).</span></span><br/>                                                                                                                                         |



 

<span data-ttu-id="8d31e-245">這些失敗的設定方式是將一或多個 FailEvent 子項目新增至 TestWriter 根項目。</span><span class="sxs-lookup"><span data-stu-id="8d31e-245">These failures are configured by adding one or more FailEvent subelements to the TestWriter root element.</span></span> <span data-ttu-id="8d31e-246">可以設定的失敗類別有兩種：可重試且無法重試。</span><span class="sxs-lookup"><span data-stu-id="8d31e-246">There are two classes of failures that can be set: retryable and non-retryable.</span></span> <span data-ttu-id="8d31e-247">如果重試整個備份程式，則可能會發生可重試的錯誤，而無法重試的錯誤則不可能消失。</span><span class="sxs-lookup"><span data-stu-id="8d31e-247">Retryable errors are errors that may go away if the entire backup process is retried, while non-retryable errors are unlikely to disappear.</span></span> <span data-ttu-id="8d31e-248">根據可重試的屬性，選擇事件的失敗類型。</span><span class="sxs-lookup"><span data-stu-id="8d31e-248">The failure type for the event is chosen based on the retryable attribute.</span></span>

<span data-ttu-id="8d31e-249">以下是基本無法重試的失敗範例：</span><span class="sxs-lookup"><span data-stu-id="8d31e-249">Here is an example of a basic non-retryable failure:</span></span>

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

<span data-ttu-id="8d31e-250">此範例會導致寫入器在 [*凍結*](vssgloss-f.md) 事件期間失敗。</span><span class="sxs-lookup"><span data-stu-id="8d31e-250">This example will cause the writer to fail during the [*Freeze*](vssgloss-f.md) event.</span></span> <span data-ttu-id="8d31e-251">[**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 會將寫入器失敗報告為 VSS \_ E \_ WRITERERROR \_ NONRETRYABLE。</span><span class="sxs-lookup"><span data-stu-id="8d31e-251">[**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) will report the writer failure to be VSS\_E\_WRITERERROR\_NONRETRYABLE.</span></span>

<span data-ttu-id="8d31e-252">以下是基本可重試錯誤的範例：</span><span class="sxs-lookup"><span data-stu-id="8d31e-252">Here is an example of a basic retryable error:</span></span>

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

<span data-ttu-id="8d31e-253">此範例會導致寫入器在收到 [*凍結*](vssgloss-f.md) 事件前兩次失敗。</span><span class="sxs-lookup"><span data-stu-id="8d31e-253">This example will cause the writer to fail the first two times it receives a [*Freeze*](vssgloss-f.md) event.</span></span> <span data-ttu-id="8d31e-254">在前兩次之後，寫入器一律會成功。</span><span class="sxs-lookup"><span data-stu-id="8d31e-254">After the first two times, the writer will always succeed.</span></span> <span data-ttu-id="8d31e-255">透過 [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 回報的寫入器失敗會是隨機可重試的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8d31e-255">The writer failure reported through [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) will be a random retryable error code.</span></span>

## <a name="declaring-supported-backup-types"></a><span data-ttu-id="8d31e-256">宣告支援的備份類型</span><span class="sxs-lookup"><span data-stu-id="8d31e-256">Declaring Supported Backup Types</span></span>

<span data-ttu-id="8d31e-257">寫入器會透過要求者的呼叫 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)來傳達支援哪些備份類型。</span><span class="sxs-lookup"><span data-stu-id="8d31e-257">Writers communicate what backup types are supported through the requester's calling [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).</span></span> <span data-ttu-id="8d31e-258">TestWriter 根項目包含每一種備份類型的屬性，以指出支援。</span><span class="sxs-lookup"><span data-stu-id="8d31e-258">The TestWriter root element contains attributes for each backup type to indicate support.</span></span> <span data-ttu-id="8d31e-259">這些屬性是 supportsCopy、supportsDifferential、supportsIncremental 和 supportsLog。</span><span class="sxs-lookup"><span data-stu-id="8d31e-259">These attributes are supportsCopy, supportsDifferential, supportsIncremental, and supportsLog.</span></span> <span data-ttu-id="8d31e-260">若要指出對特定備份類型的支援，請將對應的屬性設定為 [是]。</span><span class="sxs-lookup"><span data-stu-id="8d31e-260">To indicate support for a particular backup type, set the corresponding attribute to "yes".</span></span>

<span data-ttu-id="8d31e-261">如果要求者將備份類型設定為寫入器不支援的備份類型，寫入器會在 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)期間記下這項事實，否則會正常運作。</span><span class="sxs-lookup"><span data-stu-id="8d31e-261">If the requester sets the backup type to a backup type that is not supported by the writer, the writer will note this fact during [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), but otherwise work correctly.</span></span>

## <a name="indicating-the-file-backup-type"></a><span data-ttu-id="8d31e-262">指出檔案備份類型</span><span class="sxs-lookup"><span data-stu-id="8d31e-262">Indicating the File Backup Type</span></span>

<span data-ttu-id="8d31e-263">[**IVssWMFiledesc：： GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)方法會將位元遮罩傳回給要求者，指出應如何備份檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-263">The [**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) method returns a bitmask to the requester indicating how a file should be backed up.</span></span> <span data-ttu-id="8d31e-264">這會指出在特定類型的備份期間是否需要檔案，以及在特定類型的備份期間是否需要進行陰影複製。</span><span class="sxs-lookup"><span data-stu-id="8d31e-264">This will indicate whether a file is required or not required during specific types of backup, and also whether a shadow copy is required during specific types of backup.</span></span> <span data-ttu-id="8d31e-265">在 [備份複雜存放區](requestor-role-in-backing-up-complex-stores.md)的檔要求者角色中，會以更高的長度解釋此位元遮罩中的備份類型。</span><span class="sxs-lookup"><span data-stu-id="8d31e-265">The backup types in this bitmask are explained at greater length in the document [Requester Role in Backing Up Complex Stores](requestor-role-in-backing-up-complex-stores.md).</span></span>

<span data-ttu-id="8d31e-266">在測試寫入器中，會藉由設定每個 ComponentFile 專案中的屬性來指定此位元遮罩的元素。</span><span class="sxs-lookup"><span data-stu-id="8d31e-266">In the Test Writer, the elements of this bitmask are specified by setting attributes in each ComponentFile element.</span></span> <span data-ttu-id="8d31e-267">FullBackupRequired、diffBackupRequired、incBackupRequired 和 logBackupRequired 屬性會指定何時需要備份檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-267">The fullBackupRequired, diffBackupRequired, incBackupRequired, and logBackupRequired attributes specify when a file needs to be backed up.</span></span> <span data-ttu-id="8d31e-268">FullSnapshotRequired、diffSnapshotRequired、incSnapshotRequired 和 logSnapshotRequired 屬性會指定何時必須從磁片區的陰影複本備份檔， (而不是從原始磁片區) 。</span><span class="sxs-lookup"><span data-stu-id="8d31e-268">The fullSnapshotRequired, diffSnapshotRequired, incSnapshotRequired, and logSnapshotRequired attributes specify when a file must be backed up from a shadow copy of a volume (and never from the original volume).</span></span> <span data-ttu-id="8d31e-269">所有這些值的預設值為 [是]，表示必須一律備份檔案，而且必須從磁片區的陰影複本備份。</span><span class="sxs-lookup"><span data-stu-id="8d31e-269">The default for all of these values is "yes", indicating that a file must always be backed up and must be backed up from a shadow copy of a volume.</span></span>

## <a name="adding-partial-files"></a><span data-ttu-id="8d31e-270">新增部分檔案</span><span class="sxs-lookup"><span data-stu-id="8d31e-270">Adding Partial Files</span></span>

<span data-ttu-id="8d31e-271">在處理 [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)期間，寫入器有機會將部分檔案新增至每個元件。</span><span class="sxs-lookup"><span data-stu-id="8d31e-271">During the processing of [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), a writer has a chance to add partial files to each component.</span></span> <span data-ttu-id="8d31e-272">這些部分檔案會使用 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)來回報。</span><span class="sxs-lookup"><span data-stu-id="8d31e-272">These partial files are reported using [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile).</span></span> <span data-ttu-id="8d31e-273">您可以藉由在元件專案中指定 PartialFile 子項目，將測試編寫器設定為加入部分檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-273">The Test Writer can be configured to add partial files by specifying PartialFile subelements in a Component element.</span></span>

<span data-ttu-id="8d31e-274">以下是具有兩個 PartialFile 子項目的元件元素範例：</span><span class="sxs-lookup"><span data-stu-id="8d31e-274">Here is an example of a Component element that has two PartialFile subelements:</span></span>

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <PartialFile path="c:\files"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
        <PartialFile path="c:\files2"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
    </Component>
```

<span data-ttu-id="8d31e-275">只有部分符合現有 ComponentFile (的部分檔案，與範例中的第一個部分檔案相同) 或在與現有 ComponentFile (相同的磁片區上的新部分檔案（如同在第二個部分檔案) 應該以此方式指定）。</span><span class="sxs-lookup"><span data-stu-id="8d31e-275">Only partial files that partially match an existing ComponentFile (as in the first partial file in the example) or new partial files that are on the same volume as an existing ComponentFile (as in the second partial file) should be specified this way.</span></span> <span data-ttu-id="8d31e-276">對於此元件，要求者必須完全備份符合 c： .txt 的所有檔案， \\ \\ \* 但 partial.txt 除外。</span><span class="sxs-lookup"><span data-stu-id="8d31e-276">For this component, the requester must fully back up all files matching c:\\files\\\*.txt except for partial.txt.</span></span> <span data-ttu-id="8d31e-277">接著，要求者必須備份指定的範圍 (其中範圍是位移，後面接著檔案 c： \\ files \\partial.txt 和 c： \\ files2partial.txt 的長度) \\ 。</span><span class="sxs-lookup"><span data-stu-id="8d31e-277">The requester must then back up the specified ranges (where a range is an offset followed by a length) for the files c:\\files\\partial.txt and c:\\files2\\partial.txt.</span></span>

<span data-ttu-id="8d31e-278">如果將寫入器設定為檢查檔案還原，則只會在還原時檢查部分檔案的備份範圍。</span><span class="sxs-lookup"><span data-stu-id="8d31e-278">If the writer is configured to check file restores, only the backed-up ranges of the partial file will be checked at restore time.</span></span> <span data-ttu-id="8d31e-279">檔案其他部分的修改將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="8d31e-279">Modifications to other portions of the file will go unnoticed.</span></span> <span data-ttu-id="8d31e-280">如果設定 TestWriter 根項目的 deletePartialFiles 屬性，則在建立陰影複製之後，會立即從原始磁片區中刪除部分檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-280">If the deletePartialFiles attribute of the TestWriter root element is set, the partial files are deleted from the original volume immediately after the shadow copy is created.</span></span>

## <a name="adding-differenced-files"></a><span data-ttu-id="8d31e-281">新增差異檔案</span><span class="sxs-lookup"><span data-stu-id="8d31e-281">Adding Differenced Files</span></span>

<span data-ttu-id="8d31e-282">在處理 [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)期間，寫入器可以將差異檔案新增至每個元件。</span><span class="sxs-lookup"><span data-stu-id="8d31e-282">During the processing of [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), a writer can add differenced files to each component.</span></span> <span data-ttu-id="8d31e-283">這些差異檔案會使用 [**>ivsscomponent：： GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)來回報。</span><span class="sxs-lookup"><span data-stu-id="8d31e-283">These differenced files are reported using [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile).</span></span> <span data-ttu-id="8d31e-284">您可以設定測試寫入器，藉由在元件專案中指定 DifferencedFile 子項目，來加入差異較差的檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-284">The Test Writer can be configured to add differenced files by specifying DifferencedFile subelements in a Component element.</span></span>

<span data-ttu-id="8d31e-285">以下是具有兩個 DifferencedFile 子項目的元件元素範例：</span><span class="sxs-lookup"><span data-stu-id="8d31e-285">Here is an example of a Component element that has two DifferencedFile subelements:</span></span>

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <DifferencedFile path="c:\files"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
        <DifferencedFile path="c:\files2"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
    </Component>
```

<span data-ttu-id="8d31e-286">與部分檔案不同的是，差異檔案絕不會部分符合 ComponentFile 規格。</span><span class="sxs-lookup"><span data-stu-id="8d31e-286">Unlike partial files, differenced files should never partially match a ComponentFile specification.</span></span> <span data-ttu-id="8d31e-287">DifferencedFile 元素中的檔案規格應該完全符合 ComponentFile (，就像範例) 的第一個差異檔案中一樣，否則它不應該完全相符，而是在 ComponentFile (所參考的磁片區上，如同第二個差異檔案) 。</span><span class="sxs-lookup"><span data-stu-id="8d31e-287">The file specification in a DifferencedFile element should either exactly match a ComponentFile (as in the first differenced file in the example) or it should not match it at all, but be on a volume that is referenced in a ComponentFile (as in the second differenced file).</span></span> <span data-ttu-id="8d31e-288">日期和時間值應該相對於本地時區，但在回報給要求者之前，將會轉換為 GMT。</span><span class="sxs-lookup"><span data-stu-id="8d31e-288">The date and time values should be relative to the local time zone, but they will be converted to GMT before being reported to the requester.</span></span> <span data-ttu-id="8d31e-289">在此範例中，只會備份符合 c： \\ files \\ \* .txt 或 c： \\ files2 \\ \* 的檔案，該檔案會在1/22/2003:12:44:17 之後進行修改。</span><span class="sxs-lookup"><span data-stu-id="8d31e-289">In the example, only files matching c:\\files\\\*.txt or c:\\files2\\\*.txt that have been modified since 1/22/2003:12:44:17 will be backed up.</span></span>

<span data-ttu-id="8d31e-290">如果測試寫入器設定為檢查檔案還原，則只會檢查修改過的檔案進行還原。</span><span class="sxs-lookup"><span data-stu-id="8d31e-290">If the Test Writer is configured to check file restores, only the modified files will be checked for restore.</span></span> <span data-ttu-id="8d31e-291">如果設定 TestWriter 根項目的 deleteDifferencedFiles 屬性，就會在建立陰影複製後立即從原始磁片區中刪除差異的檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-291">If the deleteDifferencedFiles attribute of the TestWriter root element is set, the differenced files are deleted from the original volume immediately after the shadow copy is created.</span></span>

## <a name="new-targets"></a><span data-ttu-id="8d31e-292">新目標</span><span class="sxs-lookup"><span data-stu-id="8d31e-292">New Targets</span></span>

<span data-ttu-id="8d31e-293">某些寫入器可讓要求者告知已選擇新位置來還原某些檔案。</span><span class="sxs-lookup"><span data-stu-id="8d31e-293">Certain writers allow the requester to inform them that a new location has been chosen to restore certain files to.</span></span> <span data-ttu-id="8d31e-294">寫入器表示它支援此模式，做為 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)所傳回之位元遮罩的一部分。</span><span class="sxs-lookup"><span data-stu-id="8d31e-294">The writer indicates that it supports this mode as part of the bitmask returned by [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).</span></span> <span data-ttu-id="8d31e-295">依預設，測試寫入器一律支援新目標。</span><span class="sxs-lookup"><span data-stu-id="8d31e-295">By default, the Test Writer always supports new targets.</span></span> <span data-ttu-id="8d31e-296">將 TestWriter 根項目中的 supportsNewTarget 屬性設定為 "no"，即可停用這項支援。</span><span class="sxs-lookup"><span data-stu-id="8d31e-296">This support can be disabled by setting the supportsNewTarget attribute in the TestWriter root element to "no".</span></span>

<span data-ttu-id="8d31e-297">如果寫入器支援新的目標，要求者可以藉由呼叫 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)，通知寫入器的新目標。</span><span class="sxs-lookup"><span data-stu-id="8d31e-297">If a writer supports new targets, the requester can inform the writer of new targets by calling [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).</span></span> <span data-ttu-id="8d31e-298">然後，寫入器會檢查新的目標位置，以確認還原，而不是原始的位置。</span><span class="sxs-lookup"><span data-stu-id="8d31e-298">The writer will then check the new target location to verify restore rather than the original location.</span></span>

## <a name="more-information"></a><span data-ttu-id="8d31e-299">相關資訊</span><span class="sxs-lookup"><span data-stu-id="8d31e-299">More Information</span></span>

<span data-ttu-id="8d31e-300">測試寫入器支援這裡未描述的更多設定選項。</span><span class="sxs-lookup"><span data-stu-id="8d31e-300">The Test Writer supports more configuration options that are not described here.</span></span> <span data-ttu-id="8d31e-301">測試編寫器所有設定功能的完整架構，都是在 `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` (for 64 位 windows) 和 `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` 32 位 windows)  (的 swriter.xml 中指定的。</span><span class="sxs-lookup"><span data-stu-id="8d31e-301">The full schema for all of the configuration capabilities of the Test Writer is specified in swriter.xml in `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` (for 64-bit Windows) and `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (for 32-bit Windows).</span></span> <span data-ttu-id="8d31e-302">這個檔案包含一個 XML 架構，可完整描述組成設定檔的所有元素和屬性。</span><span class="sxs-lookup"><span data-stu-id="8d31e-302">This file contains an XML schema that completely describes all of the elements and attributes that make up a configuration file.</span></span> <span data-ttu-id="8d31e-303">在此檔案中的每個專案和每個屬性都會以描述，說明文件該元素或屬性的用途。</span><span class="sxs-lookup"><span data-stu-id="8d31e-303">Each element and each attribute in this file is commented with a description that documents that element's or attribute's use.</span></span>

 

 




