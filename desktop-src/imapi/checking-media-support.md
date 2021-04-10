---
title: 檢查媒體支援
description: 下列腳本會檢查光碟裝置中所載入媒體的特性。
ms.assetid: 05d88612-ff4c-4894-b838-a1d76923430c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73fca4b11a5e0c1fbe5b001576126a3685149bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183346"
---
# <a name="checking-media-support"></a><span data-ttu-id="6a7a9-103">檢查媒體支援</span><span class="sxs-lookup"><span data-stu-id="6a7a9-103">Checking Media Support</span></span>

<span data-ttu-id="6a7a9-104">下列腳本會檢查光碟裝置中所載入媒體的特性。</span><span class="sxs-lookup"><span data-stu-id="6a7a9-104">The following script examines characteristics of the media loaded in the disc device.</span></span> <span data-ttu-id="6a7a9-105">更具體來說，它會檢查媒體類型和媒體的目前狀態，以及錄製器和媒體相容性。</span><span class="sxs-lookup"><span data-stu-id="6a7a9-105">More specifically, it checks the media type and the current state of the media, as well as recorder and media compatibility.</span></span> <span data-ttu-id="6a7a9-106">您可以調整此腳本，以在使用媒體之前確認相容性和狀態問題。</span><span class="sxs-lookup"><span data-stu-id="6a7a9-106">This script can be adapted to verify compatibility and state issues before using the media.</span></span>


