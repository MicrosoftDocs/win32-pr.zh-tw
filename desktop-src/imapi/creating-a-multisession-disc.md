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
# <a name="creating-a-multisession-disc"></a>建立多會話光碟

[映射主控 API](about-imapi.md) (imapi.exe) 支援新增和移除下列多會話光碟類型的檔案：

-   CD-R/CD-RW
-   Single-Layer DVD + R/DVD-R-R
-   DVD + R 雙重圖層
-   BD-R
-   僅限 DVD-ROM/DVD + RW (**Windows 7**) 
-   **僅 (Windows 7** 的 DVD RAM) 
-   只有) 的 BD (**Windows 7**

使用 IMAPI.EXE 建立多會話光碟包含下列步驟。 這些記載的每個步驟都包含最後一節所提供完整 Visual Basic 腳本範例的相關部分。

## <a name="initializing-the-disc-recorder"></a>正在初始化光碟錄製器

在裝置初始化之前， **MsftDiscMaster2** 物件會提供系統上光學裝置的列舉。 [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)介面可讓您存取此裝置列舉，以加速適當錄製裝置的位置。 當您在電腦上新增或移除光學裝置時， **MsftDiscMaster2** 物件也會提供事件通知。

找出光碟錄製器並取出指派給它的識別碼之後，請建立新的 **MsftDiscMaster2** 物件，並使用特定的裝置識別碼將錄製器初始化。

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)介面可讓您存取基本的裝置資訊，例如廠商識別碼、產品識別碼、產品修訂，以及退出媒體或關閉紙匣的方法。

> [!Note]  
> 下列範例中宣告的其他常數和維度，稍後會在本檔的最後一節中的完整範例腳本中使用。 初始化光碟錄製器的動作不需要這些元素。

 


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



## <a name="creating-a-data-writer"></a>建立資料寫入器外掛程式

_ *MsftDiscFormat2Data** 物件提供撰寫方法、其屬性，以及媒體專屬屬性。 [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)介面會提供此物件的存取權。

光碟錄製器會使用 [**IDiscFormat2Data：:p 的操作人員 \_ 錄製**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) 器屬性，系結至格式寫入器。 將錄製器系結至格式寫入器之後，您可以在使用 [**IDiscFormat2Data：： write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) 方法將結果影像寫入光碟之前，先執行媒體和寫入特定的屬性查詢。

> [!Note]  
> 下列範例程式碼中所指定的用戶端名稱字串應該針對特定應用程式適當地調整。

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a>建立檔案系統物件

若要記錄新的會話，必須先產生燒錄映射。 **ISO9660**、 **Joliet** 和 **UDF** 格式的燒錄映射包含個別檔案和目錄的檔案系統。 **MsftFileSystemImage** 物件是檔案系統物件，其中包含要放在光學媒體上的檔案和目錄。 [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)介面提供檔案系統物件和設定的存取權。


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a>匯入檔案系統

在繼續之前，請檢查 [**IDiscFormat2：： get \_ MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) 屬性，以確定光碟不是空白的。

建立 **MsftFileSystemImage** 物件之後，您應該在呼叫 [**IFileSystemImage：： ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem)或 [**IFileSystemImage：： ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem)方法之前，先初始化 [**IFileSystemImage：:p \_**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) ] 屬性，以便從上次記錄的會話匯入檔案系統。 這些方法會使用描述先前記錄之檔案和目錄的資訊，自動填入 **MsftFileSystemImage** 物件。

> [!Note]  
> [**IFileSystemImage：:p 的 \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces)屬性通常會使用資料寫入器透過 [**IDiscFormat2Data：： get \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces)屬性提供的多會話介面進行初始化。

 

如果 IMAPI.EXE 不支援目前所插入之媒體的多會話，或是因為其他 (原因而無法附加媒體，則嘗試將 **IFileSystemImage：:p 的 \_ MultisessionInterfaces** 屬性設定為失敗，例如，因為它已) 關閉。

如果先前的燒錄會話包含一個以上的檔案系統類型， [**IFileSystemImage：： ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) 方法將會從目前最先進的檔案系統類型匯入資訊。 例如，在本主題所提供的範例中，UDF 是匯入的檔案系統。 不過，使用 [**IFileSystemImage：： ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) 方法可讓您選取要匯入的特定檔案系統。

> [!Note]  
> [**IFileSystemImage：： IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc)方法可以用來判斷光碟上可用的檔案系統。

 


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



## <a name="adding-or-removing-files-to-the-file-system"></a>新增或移除檔案系統的檔案

建立檔案系統物件並從先前的會話匯入檔案系統之後，請呼叫 [**IFileSystemImage：： CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) 和 [**IFileSystemImage：： CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) 方法，分別建立新的檔案和目錄物件。 檔案和目錄物件會提供檔案和目錄的特定詳細資料。 或者，目錄物件的 [**IFsiDirectoryItem：： AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) 方法（透過 [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) 介面表示）可以用來從另一個存放裝置新增現有的檔案和目錄， (也就是硬碟) 。

適用于 [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) 的事件處理常式更新方法會識別目前新增至檔案系統映射的檔案、已複製的磁區數目，以及要複製的磁區總數。

若要從檔案系統中移除現有的檔案和目錄，請針對透過 [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem)介面表示的目錄物件，使用 [**IFsiDirectoryItem：： remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove)和 [**IFsiDirectoryItem：： RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree)方法。 [**IFileSystemImage：： get \_ 根**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root)屬性是用來取得檔案系統根目錄的指標，以及 **IFsiDirectoryItem** 介面，以跨越目錄樹狀目錄。

> [!Note]  
> 透過 [**IFsiDirectoryItem：： Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) 和 [**IFsiDirectoryItem：： RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) 方法移除的檔案和目錄，不會實際從光碟中移除，而 advanced software 可以輕鬆地復原已刪除的資訊。

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a>建立檔案系統映射

最後一個步驟是呼叫 [**IFileSystemImage：： CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) 來建立燒錄影像的資料流程，並透過 [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) 介面提供其存取權。 此資料流程可以直接提供給 [**IDiscFormat2Data：： Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) 方法，或儲存至檔案以供稍後使用。


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a>範例摘要

下列 Visual Basic 腳本範例顯示如何使用 IMAPI.EXE 物件來建立多個多會話光碟。 此範例會建立新的會話，並將目錄新增至光碟。為了簡單起見，程式碼不會執行廣泛的錯誤檢查，並假設下列各項：

-   系統上已安裝相容的光碟裝置。
-   光碟裝置是系統上的第一個磁片磁碟機。
-   光碟裝置中會插入相容的光碟。
-   要新增至光碟的檔案位於 "g： \\ burndir"。

您可以在腳本中加入其他功能，例如廣泛的錯誤檢查、裝置和媒體相容性、事件通知，以及磁片上的可用空間計算。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 IMAPI.EXE](using-imapi.md)
</dt> <dt>

[_ *IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
