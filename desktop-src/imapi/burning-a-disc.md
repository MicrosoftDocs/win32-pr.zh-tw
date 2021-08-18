---
title: 燒錄光碟影像
description: 使用 IMAPI.EXE) 燒錄光碟的 (包含下列步驟：建立包含目錄和檔案的檔案系統映射以寫入光碟。設定光碟錄製器來與光學裝置通訊。建立資料寫入器外掛程式，並將映射燒錄至光碟。
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237a4aa73b6820b75b4a9a1ed03baeeb87ac093bfc549cb9cc0ed947077515dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758908"
---
# <a name="burning-a-disc-image"></a>燒錄光碟影像

使用 IMAPI.EXE) 燒錄光碟的主控 (包含下列步驟：

1.  建立檔案系統映射，其中包含要寫入光碟的目錄和檔案。
2.  [設定光碟錄製](#set-up-a-disc-recorder) 器來與光學裝置通訊。
3.  [建立資料寫入器外掛程式](#create-a-data-writer-and-write-the-burn-image) ，並將映射燒錄至光碟。

如需燒錄光碟影像的範例，請參閱 [VBScript 範例](#vbscript-example)。

## <a name="construct-a-burn-image"></a>建造燒錄映射

燒錄映射是準備寫入光學媒體的資料流程。 ISO9660、Joliet 和 UDF 格式的燒錄映射包含個別檔案和目錄的檔案系統。 **CFileSystemImage** 物件是檔案系統物件，可保存要放置在光學媒體上的檔案和目錄。 [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)介面提供檔案系統物件和設定的存取權。

建立檔案系統物件之後，請呼叫 [**IFileSystemImage：： CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) 和 [**IFileSystemImage：： CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) 方法，分別建立檔案和目錄物件。 檔案和目錄物件可以用來提供檔案和目錄的特定詳細資料。 適用于 [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) 的事件處理常式方法可以識別目前新增至檔案系統映射的檔案、已複製的磁區數目，以及要複製的磁區總數。

您可以選擇性地使用 [**IFileSystemImage：:p] \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) 屬性將開機映射附加至檔案系統。 如需範例，請參閱 [新增開機映射](adding-a-boot-image.md)。

最後，呼叫 [**IFileSystemImage：： CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) 來建立資料流程，並透過 [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult)提供存取權。 然後，新的資料流程可以直接提供給 [**IDiscFormat2Data：： Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) 方法，或儲存至檔案以供稍後使用。

## <a name="set-up-a-disc-recorder"></a>設定光碟錄製器

**MsftDiscMaster2** 物件會提供系統上光學裝置的列舉。 [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)介面會提供對結果裝置列舉的存取權。 跨越列舉以找出適當的錄製裝置。 當您在電腦上新增或刪除光學裝置時， **MsftDiscMaster2** 物件也會提供事件通知。

尋找光碟錄製器並取出其識別碼之後，請建立 **MsftDiscRecorder2** 物件，並使用裝置識別碼將錄製器初始化。 [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)介面提供了錄製器物件的存取權，以及一些基本的裝置資訊，例如廠商識別碼、產品識別碼、產品修訂，以及用來退出媒體並關閉紙匣的方法。

## <a name="create-a-data-writer-and-write-the-burn-image"></a>建立資料寫入器外掛程式並撰寫燒錄映射

**MsftDiscFormat2Data** 物件提供寫入方法、寫入函式和媒體專屬屬性的相關屬性。 [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)介面提供 **MsftDiscFormat2Data** 物件的存取權。

光碟錄製器會使用 [**IDiscFormat2Data：:p \_**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) 的 [ui] 錄製器屬性，連結至格式寫入器。 在錄製器系結至格式寫入器之後，您可以執行有關媒體的查詢並更新寫入特定屬性，然後再使用 [**IDiscFormat2Data：： write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) 方法將結果影像寫入光碟。

IMAPI.EXE 所提供的其他格式寫入介面同樣適用;額外的格式寫入介面包括：

-   [**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) 會清除可讀寫的光學媒體。
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) 會將原始影像寫入光學媒體。
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) 會將音軌寫入光學媒體。

> [!Note]  
> 在進行燒錄作業期間可能會發生電源狀態轉換 (也就是使用者登出或系統暫止) 這會導致燒錄程式中斷，以及可能遺失資料。 如需程式設計考慮，請參閱 [防止在燒錄期間登出或暫停](preventing-logoff-or-suspend-during-a-burn.md)。

 

## <a name="vbscript-example"></a>VBScript 範例

此腳本範例顯示如何使用 IMAPI.EXE 物件來燒錄光學媒體;更具體來說，請將目錄寫入空白光碟。程式碼不包含任何錯誤檢查，並假設如下：

-   系統上已安裝相容的光碟裝置。
-   光碟裝置是系統上的第二個磁片磁碟機。
-   光碟裝置中會插入相容的光碟。
-   光碟是空白的。
-   要寫入光碟的檔案位於 "g： \\ burndir"。

您可以在此腳本中新增其他功能，例如錯誤檢查、裝置和媒體相容性、事件通知，以及計算光碟上的可用空間。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 IMAPI.EXE](using-imapi.md)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 