```VB
' This script examines characteristics of the media loaded in the disc device.

' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** IMAPI2 Media Types 
Const IMAPI_MEDIA_TYPE_UNKNOWN            = 0  ' Media not present OR
                                               ' is unrecognized
Const IMAPI_MEDIA_TYPE_CDROM              = 1  ' CD-ROM
Const IMAPI_MEDIA_TYPE_CDR                = 2  ' CD-R
Const IMAPI_MEDIA_TYPE_CDRW               = 3  ' CD-RW
Const IMAPI_MEDIA_TYPE_DVDROM             = 4  ' DVD-ROM
Const IMAPI_MEDIA_TYPE_DVDRAM             = 5  ' DVD-RAM
Const IMAPI_MEDIA_TYPE_DVDPLUSR           = 6  ' DVD+R
Const IMAPI_MEDIA_TYPE_DVDPLUSRW          = 7  ' DVD+RW
Const IMAPI_MEDIA_TYPE_DVDPLUSR_DUALLAYER = 8  ' DVD+R dual layer
Const IMAPI_MEDIA_TYPE_DVDDASHR           = 9  ' DVD-R
Const IMAPI_MEDIA_TYPE_DVDDASHRW          = 10 ' DVD-RW
Const IMAPI_MEDIA_TYPE_DVDDASHR_DUALLAYER = 11 ' DVD-R dual layer
Const IMAPI_MEDIA_TYPE_DISK               = 12 ' Randomly writable

' *** IMAPI2 Data Media States
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_UNKNOWN            = 0
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_INFORMATIONAL_MASK = 15    
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_UNSUPPORTED_MASK   = 61532 '0xfc00
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_OVERWRITE_ONLY     = 1
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_BLANK              = 2
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_APPENDABLE         = 4     
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_FINAL_SESSION      = 8
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_DAMAGED            = 1024 '0x400
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_ERASE_REQUIRED     = 2048 '0x800
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_NON_EMPTY_SESSION  = 4096 '0x1000
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_WRITE_PROTECTED    = 8192 '0x2000
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_FINALIZED          = 16384 '0x4000
Const IMAPI_FORMAT2_DATA_MEDIA_STATE_UNSUPPORTED_MEDIA  = 32768 '0x8000


WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim recorder             ' Recorder object
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system

    ' Create a DiscMaster2 object to connect to CD/DVD drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Define the new disc format and set the recorder
    Dim dataWriter
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = recorder

    Dim boolResult
    boolResult = dataWriter.IsRecorderSupported(recorder)
    If boolResult = True then
        WScript.Echo "--- Current recorder IS supported. ---"
    else
        WScript.Echo "Current recorder IS NOT supported."
    end if

    boolResult = dataWriter.IsCurrentMediaSupported(recorder)
    If boolResult = True then
        WScript.Echo "--- Current media IS supported. ---"
    else
        WScript.Echo "Current media IS NOT supported."
    end if

    WScript.Echo "ClientName = " & dataWriter.ClientName

    ' Check a few CurrentMediaStatus possibilities. Each status
    ' is associated with a bit and some combinations are legal.
    Dim curMediaStatus
    curMediaStatus = dataWriter.CurrentMediaStatus
    WScript.Echo "Checking Current Media Status"
    
    if IMAPI_FORMAT2_DATA_MEDIA_STATE_UNKNOWN AND curMediaStatus then
        WScript.Echo "    Media state is unknown."
    end if

    if IMAPI_FORMAT2_DATA_MEDIA_STATE_OVERWRITE_ONLY AND curMediaStatus then
        WScript.Echo "    Currently, only overwriting is supported."
    end if
    
    if IMAPI_FORMAT2_DATA_MEDIA_STATE_APPENDABLE AND curMediaStatus then
        WScript.Echo "    Media is currently appendable."
    end if
    
    if IMAPI_FORMAT2_DATA_MEDIA_STATE_FINAL_SESSION AND curMediaStatus then
        WScript.Echo "    Media is in final writing session."
    end if
    
    if IMAPI_FORMAT2_DATA_MEDIA_STATE_DAMAGED AND curMediaStatus then
        WScript.Echo "    Media is damaged."
    end if
    
    Dim mediaType
    mediaType = dataWriter.CurrentPhysicalMediaType
    WScript.Echo "Current Media Type"
    DisplayMediaType(MediaType)

    WScript.Echo 
    WScript.Echo "----- Finished -----"
    Main = 0
End Function

Sub DisplayMediaType(dMediaType)
    Select Case dmediaType 
        Case IMAPI_MEDIA_TYPE_UNKNOWN
            WScript.Echo "    Empty device or an unknown disc type."
        
        Case IMAPI_MEDIA_TYPE_CDROM
            WScript.Echo "    CD-ROM"
        
        Case IMAPI_MEDIA_TYPE_CDR
            WScript.Echo "    CD-R"
        
        Case IMAPI_MEDIA_TYPE_CDRW
            WScript.Echo "    CD-RW"
        
        Case IMAPI_MEDIA_TYPE_DVDROM
            WScript.Echo "    Read-only DVD drive and/or disc"
        
        Case IMAPI_MEDIA_TYPE_DVDRAM
            WScript.Echo "    DVD-RAM"
        
        Case IMAPI_MEDIA_TYPE_DVDPLUSR
            WScript.Echo "    DVD+R"
        
        Case IMAPI_MEDIA_TYPE_DVDPLUSRW
            WScript.Echo "    DVD+RW"
        
        Case IMAPI_MEDIA_TYPE_DVDPLUSR_DUALLAYER
            WScript.Echo "    DVD+R Dual Layer media"
        
        Case IMAPI_MEDIA_TYPE_DVDDASHR
            WScript.Echo "    DVD-R"
        
        Case IMAPI_MEDIA_TYPE_DVDDASHRW
            WScript.Echo "    DVD-RW"
        
        Case IMAPI_MEDIA_TYPE_DVDDASHR_DUALLAYER
            WScript.Echo "    DVD-R Dual Layer media"
        
        Case IMAPI_MEDIA_TYPE_DISK
            WScript.Echo "    Randomly-writable, hardware-defect " _
                + "managed media type "
            WScript.Echo "    that reports the ""Disc"" profile " _
                + "as current."
        End Select
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="6a7a9-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a7a9-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a7a9-108">使用 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="6a7a9-108">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="6a7a9-109">**IMAPI.EXE \_ 媒體 \_ 實體 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6a7a9-109">**IMAPI\_MEDIA\_PHYSICAL\_TYPE**</span></span>](/windows/desktop/api/imapi2/ne-imapi2-imapi_media_physical_type)
</dt> <dt>

[<span data-ttu-id="6a7a9-110">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="6a7a9-110">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="6a7a9-111">**IDiscRecorder2**</span><span class="sxs-lookup"><span data-stu-id="6a7a9-111">**IDiscRecorder2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[<span data-ttu-id="6a7a9-112">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="6a7a9-112">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> </dl>

 

 




