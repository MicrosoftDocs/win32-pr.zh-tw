---
description: 標籤是指派給磁片區（通常是由使用者使用）的易記名稱，可讓您更容易辨識。 磁片區可以有標籤、磁碟機號、兩者或兩者皆有。 若要設定磁片區的標籤，請使用 SetVolumeLabel 函數。
ms.assetid: f640f42d-a703-4e2e-a6d3-09cbe989cd11
title: 命名磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6435b6b5c7283cf2fb9a98951698f79646dfdffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851199"
---
# <a name="naming-a-volume"></a><span data-ttu-id="e1013-105">命名磁片區</span><span class="sxs-lookup"><span data-stu-id="e1013-105">Naming a Volume</span></span>

<span data-ttu-id="e1013-106">標籤是指派給磁片區（通常是由使用者使用）的易記名稱，可讓您更容易辨識。</span><span class="sxs-lookup"><span data-stu-id="e1013-106">A label is a user-friendly name that is assigned to a volume, usually by an end user, to make it easier to recognize.</span></span> <span data-ttu-id="e1013-107">磁片區可以有標籤、磁碟機號、兩者或兩者皆有。</span><span class="sxs-lookup"><span data-stu-id="e1013-107">A volume can have a label, a drive letter, both, or neither.</span></span> <span data-ttu-id="e1013-108">若要設定磁片區的標籤，請使用 [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) 函數。</span><span class="sxs-lookup"><span data-stu-id="e1013-108">To set the label for a volume, use the [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) function.</span></span>

<span data-ttu-id="e1013-109">有幾個因素可能會讓您難以使用磁碟機號和標籤來識別特定磁片區。</span><span class="sxs-lookup"><span data-stu-id="e1013-109">Several factors can make it difficult to identify specific volumes using only drive letters and labels.</span></span> <span data-ttu-id="e1013-110">其中一個是磁片區不需要有磁碟機號或標籤。</span><span class="sxs-lookup"><span data-stu-id="e1013-110">One is that a volume is not required to have a drive letter or a label.</span></span> <span data-ttu-id="e1013-111">另一種方式是讓兩個不同的磁片區有相同的標籤，而不是由磁碟機號區別。</span><span class="sxs-lookup"><span data-stu-id="e1013-111">Another is that two different volumes can have the same label, which makes them indistinguishable except by drive letter.</span></span> <span data-ttu-id="e1013-112">第三個因素是在電腦上新增和移除磁片區時，可以變更磁碟機號指派。</span><span class="sxs-lookup"><span data-stu-id="e1013-112">A third factor is that drive letter assignments can change as volumes are added to and removed from the computer.</span></span>

<span data-ttu-id="e1013-113">為了解決這個問題，作業系統使用磁片區 *GUID 路徑* 來識別磁片區。</span><span class="sxs-lookup"><span data-stu-id="e1013-113">To solve this problem, the operating system uses *volume GUID paths* to identify volumes.</span></span> <span data-ttu-id="e1013-114">以下是這種形式的字串：</span><span class="sxs-lookup"><span data-stu-id="e1013-114">These are strings of this form:</span></span>

<span data-ttu-id="e1013-115">"\\\\?\\Volume {*GUID*} \\ "</span><span class="sxs-lookup"><span data-stu-id="e1013-115">"\\\\?\\Volume{*GUID*}\\"</span></span>

<span data-ttu-id="e1013-116">其中 *guid* 是識別磁片區 (guid) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e1013-116">where *GUID* is a globally unique identifier (GUID) that identifies the volume.</span></span>

<span data-ttu-id="e1013-117">磁片區 GUID 路徑有時稱為 *唯一磁片區名稱*，因為磁片區 guid 路徑只能參考一個磁片區。</span><span class="sxs-lookup"><span data-stu-id="e1013-117">A volume GUID path is sometimes referred to as a *unique volume name*, because a volume GUID path can refer only to one volume.</span></span> <span data-ttu-id="e1013-118">不過，因為磁片區可以有一個以上的磁片區 GUID 路徑，所以此詞彙很誤導。</span><span class="sxs-lookup"><span data-stu-id="e1013-118">However, this term is misleading, because a volume can have more than one volume GUID path.</span></span>

<span data-ttu-id="e1013-119">" \\ \\ ？ \\ " 前置詞會停用路徑剖析，而不會被視為路徑的一部分。</span><span class="sxs-lookup"><span data-stu-id="e1013-119">The "\\\\?\\" prefix disables path parsing and is not considered to be part of the path.</span></span> <span data-ttu-id="e1013-120">如需 "？" 前置詞的詳細資訊 \\ \\ \\ ，請參閱[命名檔案或目錄](naming-a-file.md)。</span><span class="sxs-lookup"><span data-stu-id="e1013-120">For more information about the "\\\\?\\" prefix, see [Naming a File or Directory](naming-a-file.md).</span></span>

<span data-ttu-id="e1013-121">使用具有 " \\ \\ ？" 前置詞的磁片區 GUID 路徑時，您必須指定完整路徑 \\ 。</span><span class="sxs-lookup"><span data-stu-id="e1013-121">You must specify full paths when using volume GUID paths with the "\\\\?\\" prefix.</span></span>

<span data-ttu-id="e1013-122">*裝載的資料夾* 是一個磁片區上的資料夾與另一個磁片區之間的關聯，因此可以使用資料夾路徑來存取磁片區。</span><span class="sxs-lookup"><span data-stu-id="e1013-122">A *mounted folder* is an association between a folder on one volume and another volume, so that the folder path can be used to access the volume.</span></span> <span data-ttu-id="e1013-123">例如，如果您使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式來建立將磁片區 "d： \\ " 與資料夾 "C： MountD" 產生關聯的已掛接資料夾 \\ \\ ，則可以使用任一路徑 ( "d： \\ " 或 "C： \\ MountD \\ " ) 來存取磁片區 "d： \\ "。</span><span class="sxs-lookup"><span data-stu-id="e1013-123">For example, if you use the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function to create a mounted folder that associates the volume "D:\\" with the folder "C:\\MountD\\", you can then use either path ("D:\\" or "C:\\MountD\\") to access the volume "D:\\".</span></span>

