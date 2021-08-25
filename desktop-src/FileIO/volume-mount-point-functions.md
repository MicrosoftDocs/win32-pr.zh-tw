---
description: 用來管理裝載資料夾的函式。
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: 裝載的資料夾函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13175dc4846d8f8438a3f1b94b3e407aaf347e2b6d10ad5c3761899882ecdfaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870778"
---
# <a name="mounted-folder-functions"></a>裝載的資料夾函式

裝載的資料夾功能可以分為三個群組：一般用途的函式、用來掃描磁片區的函式，以及用來掃描磁片區是否有載入的資料夾。

## <a name="general-purpose-mounted-folder-functions"></a>General-Purpose 載入的資料夾函式



| 函式                                                                     | 描述                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | 刪除磁碟機號或掛接的資料夾。                                                                                                                   |
| [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | 抓取與指定磁片區掛接點相關聯之磁片區的磁片區 GUID 路徑 (磁碟機號、磁片區 GUID 路徑，或已載入的資料夾) 。 |
| [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | 抓取與指定磁片區相關聯的已掛接資料夾。                                                                                  |
| [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | 將磁片區與磁碟機號或另一個磁片區上的目錄產生關聯。                                                                                   |



 

## <a name="volume-scanning-functions"></a>Volume-Scanning 函式



| 函式                                   | 描述                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | 傳回電腦上的磁片區名稱。 [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) 可用來開始列舉電腦的磁片區。 |
| [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | 繼續呼叫 [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)來開始進行磁片區搜尋。                                                     |
| [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | 關閉磁片區的搜尋。                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a>載入的資料夾掃描功能



| 函式                                                       | 描述                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | 抓取指定磁片區上所裝載的資料夾名稱。 [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) 可用來開始掃描磁片區上掛接的資料夾。 |
| [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | 繼續呼叫 [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)來開始載入的資料夾搜尋。                                                                    |
| [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | 關閉已載入資料夾的搜尋。                                                                                                                                                      |



 

 

 



