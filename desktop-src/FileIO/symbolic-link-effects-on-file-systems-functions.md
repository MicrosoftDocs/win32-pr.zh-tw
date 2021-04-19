---
description: 符號連結如何影響使用路徑名稱來指定一個或多個檔案的標準檔案函數。
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: 檔案系統函數的符號連結效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a2fe1696bf5260a0c55ba8b6e4f107270d6da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988370"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a>檔案系統函數的符號連結效果

有數個使用路徑名稱來指定一個或多個檔案的標準檔案函式，會受到符號連結的使用所影響。 本主題將列出這些函式並描述行為的變更：

-   [CopyFile 和 CopyFileTransacted](#copyfile-and-copyfiletransacted)
-   [CopyFileEx](#copyfileex)
-   [CreateFile 和 CreateFileTransacted](#createfile-and-createfiletransacted)
-   [CreateHardLink 和 CreateHardLinkTransacted](#createhardlink-and-createhardlinktransacted)
-   [DeleteFile 和 DeleteFileTransacted](#deletefile-and-deletefiletransacted)
-   [FindFirstChangeNotification](#findfirstchangenotification)
-   [FindFirstFile 和 FindFirstFileTransacted](#findfirstfile-and-findfirstfiletransacted)
-   [FindFirstFileEx](#findfirstfileex)
-   [FindNextFile](#findnextfile)
-   [GetBinaryType](#getbinarytype)
-   [GetCompressedFileSize 和 GetCompressedFileSizeTransacted](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [GetDiskFreeSpace](#getdiskfreespaceex)
-   [GetDiskFreeSpaceEx](#getdiskfreespaceex)
-   [GetFileAttributes](#getfileattributesex)
-   [GetFileAttributesEx](#getfileattributesex)
-   [GetFileSecurity](#getfilesecurity)
-   [GetTempPath](#gettemppath)
-   [GetVolumeInformation](#getvolumeinformation)
-   [SetFileAttributes](#setfileattributes)
-   [SetFileSecurity](#setfilesecurity)
-   [相關主題](#related-topics)

在下列描述中，會使用下列詞彙：

-   原始程式檔—要複製的原始檔案。
-   目的地檔案—新建立的檔案複本。
-   目標：符號連結所指向的實體。

> [!Note]  
> 接受使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式所建立之控制碼的函式行為（例如 [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)函式）會根據使用檔案旗標 **開啟重新 \_ \_ \_ 分析 \_ 點** 旗標來呼叫 **CreateFile** 函式而有所不同。 如需詳細資訊，請參閱 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 和下列 [CreateFile 和 CreateFileTransacted](#createfile-and-createfiletransacted) 一節。

 

## <a name="copyfile-and-copyfiletransacted"></a>CopyFile 和 CopyFileTransacted

如果來源檔案是符號連結，則實際複製的檔案是符號連結的目標。

如果目的地檔案已經存在，而且是符號連結，則來源檔案會覆寫符號連結。

## <a name="copyfileex"></a>CopyFileEx

如果已指定 **複製檔案 \_ 複製的 \_ \_ 符號** ，且：

-   如果來源檔案是符號連結，則會複製符號連結，而不是目標檔。
-   如果來源檔案不是符號連結，行為就不會有任何變更。
-   如果目的地檔案是現有的符號連結，則會覆寫符號連結，而不會覆寫目標檔案。
-   如果也指定了 [ **\_ \_ \_ 如果 \_ 有的話，複製檔案失敗** ]，而目的地檔案是現有的符號連結，則在所有情況下作業都會失敗。

如果未指定 **複製檔案 \_ 複製的 \_ \_ 符號** ，且：

-   如果也指定了 [ **\_ \_ \_ 如果 \_ 有的話，複製檔案失敗** ]，而目的地檔案是現有的符號連結，則只有在符號連結的目標存在時，作業才會失敗。
-   如果未指定 **\_ \_ \_ \_ EXISTS，複製檔案失敗** ，則行為不會有任何變更。

**Windows Server 2003 和 WINDOWS XP：** 不支援 **複製檔案 \_ \_ 複製 \_ 符號** 旗標。 如果來源檔案是符號連結，則實際複製的檔案是符號連結的目標。

## <a name="createfile-and-createfiletransacted"></a>CreateFile 和 CreateFileTransacted

如果對此函式的呼叫會建立新的檔案，則不會變更行為。

如果指定了檔案旗標，則會指定，且： **\_ \_ \_ \_**

-   如果現有的檔案已經開啟，而且是符號連結，則傳回的控制碼是符號連結的控制碼。
-   如果指定了 [ **\_ 永遠建立**]、[ **截斷 \_ 現有**] 或 [檔案] **旗標 \_ \_ 刪除 \_ \_** ，則會將受影響的檔案設為符號連結。

如果未指定檔案旗標， **\_ 開啟重新 \_ \_ 分析 \_ 點** ，且：

-   如果現有的檔案已經開啟，而且是符號連結，則傳回的控制碼就是目標的控制碼。
-   如果指定了 [ **\_ 永遠建立**]、[ **截斷 \_ 現有**] 或 [檔案] **旗標 \_ \_ 刪除 \_ \_** ，則會將受影響的檔案設為目標。

## <a name="createhardlink-and-createhardlinktransacted"></a>CreateHardLink 和 CreateHardLinkTransacted

如果路徑指向符號連結，此函式會建立目標的永久連結。

## <a name="deletefile-and-deletefiletransacted"></a>DeleteFile 和 DeleteFileTransacted

如果路徑指向符號連結，則會刪除符號連結，而不是目標。 若要刪除目標，您必須呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ，並 **\_ \_ \_ 在 \_ 關閉時** 指定檔案旗標刪除。

## <a name="findfirstchangenotification"></a>FindFirstChangeNotification

如果路徑指向符號連結，則會為目標建立通知控制碼。 如果應用程式已註冊接收包含符號連結之目錄的變更通知，則只有在已變更符號連結，而非目標檔案時，才會通知應用程式。

## <a name="findfirstfile-and-findfirstfiletransacted"></a>FindFirstFile 和 FindFirstFileTransacted

如果路徑指向符號連結， [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) 緩衝區就會包含符號連結（而非目標）的相關資訊。

## <a name="findfirstfileex"></a>FindFirstFileEx

如果路徑指向符號連結， [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) 緩衝區就會包含符號連結（而非目標）的相關資訊。

## <a name="findnextfile"></a>FindNextFile

如果路徑指向符號連結， [**WIN32 \_ 尋找 \_ 資料**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) 緩衝區就會包含符號連結（而非目標）的相關資訊。

## <a name="getbinarytype"></a>GetBinaryType

如果路徑指向符號連結，則會使用目標檔案。

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a>GetCompressedFileSize 和 GetCompressedFileSizeTransacted

如果路徑指向符號連結，函數會傳回目標的檔案大小。

## <a name="getdiskfreespace"></a>GetDiskFreeSpace

如果路徑指向符號連結，則會在目標上執行操作。

## <a name="getdiskfreespaceex"></a>GetDiskFreeSpaceEx

如果路徑指向符號連結，則會在目標上執行操作。

## <a name="getfileattributes"></a>GetFileAttributes

如果路徑指向符號連結，函數會傳回符號連結的屬性。

## <a name="getfileattributesex"></a>GetFileAttributesEx

如果路徑指向符號連結，函數會傳回符號連結的屬性。

## <a name="getfilesecurity"></a>GetFileSecurity

如果路徑指向符號連結，函數會傳回符號連結的屬性。

## <a name="gettemppath"></a>GetTempPath

如果路徑指向符號連結，則暫存路徑名稱會維護任何符號連結。

## <a name="getvolumeinformation"></a>GetVolumeInformation

如果路徑指向符號連結，此函數會傳回目標的磁片區資訊。

## <a name="setfileattributes"></a>SetFileAttributes

如果路徑指向符號連結，則函式會抓取符號連結的屬性。

## <a name="setfilesecurity"></a>SetFileSecurity

如果路徑指向符號連結，函數會傳回符號連結的屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[**GetBinaryType**](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