<span data-ttu-id="e1013-124">*磁片區掛接點* 是可用於存取磁片區的任何使用者模式路徑。</span><span class="sxs-lookup"><span data-stu-id="e1013-124">A *volume mount point* is any user-mode path that can be used to access a volume.</span></span> <span data-ttu-id="e1013-125">磁片區掛接點有三種類型：</span><span class="sxs-lookup"><span data-stu-id="e1013-125">There are three types of volume mount points:</span></span>

-   <span data-ttu-id="e1013-126">磁碟機號，例如 "C： \\ "。</span><span class="sxs-lookup"><span data-stu-id="e1013-126">A drive letter, for example, "C:\\".</span></span>
-   <span data-ttu-id="e1013-127">磁片區 GUID 路徑，例如 " \\ \\ ？ \\磁片區 {26a21bda-a627-11d7-9931-806e6f6e6963} \\ "。</span><span class="sxs-lookup"><span data-stu-id="e1013-127">A volume GUID path, for example, "\\\\?\\Volume{26a21bda-a627-11d7-9931-806e6f6e6963}\\".</span></span>
-   <span data-ttu-id="e1013-128">裝載的資料夾，例如 "C： \\ MountD \\ "。</span><span class="sxs-lookup"><span data-stu-id="e1013-128">A mounted folder, for example, "C:\\MountD\\".</span></span>

<span data-ttu-id="e1013-129">將磁片區 GUID 路徑當作輸入參數的所有磁片區和已掛接的資料夾函式都需要尾端的反斜線。</span><span class="sxs-lookup"><span data-stu-id="e1013-129">All volume and mounted folder functions that take a volume GUID path as an input parameter require the trailing backslash.</span></span> <span data-ttu-id="e1013-130">所有會傳回磁片區 GUID 路徑的磁片區和已掛接資料夾函式都會提供尾端的反斜線，但 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式並不會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e1013-130">All volume and mounted folder functions that return a volume GUID path provide the trailing backslash, but this is not the case with the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="e1013-131">您可以藉由呼叫 **CreateFile** 來開啟磁片區，並從您指定的磁片區名稱中省略尾端的反斜線。</span><span class="sxs-lookup"><span data-stu-id="e1013-131">You can open a volume by calling **CreateFile** and omit the trailing backslash from the volume name you specify.</span></span> <span data-ttu-id="e1013-132">**CreateFile** 會以附加的反斜線做為磁片區的根目錄，來處理磁片區 GUID 路徑。</span><span class="sxs-lookup"><span data-stu-id="e1013-132">**CreateFile** processes a volume GUID path with an appended backslash as the root directory of the volume.</span></span>

<span data-ttu-id="e1013-133">當第一次安裝磁片區以及格式化磁片區時，作業系統會將磁片區 GUID 路徑指派給磁片區。</span><span class="sxs-lookup"><span data-stu-id="e1013-133">The operating system assigns a volume GUID path to a volume when the volume is first installed and when the volume is formatted.</span></span> <span data-ttu-id="e1013-134">磁片區和裝載的資料夾功能會使用磁片區 GUID 路徑來存取磁片區。</span><span class="sxs-lookup"><span data-stu-id="e1013-134">The volume and mounted folder functions use volume GUID paths to access volumes.</span></span> <span data-ttu-id="e1013-135">若要取得磁片區的磁片區 GUID 路徑，請使用 [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) 函數。</span><span class="sxs-lookup"><span data-stu-id="e1013-135">To obtain the volume GUID path for a volume, use the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>

<span data-ttu-id="e1013-136">建立掛接的資料夾時，路徑長度可能會是個問題，其會將具有深度目錄樹狀目錄的磁片區與另一個磁片區上的目錄產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e1013-136">Path lengths may be a concern when a mounted folder is created that associates a volume that has a deep directory tree with a directory on another volume.</span></span> <span data-ttu-id="e1013-137">這是因為磁片區的路徑會串連至目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="e1013-137">This is because the path of the volume is concatenated to the path of the directory.</span></span> <span data-ttu-id="e1013-138">全域定義的常數 **最大 \_ 路徑** 會定義路徑可具有的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="e1013-138">The globally defined constant **MAX\_PATH** defines the maximum number of characters a path can have.</span></span> <span data-ttu-id="e1013-139"> (如需 **最大 \_ 路徑** 的詳細資訊，請參閱 [命名檔案或目錄](naming-a-file.md)。 ) 您可以執行下列其中一項動作來避免這個限制：</span><span class="sxs-lookup"><span data-stu-id="e1013-139">(For more information about **MAX\_PATH**, see [Naming a File or Directory](naming-a-file.md).) You can avoid this constraint by doing either of the following:</span></span>

-   <span data-ttu-id="e1013-140">請依磁片區 GUID 路徑來參考磁片區。</span><span class="sxs-lookup"><span data-stu-id="e1013-140">Refer to volumes by their volume GUID paths.</span></span>
-   <span data-ttu-id="e1013-141">使用 Unicode (W) 檔案函式版本，其支援 \\ \\ ？前置詞 \\ 。</span><span class="sxs-lookup"><span data-stu-id="e1013-141">Use the Unicode (W) versions of file functions, which support the \\\\?\\ prefix.</span></span>

 

 



