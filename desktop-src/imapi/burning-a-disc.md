---
title: 燒錄光碟影像
description: 使用 IMAPI.EXE) 燒錄光碟的 (包含下列步驟：建立包含目錄和檔案的檔案系統映射以寫入光碟。設定光碟錄製器來與光學裝置通訊。建立資料寫入器外掛程式，並將映射燒錄至光碟。
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314923"
---
# <a name="burning-a-disc-image"></a><span data-ttu-id="d7095-103">燒錄光碟影像</span><span class="sxs-lookup"><span data-stu-id="d7095-103">Burning a Disc Image</span></span>

<span data-ttu-id="d7095-104">使用 IMAPI.EXE) 燒錄光碟的主控 (包含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="d7095-104">Mastering (burning a disc) using IMAPI consists of the following steps:</span></span>

1.  <span data-ttu-id="d7095-105">建立檔案系統映射，其中包含要寫入光碟的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="d7095-105">Construct a file system image that contains the directories and files to write disc.</span></span>
2.  <span data-ttu-id="d7095-106">[設定光碟錄製](#set-up-a-disc-recorder) 器來與光學裝置通訊。</span><span class="sxs-lookup"><span data-stu-id="d7095-106">[Set up a disc recorder](#set-up-a-disc-recorder) to communicate with the optical device.</span></span>
3.  <span data-ttu-id="d7095-107">[建立資料寫入器外掛程式](#create-a-data-writer-and-write-the-burn-image) ，並將映射燒錄至光碟。</span><span class="sxs-lookup"><span data-stu-id="d7095-107">[Create a data writer](#create-a-data-writer-and-write-the-burn-image) and burn the image to disc.</span></span>

<span data-ttu-id="d7095-108">如需燒錄光碟影像的範例，請參閱 [VBScript 範例](#vbscript-example)。</span><span class="sxs-lookup"><span data-stu-id="d7095-108">For an example that burns a disc image, see [VBScript example](#vbscript-example).</span></span>

## <a name="construct-a-burn-image"></a><span data-ttu-id="d7095-109">建造燒錄映射</span><span class="sxs-lookup"><span data-stu-id="d7095-109">Construct a burn image</span></span>

<span data-ttu-id="d7095-110">燒錄映射是準備寫入光學媒體的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d7095-110">A burn image is a data stream that is ready to be written to optical media.</span></span> <span data-ttu-id="d7095-111">ISO9660、Joliet 和 UDF 格式的燒錄映射包含個別檔案和目錄的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="d7095-111">The burn image for ISO9660, Joliet and UDF formats consists of a file system of individual files and directories.</span></span> <span data-ttu-id="d7095-112">**CFileSystemImage** 物件是檔案系統物件，可保存要放置在光學媒體上的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="d7095-112">The **CFileSystemImage** object is the file system object that holds the files and directories to place on the optical media.</span></span> <span data-ttu-id="d7095-113">[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)介面提供檔案系統物件和設定的存取權。</span><span class="sxs-lookup"><span data-stu-id="d7095-113">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>

<span data-ttu-id="d7095-114">建立檔案系統物件之後，請呼叫 [**IFileSystemImage：： CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) 和 [**IFileSystemImage：： CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) 方法，分別建立檔案和目錄物件。</span><span class="sxs-lookup"><span data-stu-id="d7095-114">After creating the file system object, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create the file and directory objects, respectively.</span></span> <span data-ttu-id="d7095-115">檔案和目錄物件可以用來提供檔案和目錄的特定詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d7095-115">The file and directory objects can be used to provide specific details about the file and directory.</span></span> <span data-ttu-id="d7095-116">適用于 [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) 的事件處理常式方法可以識別目前新增至檔案系統映射的檔案、已複製的磁區數目，以及要複製的磁區總數。</span><span class="sxs-lookup"><span data-stu-id="d7095-116">The event handler methods available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) can identify the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="d7095-117">您可以選擇性地使用 [**IFileSystemImage：:p] \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) 屬性將開機映射附加至檔案系統。</span><span class="sxs-lookup"><span data-stu-id="d7095-117">Optionally, a boot image can be attached to the file system using the [**IFileSystemImage::put\_BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) property.</span></span> <span data-ttu-id="d7095-118">如需範例，請參閱 [新增開機映射](adding-a-boot-image.md)。</span><span class="sxs-lookup"><span data-stu-id="d7095-118">For an example, see [Adding a Boot Image](adding-a-boot-image.md).</span></span>

<span data-ttu-id="d7095-119">最後，呼叫 [**IFileSystemImage：： CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) 來建立資料流程，並透過 [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult)提供存取權。</span><span class="sxs-lookup"><span data-stu-id="d7095-119">Finally, call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream and provides access through [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span></span> <span data-ttu-id="d7095-120">然後，新的資料流程可以直接提供給 [**IDiscFormat2Data：： Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) 方法，或儲存至檔案以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="d7095-120">The new data stream can then be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>

## <a name="set-up-a-disc-recorder"></a><span data-ttu-id="d7095-121">設定光碟錄製器</span><span class="sxs-lookup"><span data-stu-id="d7095-121">Set up a disc recorder</span></span>

<span data-ttu-id="d7095-122">**MsftDiscMaster2** 物件會提供系統上光學裝置的列舉。</span><span class="sxs-lookup"><span data-stu-id="d7095-122">The **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="d7095-123">[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)介面會提供對結果裝置列舉的存取權。</span><span class="sxs-lookup"><span data-stu-id="d7095-123">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to the resultant device enumeration.</span></span> <span data-ttu-id="d7095-124">跨越列舉以找出適當的錄製裝置。</span><span class="sxs-lookup"><span data-stu-id="d7095-124">Traverse the enumerations to locate an appropriate recording device.</span></span> <span data-ttu-id="d7095-125">當您在電腦上新增或刪除光學裝置時， **MsftDiscMaster2** 物件也會提供事件通知。</span><span class="sxs-lookup"><span data-stu-id="d7095-125">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or deleted from a computer.</span></span>

<span data-ttu-id="d7095-126">尋找光碟錄製器並取出其識別碼之後，請建立 **MsftDiscRecorder2** 物件，並使用裝置識別碼將錄製器初始化。</span><span class="sxs-lookup"><span data-stu-id="d7095-126">After finding an optical recorder and retrieving its ID, create an **MsftDiscRecorder2** object and initialize the recorder using the device ID.</span></span> <span data-ttu-id="d7095-127">[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)介面提供了錄製器物件的存取權，以及一些基本的裝置資訊，例如廠商識別碼、產品識別碼、產品修訂，以及用來退出媒體並關閉紙匣的方法。</span><span class="sxs-lookup"><span data-stu-id="d7095-127">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to the recorder object as well as some basic device information such as vendor ID, product ID, product revision, and methods to eject the media and close the tray.</span></span>

## <a name="create-a-data-writer-and-write-the-burn-image"></a><span data-ttu-id="d7095-128">建立資料寫入器外掛程式並撰寫燒錄映射</span><span class="sxs-lookup"><span data-stu-id="d7095-128">Create a data writer and write the burn image</span></span>

<span data-ttu-id="d7095-129">**MsftDiscFormat2Data** 物件提供寫入方法、寫入函式和媒體專屬屬性的相關屬性。</span><span class="sxs-lookup"><span data-stu-id="d7095-129">The **MsftDiscFormat2Data** object provides the writing method, the properties about the write function and media-specific properties.</span></span> <span data-ttu-id="d7095-130">[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)介面提供 **MsftDiscFormat2Data** 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="d7095-130">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to the **MsftDiscFormat2Data** object.</span></span>

<span data-ttu-id="d7095-131">光碟錄製器會使用 [**IDiscFormat2Data：:p \_**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) 的 [ui] 錄製器屬性，連結至格式寫入器。</span><span class="sxs-lookup"><span data-stu-id="d7095-131">The disc recorder links to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="d7095-132">在錄製器系結至格式寫入器之後，您可以執行有關媒體的查詢並更新寫入特定屬性，然後再使用 [**IDiscFormat2Data：： write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) 方法將結果影像寫入光碟。</span><span class="sxs-lookup"><span data-stu-id="d7095-132">After the recorder is bound to the format writer, you can perform queries regarding the media and update write-specific properties before writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

<span data-ttu-id="d7095-133">IMAPI.EXE 所提供的其他格式寫入介面同樣適用;額外的格式寫入介面包括：</span><span class="sxs-lookup"><span data-stu-id="d7095-133">Other format writing interfaces provided by IMAPI work similarly; additional format writing interfaces include:</span></span>

-   <span data-ttu-id="d7095-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) 會清除可讀寫的光學媒體。</span><span class="sxs-lookup"><span data-stu-id="d7095-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) erases rewritable optical media.</span></span>
-   <span data-ttu-id="d7095-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) 會將原始影像寫入光學媒體。</span><span class="sxs-lookup"><span data-stu-id="d7095-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) writes a raw image to optical media.</span></span>
-   <span data-ttu-id="d7095-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) 會將音軌寫入光學媒體。</span><span class="sxs-lookup"><span data-stu-id="d7095-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) writes audio tracks to optical media.</span></span>

> [!Note]  
> <span data-ttu-id="d7095-137">在進行燒錄作業期間可能會發生電源狀態轉換 (也就是使用者登出或系統暫止) 這會導致燒錄程式中斷，以及可能遺失資料。</span><span class="sxs-lookup"><span data-stu-id="d7095-137">It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the interruption of the burn process and possible data loss.</span></span> <span data-ttu-id="d7095-138">如需程式設計考慮，請參閱 [防止在燒錄期間登出或暫停](preventing-logoff-or-suspend-during-a-burn.md)。</span><span class="sxs-lookup"><span data-stu-id="d7095-138">For programming considerations, see [Preventing Logoff or Suspend During a Burn](preventing-logoff-or-suspend-during-a-burn.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="d7095-139">VBScript 範例</span><span class="sxs-lookup"><span data-stu-id="d7095-139">VBScript example</span></span>

<span data-ttu-id="d7095-140">此腳本範例顯示如何使用 IMAPI.EXE 物件來燒錄光學媒體;更具體來說，請將目錄寫入空白光碟。程式碼不包含任何錯誤檢查，並假設如下：</span><span class="sxs-lookup"><span data-stu-id="d7095-140">This script example shows how to use the IMAPI objects to burn optical media; more specifically, write a directory to a blank disc. The code contains no error checking, and assumes the following:</span></span>

-   <span data-ttu-id="d7095-141">系統上已安裝相容的光碟裝置。</span><span class="sxs-lookup"><span data-stu-id="d7095-141">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="d7095-142">光碟裝置是系統上的第二個磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d7095-142">The disc device is the second drive on the system.</span></span>
-   <span data-ttu-id="d7095-143">光碟裝置中會插入相容的光碟。</span><span class="sxs-lookup"><span data-stu-id="d7095-143">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="d7095-144">光碟是空白的。</span><span class="sxs-lookup"><span data-stu-id="d7095-144">The disc is blank.</span></span>
-   <span data-ttu-id="d7095-145">要寫入光碟的檔案位於 "g： \\ burndir"。</span><span class="sxs-lookup"><span data-stu-id="d7095-145">Files to write to disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="d7095-146">您可以在此腳本中新增其他功能，例如錯誤檢查、裝置和媒體相容性、事件通知，以及計算光碟上的可用空間。</span><span class="sxs-lookup"><span data-stu-id="d7095-146">Additional functionality such as error checking, device and media compatibility, event notification, and calculating free space on the disc can be added to this script.</span></span>


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="d7095-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7095-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7095-148">使用 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="d7095-148">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="d7095-149">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="d7095-149">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="d7095-150">**IDiscFormat2Erase**</span><span class="sxs-lookup"><span data-stu-id="d7095-150">**IDiscFormat2Erase**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[<span data-ttu-id="d7095-151">**IDiscFormat2RawCD**</span><span class="sxs-lookup"><span data-stu-id="d7095-151">**IDiscFormat2RawCD**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[<span data-ttu-id="d7095-152">**IDiscFormat2TrackAtOnce**</span><span class="sxs-lookup"><span data-stu-id="d7095-152">**IDiscFormat2TrackAtOnce**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[<span data-ttu-id="d7095-153">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="d7095-153">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="d7095-154">**IDiscRecorder2**</span><span class="sxs-lookup"><span data-stu-id="d7095-154">**IDiscRecorder2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[<span data-ttu-id="d7095-155">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="d7095-155">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[<span data-ttu-id="d7095-156">**IStream**</span><span class="sxs-lookup"><span data-stu-id="d7095-156">**IStream**</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 