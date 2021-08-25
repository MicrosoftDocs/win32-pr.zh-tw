---
title: 將已捕捉的資料儲存至新檔案
description: 將已捕捉的資料儲存至新檔案
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS 訊息
- capFileSaveAs 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f6f2f94ed1a7c7f7f8cae20b20c6fa4b5aa27e8105ab3f5dc33e60b7aff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892908"
---
# <a name="saving-captured-data-to-a-new-file"></a>將已捕捉的資料儲存至新檔案

如果使用者想要儲存已捕捉的資料，則應用程式應該使用 WM CAP 檔案的 [ [**\_ \_ \_ 另存**](wm-cap-file-saveas.md) 新檔] 訊息 (或 [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) 宏) ，將該檔案的內容儲存至另一個檔案。 此訊息不會變更 capture 檔案的名稱或內容。 您的應用程式必須指定新檔案的名稱，因為 capture 檔會保留其原始檔案名。

一般情況下，會針對預期的最大 capture 區段預先配置 capture 檔案，而且只會使用其中一部分來捕捉資料。 此訊息只會複製包含 capture 資料之 capture 檔案的部分。

 

 




