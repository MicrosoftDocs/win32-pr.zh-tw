---
title: 監視事件的進度
description: 數個介面可讓您執行事件處理常式來接收進度資訊。 例如，事件物件可以附加至資料寫入器，以接收寫入作業的狀態。
ms.assetid: 1f15a5fe-f5d7-4e09-805f-2d0380bf2bb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a871120ca872a3258d32290273dda11360f1d5abb356d1ec48f6130d87e45648
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849008"
---
# <a name="monitoring-progress-with-events"></a>監視事件的進度

數個介面可讓您執行事件處理常式來接收進度資訊。 例如，事件物件可以附加至資料寫入器，以接收寫入作業的狀態。

在腳本中，事件處理常式會實作為副程式。 下列範例示範如何定義副程式，並使用 **wscript.echo. ConnectObject** 方法將事件處理常式連接到物件。


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



針對事件處理常式名稱指定的名稱必須包含底線尾碼 ( " \_ " ) 。 若要形成副程式名稱，請將方法名稱串連至事件處理常式名稱。 例如，如果您使用 "dataWriterEvent \_ " 做為事件處理常式名稱，而方法名稱為 "update"，則副程式名稱會是 dataWriterEvent \_ Update。

下列範例顯示將事件處理常式連接到物件的替代方法。


```VB
    ' Create object and connect the event handler in one step.
    '   Set dataWriter = _
    '   WScript.CreateObject("IMAPI2.MsftDiscFormat2Data","dwBurnEvent_")


' Event handler  
SUB dwBurnEvent_Update( byRef object, byRef progress )
    '--- Other code occurs here. 
END SUB
```



如果系統包含第二個要監視的燒錄裝置，您必須建立另一個 **MsftDiscFormat2Data** 物件和事件處理常式。

下列範例是 [以燒錄光碟影像](burning-a-disc.md) 範例為基礎。 此範例會將 ISO 映像寫入空白光碟，並使用事件處理常式來提供進度更新。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 IMAPI.EXE](using-imapi.md)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 