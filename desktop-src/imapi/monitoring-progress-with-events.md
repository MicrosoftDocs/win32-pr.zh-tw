---
title: 監視事件的進度
description: 數個介面可讓您執行事件處理常式來接收進度資訊。 例如，事件物件可以附加至資料寫入器，以接收寫入作業的狀態。
ms.assetid: 1f15a5fe-f5d7-4e09-805f-2d0380bf2bb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae3b425fc096234abf59d3a082fbe8a06f3f554
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842208"
---
# <a name="monitoring-progress-with-events"></a><span data-ttu-id="f59b7-104">監視事件的進度</span><span class="sxs-lookup"><span data-stu-id="f59b7-104">Monitoring Progress With Events</span></span>

<span data-ttu-id="f59b7-105">數個介面可讓您執行事件處理常式來接收進度資訊。</span><span class="sxs-lookup"><span data-stu-id="f59b7-105">Several interfaces let you implement an event handler to receive progress information.</span></span> <span data-ttu-id="f59b7-106">例如，事件物件可以附加至資料寫入器，以接收寫入作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="f59b7-106">For example, an event object can be attached to the data writer to receive status of the write operation.</span></span>

<span data-ttu-id="f59b7-107">在腳本中，事件處理常式會實作為副程式。</span><span class="sxs-lookup"><span data-stu-id="f59b7-107">An event handler is implemented as a subroutine in a script.</span></span> <span data-ttu-id="f59b7-108">下列範例示範如何定義副程式，並使用 **wscript.echo. ConnectObject** 方法將事件處理常式連接到物件。</span><span class="sxs-lookup"><span data-stu-id="f59b7-108">The following example shows how to define the subroutine and use the **WScript.ConnectObject** method to connect the event handler to the object.</span></span>


```VB
    ' Create the MsftDiscFormat2Data object (see the IDiscFormat2Data interface).
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")

    ' Attach event handler (see the DDiscFormat2DataEvents interface).
    ' The "dwBurnEvent_" parameter identifies the handler (see the 
    ' dwBurnEvent_Update subroutine).
    WScript.ConnectObject  dataWriter, "dwBurnEvent_"

' Event handler for the MsftDiscFormat2Data.Write method.
' For details of the subroutine's parameters, see the 
' DDiscFormat2DataEvents::Update method.
SUB dwBurnEvent_Update( byRef object, byRef progress )
    ' --- Other code occurs here. 
END SUB

```



<span data-ttu-id="f59b7-109">針對事件處理常式名稱指定的名稱必須包含底線尾碼 ( " \_ " ) 。</span><span class="sxs-lookup"><span data-stu-id="f59b7-109">The name specified for the event handler name must contain the underscore suffix ("\_").</span></span> <span data-ttu-id="f59b7-110">若要形成副程式名稱，請將方法名稱串連至事件處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="f59b7-110">To form the subroutine name, concatenate the method name to the event handler name.</span></span> <span data-ttu-id="f59b7-111">例如，如果您使用 "dataWriterEvent \_ " 做為事件處理常式名稱，而方法名稱為 "update"，則副程式名稱會是 dataWriterEvent \_ Update。</span><span class="sxs-lookup"><span data-stu-id="f59b7-111">For example, if you use "dataWriterEvent\_" as the event handler name and the method name is "Update", the subroutine name would be dataWriterEvent\_Update.</span></span>

<span data-ttu-id="f59b7-112">下列範例顯示將事件處理常式連接到物件的替代方法。</span><span class="sxs-lookup"><span data-stu-id="f59b7-112">The following example shows an alternative approach to connecting the event handler to the object.</span></span>


```VB
    ' Create object and connect the event handler in one step.
    '   Set dataWriter = _
    '   WScript.CreateObject("IMAPI2.MsftDiscFormat2Data","dwBurnEvent_")


' Event handler  
SUB dwBurnEvent_Update( byRef object, byRef progress )
    '--- Other code occurs here. 
END SUB
```



<span data-ttu-id="f59b7-113">如果系統包含第二個要監視的燒錄裝置，您必須建立另一個 **MsftDiscFormat2Data** 物件和事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="f59b7-113">If a system contains a second burn device to monitor, you would need to create another **MsftDiscFormat2Data** object and event handler.</span></span>

<span data-ttu-id="f59b7-114">下列範例是 [以燒錄光碟影像](burning-a-disc.md) 範例為基礎。</span><span class="sxs-lookup"><span data-stu-id="f59b7-114">The following example builds on the [Burning a Disc Image](burning-a-disc.md) example.</span></span> <span data-ttu-id="f59b7-115">此範例會將 ISO 映像寫入空白光碟，並使用事件處理常式來提供進度更新。</span><span class="sxs-lookup"><span data-stu-id="f59b7-115">The example writes an ISO image to a blank disc and uses an event handler to give progress updates.</span></span>


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree. 

' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

' *** IFormat2Data Write Action Enumerations
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_VALIDATING_MEDIA      = 0
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_FORMATTING_MEDIA      = 1
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_INITIALIZING_HARDWARE = 2
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_CALIBRATING_POWER     = 3
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_WRITING_DATA          = 4
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_FINALIZATION          = 5
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_COMPLETED             = 6
const IMAPI_FORMAT2_DATA_WRITE_ACTION_VERIFYING             = 7

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "c:\test\imt\data\2tracks"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to CD/DVD drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  'Disc file system
    Dim Dir                  'Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    ' Define the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.FreeMediaBlocks = dataWriter.FreeSectorsOnMedia
    FSI.FileSystemsToCreate = FsiFileSystemISO9660

    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Attach event handler to the data writing object.
    WScript.ConnectObject  dataWriter, "dwBurnEvent_"

    ' Specify the recorder and write the stream to disc.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

' Event handler - Progress updates when writing data

SUB dwBurnEvent_Update( byRef object, byRef progress )
    DIM strTimeStatus
    strTimeStatus = "Time: " & progress.ElapsedTime & _
        " / " & progress.TotalTime
   
    SELECT CASE progress.CurrentAction
    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_VALIDATING_MEDIA
        WScript.Echo "Validating media " & strTimeStatus

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_FORMATTING_MEDIA
        WScript.Echo "Formatting media " & strTimeStatus
        
    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_INITIALIZING_HARDWARE
        WScript.Echo "Initializing Hardware " & strTimeStatus

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_CALIBRATING_POWER
        WScript.Echo "Calibrating Power (OPC) " & strTimeStatus

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_WRITING_DATA
        DIM totalSectors, writtenSectors, percentDone
        totalSectors = progress.SectorCount
        writtenSectors = progress.LastWrittenLba - progress.StartLba
        percentDone = FormatPercent(writtenSectors/totalSectors)
        WScript.Echo "Progress:  " & percentDone & "  " & strTimeStatus

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_FINALIZATION
        WScript.Echo "Finishing the writing " & strTimeStatus
    
    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_COMPLETED
        WScript.Echo "Completed the burn."

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_VERIFYING
        WScript.Echo "Verifying the data."

    CASE ELSE
        WScript.Echo "Unknown action: " & progress.CurrentAction
    END SELECT
END SUB
```



## <a name="related-topics"></a><span data-ttu-id="f59b7-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="f59b7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f59b7-117">使用 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="f59b7-117">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="f59b7-118">**IStream**</span><span class="sxs-lookup"><span data-stu-id="f59b7-118">**IStream**</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="f59b7-119">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="f59b7-119">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="f59b7-120">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="f59b7-120">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="f59b7-121">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="f59b7-121">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 