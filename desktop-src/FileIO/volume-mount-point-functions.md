---
description: 用來管理裝載資料夾的函式。
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: 裝載的資料夾函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319408"
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



 

 

 



