---
description: 用來列舉磁片區上所裝載之資料夾的函式。
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: 列舉裝載的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b047e4af74f33d6bc56476734f0f39c41dd14f
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386657"
---
# <a name="enumerating-mounted-folders"></a>列舉裝載的資料夾

下列函式可用來列舉指定 NTFS 磁片區上的已掛接資料夾：

-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

這些函式的運作方式非常類似 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)、 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)和 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數。

若要列舉磁片區上裝載的資料夾，請先找出磁片區是否支援掛接的資料夾。 若要這樣做，請使用 [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) 和 [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) 函數所傳回的磁片區名稱來呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式。 傳回的名稱會包含尾端的反斜線 (\\) 與 [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) 函式和相關函數相容。 如需有關用來掃描電腦上磁片區之函式的詳細資訊，請參閱 [列舉磁片](enumerating-volumes.md)區。 當您呼叫 **GetVolumeInformation** 函式時，如果 *lpFileSystemNameBuffer* 參數中傳回 "NTFS"，則磁片區是 NTFS 磁片區。 NTFS 檔案系統支援裝載的資料夾。

如果磁片區是 NTFS 磁片區，請呼叫 [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)來開始搜尋裝載的資料夾。 如果搜尋成功，請根據您的應用程式需求來處理結果。 然後在迴圈中使用 [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) ，以一次尋找並處理一個掛接的資料夾。 如果沒有其他已載入的資料夾要列舉，請呼叫 [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)來關閉搜尋控制碼。 請注意，搜尋只會尋找指定磁片區上所裝載的資料夾。

您不應該假設這些函式所傳回的已掛接資料夾順序與其他函式或工具傳回的裝載資料夾順序之間的任何關聯性。

 

 



