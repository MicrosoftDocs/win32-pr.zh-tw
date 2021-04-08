---
description: 當使用 CreateFile 函式的進程開啟檔案時，檔案控制代碼會與其相關聯，直到進程終止或使用 CloseHandle 函數關閉控制碼為止。
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: 檔案控制代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852128"
---
# <a name="file-handles"></a>檔案控制代碼

當使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式的進程開啟檔案時， *檔案控制代碼* 會與其相關聯，直到進程終止或使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函數關閉控制碼為止。 檔案控制代碼用來識別許多函式呼叫中的檔案。

每個檔案控制代碼和檔案物件通常都是開啟檔案的每個處理常式所特有的，唯一的例外是當處理常式所持有的檔案控制代碼重複，或子進程繼承父進程的檔案控制代碼時。 在這些情況下，這些檔案控制代碼是唯一的，但會看到單一的共用檔案物件。 如需有關複製進程所持有之檔案控制代碼的詳細資訊，請參閱 [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) 。

請注意，雖然檔案控制代碼通常是處理常式的私用，但檔案處理的檔案資料則不是。 因此，共用相同檔案的進程和執行緒必須同步處理其存取。 針對檔案的大部分作業，進程會透過其私用的控制碼集區來識別該檔案。

 

 
