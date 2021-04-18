---
description: InstallFiles 動作會將檔案資料表中指定的檔案從來源目錄複寫到目的地目錄。
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: InstallFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983353"
---
# <a name="installfiles-action"></a><span data-ttu-id="36d66-103">InstallFiles 動作</span><span class="sxs-lookup"><span data-stu-id="36d66-103">InstallFiles Action</span></span>

<span data-ttu-id="36d66-104">InstallFiles 動作會將檔案資料表中指定的檔案從來源目錄複寫到目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="36d66-104">The InstallFiles action copies files specified in the File table from the source directory to the destination directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="36d66-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="36d66-105">Sequence Restrictions</span></span>

<span data-ttu-id="36d66-106">InstallFiles 動作必須在 [InstallValidate](installvalidate-action.md) 動作之後，以及任何與檔案相依的動作之前。</span><span class="sxs-lookup"><span data-stu-id="36d66-106">The InstallFiles action must come after the [InstallValidate](installvalidate-action.md) action and before any file-dependent actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="36d66-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="36d66-107">ActionData Messages</span></span>



| <span data-ttu-id="36d66-108">欄位</span><span class="sxs-lookup"><span data-stu-id="36d66-108">Field</span></span> | <span data-ttu-id="36d66-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="36d66-109">Description of action data</span></span>                      |
|-------|-------------------------------------------------|
| <span data-ttu-id="36d66-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="36d66-110">\[1\]</span></span> | <span data-ttu-id="36d66-111">已安裝檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="36d66-111">Identifier of installed file.</span></span>                   |
| <span data-ttu-id="36d66-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="36d66-112">\[6\]</span></span> | <span data-ttu-id="36d66-113">已安裝檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36d66-113">Size of installed file in bytes.</span></span>                |
| <span data-ttu-id="36d66-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="36d66-114">\[9\]</span></span> | <span data-ttu-id="36d66-115">保存已安裝檔案的目錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="36d66-115">Identifier of directory holding installed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="36d66-116">備註</span><span class="sxs-lookup"><span data-stu-id="36d66-116">Remarks</span></span>

<span data-ttu-id="36d66-117">InstallFiles 動作會在 [File 資料表](file-table.md)中指定的檔案上運作。</span><span class="sxs-lookup"><span data-stu-id="36d66-117">The InstallFiles action operates on files specified in the [File table](file-table.md).</span></span> <span data-ttu-id="36d66-118">每個檔案都會根據 [元件資料表](component-table.md)中檔案相關元件的安裝狀態進行安裝。</span><span class="sxs-lookup"><span data-stu-id="36d66-118">Each file is installed based on the installation state of the file's associated component in the [Component table](component-table.md).</span></span> <span data-ttu-id="36d66-119">只有元件的元件會解析為 **msiInstallStatelocal** 狀態時，才有資格進行複製。</span><span class="sxs-lookup"><span data-stu-id="36d66-119">Only those files whose components are resolved to the **msiInstallStatelocal** state are eligible for copying.</span></span>

<span data-ttu-id="36d66-120">InstallFiles 動作會執行檔案資料表的下列資料行。</span><span class="sxs-lookup"><span data-stu-id="36d66-120">The InstallFiles action implements the following columns of the File table.</span></span>

-   <span data-ttu-id="36d66-121">FileName 資料行指定目的檔案名。</span><span class="sxs-lookup"><span data-stu-id="36d66-121">The FileName column specifies the target file name.</span></span>
-   <span data-ttu-id="36d66-122">版本資料行指定檔案版本。</span><span class="sxs-lookup"><span data-stu-id="36d66-122">The Version column specifies the file version.</span></span>
-   <span data-ttu-id="36d66-123">[屬性] 欄指定檔案和安裝屬性旗標位。</span><span class="sxs-lookup"><span data-stu-id="36d66-123">The Attributes column specifies the file and installation attribute flag bits.</span></span>
-   <span data-ttu-id="36d66-124">File 資料行指定唯一的檔案 token。</span><span class="sxs-lookup"><span data-stu-id="36d66-124">The File column specifies the unique file token.</span></span>
-   <span data-ttu-id="36d66-125">FileSize 資料行指定未壓縮的檔案大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="36d66-125">The FileSize column specifies the uncompressed file size in bytes.</span></span>
-   <span data-ttu-id="36d66-126">[語言] 資料行指定檔案語言識別項。</span><span class="sxs-lookup"><span data-stu-id="36d66-126">The Language column specifies the file language identifier.</span></span>
-   <span data-ttu-id="36d66-127">[順序] 資料行指定媒體上的序號。</span><span class="sxs-lookup"><span data-stu-id="36d66-127">The Sequence column specifies the sequence number on media.</span></span>

<span data-ttu-id="36d66-128">InstallFiles 動作會執行元件資料表的下列資料行。</span><span class="sxs-lookup"><span data-stu-id="36d66-128">The InstallFiles action implements the following columns of the Component table.</span></span>

