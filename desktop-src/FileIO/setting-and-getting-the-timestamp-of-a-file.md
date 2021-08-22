---
description: 應用程式可以使用 GetFileTime 和 SetFileTime 函式來取得和設定檔案的建立日期和時間、上次修改時間或上次存取的時間。
ms.assetid: f8930be6-7c2a-4e50-a7a1-d25f6e2a3951
title: 設定和取得檔案的時間戳記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e98bd87ae8224ecbebc46e5f9d0ed71ad3522097fb865afc0d16e53a828812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015126"
---
# <a name="setting-and-getting-the-timestamp-of-a-file"></a>設定和取得檔案的時間戳記

應用程式可以使用 [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) 和 [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) 函式來取得和設定檔案的建立日期和時間、上次修改時間或上次存取的時間。 如需詳細資訊，請參閱檔案 [時間](/windows/desktop/SysInfo/file-times)。

> [!Note]  
> 並非所有檔案系統都可以記錄建立和上次存取時間，而且並非所有檔案系統都會以相同的方式記錄它們。 例如，在 FAT 檔案系統上，建立時間的解析度為10毫秒、寫入時間的解析度為2秒，而存取時間的解析為1天 (真的是存取日期) 。 NTFS 檔案系統會在上次存取後的最多一小時內，延遲檔案上次存取時間的更新。

 

 

 
