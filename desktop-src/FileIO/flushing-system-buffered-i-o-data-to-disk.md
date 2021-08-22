---
description: Windows 會將資料儲存在系統維護的資料緩衝區中的檔案讀取和寫入作業，以將磁片效能優化。
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: 將 System-Buffered i/o 資料排清到磁片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44740158ce1a5a2c3449a0fc5b90bc04bb0da525709cf7ee05c8768d10c39460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068698"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a>將 System-Buffered i/o 資料排清到磁片

Windows 會將資料儲存在系統維護的資料緩衝區中的檔案讀取和寫入作業，以將磁片效能優化。 當應用程式寫入檔案時，系統通常會緩衝資料，並定期將資料寫入磁片。 應用程式可以使用 [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) 函數，強制作業系統將這些資料緩衝區的內容寫入磁片。 或者，應用程式可以指定當使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式建立或開啟檔案時，將檔案旗標設定為 **\_ \_ 無 \_ 緩衝** 旗標，以略過資料緩衝區並直接寫入磁片。

如果在檔案關閉時，內部緩衝區中有資料，作業系統不會在關閉檔案之前自動將緩衝區的內容寫入磁片。 如果應用程式不會在關閉檔案之前強制作業系統將緩衝區寫入磁片，快取演算法會決定寫入緩衝區的時間。

> [!Note]  
> 在讀取或寫入作業使用時存取資料緩衝區可能會損毀緩衝區。 在作業完成之前，應用程式不得讀取、寫入、重新配置或釋放讀取或寫入作業正在使用的資料緩衝區。

 

 

 