-   <span data-ttu-id="36d66-129">目錄資料 \_ 行指定 [目錄資料表](directory-table.md) 專案的參考。</span><span class="sxs-lookup"><span data-stu-id="36d66-129">The Directory\_ column specifies a reference to a [Directory table](directory-table.md) item.</span></span>
-   <span data-ttu-id="36d66-130">元件資料行指定元件專案的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="36d66-130">The Component column specifies a unique name for the component item.</span></span>

<span data-ttu-id="36d66-131">只有在下列其中一項為真時，才會複製指定的檔案：</span><span class="sxs-lookup"><span data-stu-id="36d66-131">The specified file is copied only if one of the following is true:</span></span>

-   <span data-ttu-id="36d66-132">檔案目前未安裝在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="36d66-132">The file is not currently installed on the local computer.</span></span>
-   <span data-ttu-id="36d66-133">檔案是在本機電腦上，但版本號碼比檔案 [資料表](file-table.md)中的檔案還要低。</span><span class="sxs-lookup"><span data-stu-id="36d66-133">The file is on the local computer but has a lower version number than the file in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="36d66-134">檔案是在本機電腦上，但沒有相關聯的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="36d66-134">The file is on the local computer, but there is no associated version number.</span></span>

<span data-ttu-id="36d66-135">每個要複製之檔案的來原始目錄都是由 sourceMode 所決定，而這會依媒體資料表的 [封包] 資料行中的值而定。</span><span class="sxs-lookup"><span data-stu-id="36d66-135">The source directory for each file to be copied is determined by the sourceMode, which in turn depends on the value in the Cabinet column of the Media table.</span></span> <span data-ttu-id="36d66-136">如需來源模式的完整討論，請參閱 [媒體資料表](media-table.md)。</span><span class="sxs-lookup"><span data-stu-id="36d66-136">For a full discussion of the source mode, see the [Media table](media-table.md).</span></span>

<span data-ttu-id="36d66-137">如果要複製之檔案的來原始目錄位於卸載式媒體（例如磁片或 CD-ROM）上，則 InstallFiles 動作會先確認已插入適當的來源媒體，然後再嘗試複製檔案。</span><span class="sxs-lookup"><span data-stu-id="36d66-137">If the source directory for a file to be copied resides on removable media such as a floppy disk or CD-ROM, the InstallFiles action verifies that the proper source media is inserted before attempting to copy the file.</span></span> <span data-ttu-id="36d66-138">InstallFiles 會使用與媒體資料表的 VolumeLabel 資料行中所指定值相符的 [*磁片區卷*](v-gly.md) 標，搜尋相同卸載型別的媒體。</span><span class="sxs-lookup"><span data-stu-id="36d66-138">The InstallFiles searches for media of the same removable type with a [*volume*](v-gly.md) label that matches the value given in the VolumeLabel column of the Media table.</span></span> <span data-ttu-id="36d66-139">如果找到相符的已載入磁片區，則會繼續進行檔案複製程式。</span><span class="sxs-lookup"><span data-stu-id="36d66-139">If a matching mounted volume is found, the file copying process proceeds.</span></span> <span data-ttu-id="36d66-140">如果找不到相符項，對話方塊會要求使用者插入適當的媒體。</span><span class="sxs-lookup"><span data-stu-id="36d66-140">If no match is found, a dialog box requests that the user to insert the proper media.</span></span> <span data-ttu-id="36d66-141">在此情況下，對話方塊會使用媒體資料表的 DiskPrompt 資料行中所找到的媒體名稱做為提示的一部分。</span><span class="sxs-lookup"><span data-stu-id="36d66-141">In this case, the dialog box uses the media name found in the DiskPrompt column of the Media table as part of the prompt.</span></span>

<span data-ttu-id="36d66-142">必須小心，因為 InstallFiles 動作可以刪除原始檔案，而不是取代它。</span><span class="sxs-lookup"><span data-stu-id="36d66-142">Caution must be exercised because the InstallFiles action can delete an original file and not replace it.</span></span> <span data-ttu-id="36d66-143">當 InstallFiles 動作取代較舊的檔案，且使用者選擇忽略錯誤時，就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="36d66-143">This occurs when the InstallFiles action experiences an error while replacing an older file and the user chooses to ignore the error.</span></span> <span data-ttu-id="36d66-144">安裝程式的預設行為是在確定已正確複製新檔案之前，先刪除舊的檔案。</span><span class="sxs-lookup"><span data-stu-id="36d66-144">The default behavior of installer is to delete an old file before ensuring the new file is copied correctly.</span></span>

<span data-ttu-id="36d66-145">如需安裝程式所使用的檔案版本控制規則，請參閱檔案 [版本控制規則](file-versioning-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="36d66-145">For the file versioning rules used by the installer, see [File Versioning Rules](file-versioning-rules.md).</span></span>

 

 



