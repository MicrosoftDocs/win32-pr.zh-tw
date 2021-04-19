---
description: 磁片管理中使用的函數。
ms.assetid: 301d3062-29a1-4b44-bbcd-e9d5b7d7823b
title: 磁片管理功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677443c58aa8b9a60758d817e31e3804ef25ae66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997905"
---
# <a name="disk-management-functions"></a>磁片管理功能

下列功能用於磁片管理。

## <a name="in-this-section"></a>本節內容



| 函式                                                    | 描述                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)<br/>     | 抓取指定磁片的相關資訊，包括磁片上的可用空間量。<br/>                                                                                                                                                              |
| [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)<br/> | 抓取磁片區可用空間量的相關資訊，也就是總空間量、可用空間的總容量，以及與呼叫執行緒相關聯之使用者可用的可用空間總量。<br/> |



 

磁片管理中使用的其他功能。



| 函式                         | 描述                                                                                                                                                                                                                        |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) | 建立或開啟檔案或 i/o 裝置。 最常使用的 i/o 裝置如下：檔案、檔案串流、目錄、實體磁片、磁片區、主控台緩衝區、磁帶機、通訊資源、郵筒和管道。<br/> |
| [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) | 刪除現有的檔案。<br/>                                                                                                                                                                                               |



 

 

 




