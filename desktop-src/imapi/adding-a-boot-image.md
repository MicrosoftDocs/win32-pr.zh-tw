---
title: 新增開機映射
description: 此範例以燒錄光碟映射範例為基礎，新增程式碼以在光碟的開機區段中包含可開機映射。
ms.assetid: b23cdbb9-ae0d-4261-965b-56abe865f323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce48537f32f1dc574eef174b26daaa5e2ebe255
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022075"
---
# <a name="adding-a-boot-image"></a><span data-ttu-id="05ffa-103">新增開機映射</span><span class="sxs-lookup"><span data-stu-id="05ffa-103">Adding a Boot Image</span></span>

<span data-ttu-id="05ffa-104">此範例以 [燒錄光碟映射](burning-a-disc.md) 範例為基礎，新增程式碼以在光碟的開機區段中包含可開機映射。可開機映射會連接至寫入光碟的檔案系統物件。附加之後，其餘的燒錄程式與基本的燒錄程式相同。</span><span class="sxs-lookup"><span data-stu-id="05ffa-104">This example builds on the [Burning a Disc Image](burning-a-disc.md) example by adding code to include a bootable image in the boot section of the disc. The bootable image connects to the file system object that is written to disc. Once attached, the rest of the burning process is identical to the basic burning procedure.</span></span> <span data-ttu-id="05ffa-105">開機映射使用 CD 或 DVD 光碟機提供系統啟動。</span><span class="sxs-lookup"><span data-stu-id="05ffa-105">The boot image provides system startup using the CD or DVD disc drive.</span></span>

<span data-ttu-id="05ffa-106">此範例會 callpriority 可開機映射的路徑。</span><span class="sxs-lookup"><span data-stu-id="05ffa-106">The example hardcodes the path to the bootable image.</span></span> <span data-ttu-id="05ffa-107">請務必視需要變更路徑和其他的硬式編碼值。</span><span class="sxs-lookup"><span data-stu-id="05ffa-107">Be sure to change the path along with other hardcoded values as appropriate.</span></span>


```VB
' This script burns a boot image and data files to disc in a 
' single session  using files from a single directory tree. 

'Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF  = 4

WScript.Quit(Main)

Function Main
    Dim index                ' Index to recording drive.
    Dim recorder             ' Recorder object
    Dim path                 ' Directory of files to burn
    Dim stream               ' Data stream for burning device
    Dim bootFile             ' Path and filename of boot image
    
    index = 1                ' Second drive on the system
    path = "g:\BurnDir"      
    bootFile = "g:\BootImg\etfsboot.com"

    ' Create a DiscMaster2 object to connect to CD/DVD drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' -------- Adding Boot Image Code -----
    Dim bootOptions    
    WScript.Echo "Creating BootOptions"
    SET bootOptions = WScript.CreateObject("IMAPI2FS.BootOptions")
    bootOptions.Manufacturer = "Microsoft"
    bootOptions.PlatformId   = 0       ' x86 processor
    bootOptions.Emulation    = 0       ' EmulationType.EmulationNone
    
    ' Need a stream for the boot image file 
    Const adFileTypeBinary = 1
    DIM bootStream
    Set bootStream = CreateObject("ADODB.Stream")
    WScript.Echo "Creating IStream for file " + bootFile
    bootStream.Open
    bootStream.Type = adFileTypeBinary
    bootStream.LoadFromFile bootFile
    bootOptions.AssignBootImage(bootStream)
    
    ' Create disc file system image (ISO9660 in this example)
    Dim FSI
    SET FSI = WScript.CreateObject("IMAPI2FS.MsftFileSystemImage")
    FSI.ChooseImageDefaults(Recorder)
   
    ' Add the boot directory and its contents to the file system 
    FSI.BootImageOptions = bootOptions

    ' Add the content directory and files to the file system 
    FSI.root.AddTree path, FALSE

    Dim result
    Set result = FSI.CreateResultImage()
    stream = result.ImageStream

    ' Create and write stream to disc using the specified recorder.
    Dim dataWriter
    Set dataWriter = CreateObject("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    dataWriter.write(stream)
    WScript.Echo "----- Finished writing content -----"

    Main = 0
End Function

```



## <a name="related-topics"></a><span data-ttu-id="05ffa-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="05ffa-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05ffa-109">使用 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="05ffa-109">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="05ffa-110">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="05ffa-110">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="05ffa-111">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="05ffa-111">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="05ffa-112">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="05ffa-112">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 




