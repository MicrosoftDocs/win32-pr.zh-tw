---
title: 建立多會話光碟
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: 深入瞭解：建立多會話光碟
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db17b8a16f46797fc0f6de2bf94850e3b3039bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469304"
---
# <a name="creating-a-multisession-disc"></a><span data-ttu-id="5bc79-103">建立多會話光碟</span><span class="sxs-lookup"><span data-stu-id="5bc79-103">Creating a Multisession Disc</span></span>

<span data-ttu-id="5bc79-104">[映射主控 API](about-imapi.md) (imapi.exe) 支援新增和移除下列多會話光碟類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="5bc79-104">The [Image Mastering API](about-imapi.md) (IMAPI) supports the addition and removal of files to, or from, the following multisession disc types:</span></span>

-   <span data-ttu-id="5bc79-105">CD-R/CD-RW</span><span class="sxs-lookup"><span data-stu-id="5bc79-105">CD-R/CD-RW</span></span>
-   <span data-ttu-id="5bc79-106">Single-Layer DVD + R/DVD-R-R</span><span class="sxs-lookup"><span data-stu-id="5bc79-106">Single-Layer DVD+R/DVD-R</span></span>
-   <span data-ttu-id="5bc79-107">DVD + R 雙重圖層</span><span class="sxs-lookup"><span data-stu-id="5bc79-107">DVD+R Dual Layer</span></span>
-   <span data-ttu-id="5bc79-108">BD-R</span><span class="sxs-lookup"><span data-stu-id="5bc79-108">BD-R</span></span>
-   <span data-ttu-id="5bc79-109">僅限 DVD-ROM/DVD + RW (**Windows 7**) </span><span class="sxs-lookup"><span data-stu-id="5bc79-109">DVD-RW/DVD+RW (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="5bc79-110">**僅 (Windows 7** 的 DVD RAM) </span><span class="sxs-lookup"><span data-stu-id="5bc79-110">DVD-RAM (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="5bc79-111">只有) 的 BD (**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="5bc79-111">BD-RE (**Windows 7 Only**)</span></span>

<span data-ttu-id="5bc79-112">使用 IMAPI.EXE 建立多會話光碟包含下列步驟。</span><span class="sxs-lookup"><span data-stu-id="5bc79-112">Creation of a multisession disc using IMAPI consists of the following steps.</span></span> <span data-ttu-id="5bc79-113">這些記載的每個步驟都包含最後一節所提供完整 Visual Basic 腳本範例的相關部分。</span><span class="sxs-lookup"><span data-stu-id="5bc79-113">Each of these documented steps contains the relevant portion of the complete Visual Basic script example provided in the final section.</span></span>

## <a name="initializing-the-disc-recorder"></a><span data-ttu-id="5bc79-114">正在初始化光碟錄製器</span><span class="sxs-lookup"><span data-stu-id="5bc79-114">Initializing the Disc Recorder</span></span>

<span data-ttu-id="5bc79-115">在裝置初始化之前， **MsftDiscMaster2** 物件會提供系統上光學裝置的列舉。</span><span class="sxs-lookup"><span data-stu-id="5bc79-115">Prior to device initialization, the **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="5bc79-116">[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)介面可讓您存取此裝置列舉，以加速適當錄製裝置的位置。</span><span class="sxs-lookup"><span data-stu-id="5bc79-116">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to this device enumeration to facilitate the location of the appropriate recording device.</span></span> <span data-ttu-id="5bc79-117">當您在電腦上新增或移除光學裝置時， **MsftDiscMaster2** 物件也會提供事件通知。</span><span class="sxs-lookup"><span data-stu-id="5bc79-117">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or removed from a machine.</span></span>

<span data-ttu-id="5bc79-118">找出光碟錄製器並取出指派給它的識別碼之後，請建立新的 **MsftDiscMaster2** 物件，並使用特定的裝置識別碼將錄製器初始化。</span><span class="sxs-lookup"><span data-stu-id="5bc79-118">After locating an optical recorder and retrieving the ID assigned to it, create a new **MsftDiscMaster2** object and initialize the recorder using the specific device ID.</span></span>

<span data-ttu-id="5bc79-119">[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)介面可讓您存取基本的裝置資訊，例如廠商識別碼、產品識別碼、產品修訂，以及退出媒體或關閉紙匣的方法。</span><span class="sxs-lookup"><span data-stu-id="5bc79-119">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to basic device information such as vendor ID, product ID, product revision, as well as the methods to eject media or close the tray.</span></span>

> [!Note]  
> <span data-ttu-id="5bc79-120">下列範例中宣告的其他常數和維度，稍後會在本檔的最後一節中的完整範例腳本中使用。</span><span class="sxs-lookup"><span data-stu-id="5bc79-120">The additional constants and dimensions declared in the following sample are used later in the complete sample script located in the final section of this document.</span></span> <span data-ttu-id="5bc79-121">初始化光碟錄製器的動作不需要這些元素。</span><span class="sxs-lookup"><span data-stu-id="5bc79-121">These elements are not required for the act of initializing a disc recorder.</span></span>

 


```VB
' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a><span data-ttu-id="5bc79-122">建立資料寫入器外掛程式</span><span class="sxs-lookup"><span data-stu-id="5bc79-122">Creating a Data Writer</span></span>

<span data-ttu-id="5bc79-123">_ *MsftDiscFormat2Data*\* 物件提供撰寫方法、其屬性，以及媒體專屬屬性。</span><span class="sxs-lookup"><span data-stu-id="5bc79-123">The _ *MsftDiscFormat2Data*\* object provides the writing method, its properties, as well as the media-specific properties.</span></span> <span data-ttu-id="5bc79-124">[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)介面會提供此物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="5bc79-124">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to this object.</span></span>

<span data-ttu-id="5bc79-125">光碟錄製器會使用 [**IDiscFormat2Data：:p 的操作人員 \_ 錄製**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) 器屬性，系結至格式寫入器。</span><span class="sxs-lookup"><span data-stu-id="5bc79-125">The disc recorder binds to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="5bc79-126">將錄製器系結至格式寫入器之後，您可以在使用 [**IDiscFormat2Data：： write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) 方法將結果影像寫入光碟之前，先執行媒體和寫入特定的屬性查詢。</span><span class="sxs-lookup"><span data-stu-id="5bc79-126">After the recorder is bound to the format writer, media and write-specific property queries can be performed prior to writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

> [!Note]  
> <span data-ttu-id="5bc79-127">下列範例程式碼中所指定的用戶端名稱字串應該針對特定應用程式適當地調整。</span><span class="sxs-lookup"><span data-stu-id="5bc79-127">The client name string specified in the sample code below should be adjusted as appropriate for the specific application.</span></span>

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a><span data-ttu-id="5bc79-128">建立檔案系統物件</span><span class="sxs-lookup"><span data-stu-id="5bc79-128">Creating the File System Object</span></span>

<span data-ttu-id="5bc79-129">若要記錄新的會話，必須先產生燒錄映射。</span><span class="sxs-lookup"><span data-stu-id="5bc79-129">In order to record a new session, a burn image must be generated for it first.</span></span> <span data-ttu-id="5bc79-130">**ISO9660**、 **Joliet** 和 **UDF** 格式的燒錄映射包含個別檔案和目錄的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5bc79-130">A burn image for **ISO9660**, **Joliet** and **UDF** formats consist of file systems of individual files and directories.</span></span> <span data-ttu-id="5bc79-131">**MsftFileSystemImage** 物件是檔案系統物件，其中包含要放在光學媒體上的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="5bc79-131">The **MsftFileSystemImage** object is the file system object that contains the files and directories to be placed on the optical media.</span></span> <span data-ttu-id="5bc79-132">[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)介面提供檔案系統物件和設定的存取權。</span><span class="sxs-lookup"><span data-stu-id="5bc79-132">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a><span data-ttu-id="5bc79-133">匯入檔案系統</span><span class="sxs-lookup"><span data-stu-id="5bc79-133">Importing a File System</span></span>

<span data-ttu-id="5bc79-134">在繼續之前，請檢查 [**IDiscFormat2：： get \_ MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) 屬性，以確定光碟不是空白的。</span><span class="sxs-lookup"><span data-stu-id="5bc79-134">Before proceeding, ensure that the disc is not blank by checking the [**IDiscFormat2::get\_MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) property.</span></span>

<span data-ttu-id="5bc79-135">建立 **MsftFileSystemImage** 物件之後，您應該在呼叫 [**IFileSystemImage：： ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem)或 [**IFileSystemImage：： ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem)方法之前，先初始化 [**IFileSystemImage：:p \_**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) ] 屬性，以便從上次記錄的會話匯入檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5bc79-135">After creating the **MsftFileSystemImage** object, the [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property should be initialized prior to a call to either the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) or [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method to import the file system from the last recorded session.</span></span> <span data-ttu-id="5bc79-136">這些方法會使用描述先前記錄之檔案和目錄的資訊，自動填入 **MsftFileSystemImage** 物件。</span><span class="sxs-lookup"><span data-stu-id="5bc79-136">These methods will automatically populate the **MsftFileSystemImage** object with information describing the previously recorded files and directories.</span></span>

> [!Note]  
> <span data-ttu-id="5bc79-137">[**IFileSystemImage：:p 的 \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces)屬性通常會使用資料寫入器透過 [**IDiscFormat2Data：： get \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces)屬性提供的多會話介面進行初始化。</span><span class="sxs-lookup"><span data-stu-id="5bc79-137">The [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property is typically initialized with the multisession interfaces provided by the data writer via the [**IDiscFormat2Data::get\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) property.</span></span>

 

<span data-ttu-id="5bc79-138">如果 IMAPI.EXE 不支援目前所插入之媒體的多會話，或是因為其他 (原因而無法附加媒體，則嘗試將 **IFileSystemImage：:p 的 \_ MultisessionInterfaces** 屬性設定為失敗，例如，因為它已) 關閉。</span><span class="sxs-lookup"><span data-stu-id="5bc79-138">Attempts to set the **IFileSystemImage::put\_MultisessionInterfaces** property will fail if IMAPI does not support multisession for the currently inserted media or the media cannot be appended for some other reason (e.g. because it is closed).</span></span>

<span data-ttu-id="5bc79-139">如果先前的燒錄會話包含一個以上的檔案系統類型， [**IFileSystemImage：： ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) 方法將會從目前最先進的檔案系統類型匯入資訊。</span><span class="sxs-lookup"><span data-stu-id="5bc79-139">If the previous burn session contained more than one file system type, the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method will import information from the most advanced file system type present.</span></span> <span data-ttu-id="5bc79-140">例如，在本主題所提供的範例中，UDF 是匯入的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5bc79-140">For example, in the example provided in this topic, UDF is the imported file system.</span></span> <span data-ttu-id="5bc79-141">不過，使用 [**IFileSystemImage：： ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) 方法可讓您選取要匯入的特定檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5bc79-141">However, use of the [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method allows the specific selection of the file system to import.</span></span>

> [!Note]  
> <span data-ttu-id="5bc79-142">[**IFileSystemImage：： IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc)方法可以用來判斷光碟上可用的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="5bc79-142">The [**IFileSystemImage::IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) method can be used to determine which file systems are available on the disc.</span></span>

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a><span data-ttu-id="5bc79-143">新增或移除檔案系統的檔案</span><span class="sxs-lookup"><span data-stu-id="5bc79-143">Adding or Removing Files to the File System</span></span>

<span data-ttu-id="5bc79-144">建立檔案系統物件並從先前的會話匯入檔案系統之後，請呼叫 [**IFileSystemImage：： CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) 和 [**IFileSystemImage：： CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) 方法，分別建立新的檔案和目錄物件。</span><span class="sxs-lookup"><span data-stu-id="5bc79-144">After creating the file system object and importing the file system from the previous session, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create new file and directory objects, respectively.</span></span> <span data-ttu-id="5bc79-145">檔案和目錄物件會提供檔案和目錄的特定詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5bc79-145">The file and directory objects provide specific details about the files and directories.</span></span> <span data-ttu-id="5bc79-146">或者，目錄物件的 [**IFsiDirectoryItem：： AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) 方法（透過 [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) 介面表示）可以用來從另一個存放裝置新增現有的檔案和目錄， (也就是硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="5bc79-146">Alternatively, the [**IFsiDirectoryItem::AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) method of a directory object, represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface, can be used to add existing files and directories from another storage device (i.e. a hard drive).</span></span>

<span data-ttu-id="5bc79-147">適用于 [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) 的事件處理常式更新方法會識別目前新增至檔案系統映射的檔案、已複製的磁區數目，以及要複製的磁區總數。</span><span class="sxs-lookup"><span data-stu-id="5bc79-147">The event handler update method available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifies the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="5bc79-148">若要從檔案系統中移除現有的檔案和目錄，請針對透過 [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem)介面表示的目錄物件，使用 [**IFsiDirectoryItem：： remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove)和 [**IFsiDirectoryItem：： RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree)方法。</span><span class="sxs-lookup"><span data-stu-id="5bc79-148">To remove existing files and directories from the file system, use the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods of the directory objects represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface.</span></span> <span data-ttu-id="5bc79-149">[**IFileSystemImage：： get \_ 根**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root)屬性是用來取得檔案系統根目錄的指標，以及 **IFsiDirectoryItem** 介面，以跨越目錄樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="5bc79-149">The [**IFileSystemImage::get\_Root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) property is used to get a pointer to the root directory of the file system and the **IFsiDirectoryItem** interface to traverse through the directory tree.</span></span>

> [!Note]  
> <span data-ttu-id="5bc79-150">透過 [**IFsiDirectoryItem：： Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) 和 [**IFsiDirectoryItem：： RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) 方法移除的檔案和目錄，不會實際從光碟中移除，而 advanced software 可以輕鬆地復原已刪除的資訊。</span><span class="sxs-lookup"><span data-stu-id="5bc79-150">Files and directories removed via the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods are not physically removed from the disc, and advanced software can easily recover the deleted information.</span></span>

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a><span data-ttu-id="5bc79-151">建立檔案系統映射</span><span class="sxs-lookup"><span data-stu-id="5bc79-151">Constructing a File System Image</span></span>

<span data-ttu-id="5bc79-152">最後一個步驟是呼叫 [**IFileSystemImage：： CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) 來建立燒錄影像的資料流程，並透過 [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) 介面提供其存取權。</span><span class="sxs-lookup"><span data-stu-id="5bc79-152">The final step is to call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream for the burn image and provide access to it through the [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) interface.</span></span> <span data-ttu-id="5bc79-153">此資料流程可以直接提供給 [**IDiscFormat2Data：： Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) 方法，或儲存至檔案以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="5bc79-153">This data stream can either be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a><span data-ttu-id="5bc79-154">範例摘要</span><span class="sxs-lookup"><span data-stu-id="5bc79-154">Example Summary</span></span>

<span data-ttu-id="5bc79-155">下列 Visual Basic 腳本範例顯示如何使用 IMAPI.EXE 物件來建立多個多會話光碟。</span><span class="sxs-lookup"><span data-stu-id="5bc79-155">The following Visual Basic script example shows how to use IMAPI objects to create multisession discs.</span></span> <span data-ttu-id="5bc79-156">此範例會建立新的會話，並將目錄新增至光碟。為了簡單起見，程式碼不會執行廣泛的錯誤檢查，並假設下列各項：</span><span class="sxs-lookup"><span data-stu-id="5bc79-156">The example creates a new session and adds a directory to the disc. For the sake of simplicity, the code does not perform extensive error checking, and assumes the following:</span></span>

-   <span data-ttu-id="5bc79-157">系統上已安裝相容的光碟裝置。</span><span class="sxs-lookup"><span data-stu-id="5bc79-157">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="5bc79-158">光碟裝置是系統上的第一個磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5bc79-158">The disc device is the first drive on the system.</span></span>
-   <span data-ttu-id="5bc79-159">光碟裝置中會插入相容的光碟。</span><span class="sxs-lookup"><span data-stu-id="5bc79-159">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="5bc79-160">要新增至光碟的檔案位於 "g： \\ burndir"。</span><span class="sxs-lookup"><span data-stu-id="5bc79-160">Files to add to the disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="5bc79-161">您可以在腳本中加入其他功能，例如廣泛的錯誤檢查、裝置和媒體相容性、事件通知，以及磁片上的可用空間計算。</span><span class="sxs-lookup"><span data-stu-id="5bc79-161">Additional functionality such as extensive error checking, device and media compatibility, event notification, and calculation of free space on the disc can be added to the script.</span></span>


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="5bc79-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="5bc79-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bc79-163">使用 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="5bc79-163">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="5bc79-164">_ *IStream*\*</span><span class="sxs-lookup"><span data-stu-id="5bc79-164">_ *IStream*\*</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="5bc79-165">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="5bc79-165">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="5bc79-166">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="5bc79-166">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="5bc79-167">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="5bc79-167">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
