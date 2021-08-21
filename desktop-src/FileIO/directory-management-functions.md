---
description: 目錄管理中使用的函數。
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: 目錄管理功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2042b7fc4cc7f6af64c3c0eba0938b3f5d78e7b551981e1cc820b38000b1d745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150436"
---
# <a name="directory-management-functions"></a>目錄管理功能

目錄管理中會使用下列功能。

## <a name="in-this-section"></a>本節內容



| 函式                                                                      | 描述                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | 建立新目錄。<br/>                                                                                                                                       |
| [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | 使用指定之範本目錄的屬性，建立新的目錄。<br/>                                                                                 |
| [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | 使用指定範本目錄的屬性，建立新目錄做為交易作業。<br/>                                                      |
| [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | 停止變更通知控制碼監視。<br/>                                                                                                                   |
| [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | 建立變更通知控制碼，並設定初始變更通知篩選準則。<br/>                                                                |
| [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | 要求作業系統在下次偵測到適當的變更時，發出變更通知處理。<br/>                                         |
| [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | 抓取目前進程的目前的目錄。<br/>                                                                                                       |
| [**ReadDirectoryChangesExW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | 抓取描述指定目錄內之變更的資訊，如果指定了該資訊類型，就可以包含擴充資訊。<br/> |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | 抓取描述指定目錄內變更的資訊。<br/>                                                                               |
| [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | 刪除現有的空白目錄。<br/>                                                                                                                           |
| [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | 將現有的空白目錄刪除為交易作業。<br/>                                                                                                 |
| [**>setcurrentdirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | 變更目前進程的目前的目錄。<br/>                                                                                                         |



 

 

 




