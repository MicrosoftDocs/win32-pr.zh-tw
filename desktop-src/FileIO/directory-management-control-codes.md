---
description: 搭配檔案壓縮和解壓縮以及重新分析點使用的控制代碼。
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: 目錄管理控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1354d1a4ce72f2867ece1f15218d9c7cb3f364a12ea3eb0d3b16f66b0954e89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755188"
---
# <a name="directory-management-control-codes"></a>目錄管理控制碼

下列控制碼適用于 [檔案壓縮和解壓縮](file-compression-and-decompression.md)。



| 控制程式代碼                                             | 意義                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ 取得 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | 在檔案系統支援每個資料流程壓縮的磁片區上，抓取檔案或目錄的目前壓縮狀態。<br/>    |
| [**FSCTL \_ 設定 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | 在檔案系統支援每個檔案和每個目錄壓縮的磁片區上，設定檔案或目錄的壓縮狀態。<br/> |



 

下列控制碼會搭配重新 [分析點](reparse-points.md)使用。

## <a name="in-this-section"></a>本節內容



| 控制程式代碼                                                                   | 描述                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ 刪除重新 \_ 分析 \_ 點**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | 從指定的檔案或目錄中刪除重新分析點。<br/>                                              |
| [**FSCTL \_ 取得重新 \_ 剖析 \_ 點**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | 抓取與指定之控制碼所識別之檔案或目錄相關聯的重新分析點資料。<br/> |
| [**FSCTL \_ 設定重新 \_ 分析 \_ 點**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | 在檔案或目錄上設定重新分析點。<br/>                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案管理控制碼](file-management-control-codes.md)
</dt> <dt>

[磁碟區管理控制碼](volume-management-control-codes.md)
</dt> </dl>

 

