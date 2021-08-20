---
description: Windows 的安全性模型可讓您控制對檔案對應物件的存取。 如需詳細資訊，請參閱 Access-Control 模型。
ms.assetid: 8bbf7c98-ff83-4ed9-8b82-f08dcd31295c
title: 檔案對應安全性和存取權限
ms.topic: article
ms.date: 10/06/2018
ms.openlocfilehash: b34c383536e193023d08cc9b73363ffcc5f876e59fbfb520c78c74478090c501
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992821"
---
# <a name="file-mapping-security-and-access-rights"></a>檔案對應安全性和存取權限

Windows 的安全性模型可讓您控制對檔案對應物件的存取。 如需詳細資訊，請參閱 [存取控制模型](../secauthz/access-control-model.md)。

當您呼叫 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數時，可以指定檔案對應物件的 [安全描述項](../secauthz/security-descriptors.md)。 如果您指定 **Null**，則物件會取得預設安全描述項。 檔案對應物件之預設安全描述項中的 Acl 來自于建立者的主要或模擬權杖。

若要取出檔案對應物件的安全描述項，請呼叫 [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa) 或 [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo) 函數。 若要設定檔案對應物件的安全描述項，請呼叫 [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa) 或 [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

檔案對應物件的有效存取權限包括 **刪除**、 **讀取 \_ 控制**、 **寫入 \_ DAC**，以及 **寫入 \_ 擁有** 者 [標準存取權限](../secauthz/standard-access-rights.md)。 檔案對應物件不支援 [ **同步處理** 標準] 存取權限。 下表列出檔案對應物件特定的存取權限。

| 存取權限 | 意義 |
|-|-|
| **檔案 \_ 對應的 \_ 所有 \_ 存取** | 包含檔案對應物件的所有存取權限，但不包括檔案 **\_ 對應 \_ 執行**。 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile)和 [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex)函式會將此視為與指定 **檔案 \_ 對應 \_ 寫入** 相同。 |
| **檔案 \_ 對應 \_ 執行** | 允許對應檔案對應物件的可執行檔。 物件必須使用頁面保護建立，以允許執行存取，例如 **page \_ execute \_ READ**、 **page \_ execute \_ WRITECOPY** 或 **page \_ execute \_ READWRITE** 保護。  |
| **檔案 \_ 對應 \_ 讀取** | 允許對應檔對應物件的唯讀或可寫入寫入視圖。  |
| **檔案 \_ 對應 \_ 寫入** | 允許對應檔對應物件的唯讀、寫入寫入或讀取/寫入視圖。 物件必須以允許寫入存取權的頁面保護建立，例如 **page \_ READWRITE** 或 **page \_ EXECUTE \_ READWRITE** 保護。 |

對應檔案對應物件的「寫入時複製」視圖，需要與對應唯讀視圖相同的存取權。 **FILE \_ MAP \_ COPY** 旗標不是存取權限，而且不應該在安全描述項中指定為 DACL 的一部分。 這個值只能與對應檔案對應物件（例如 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 和 [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) 函式）的函式搭配使用，或與 [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) 函式搭配使用，它會將檔案 **\_ 對應 \_ 複製** 視為 **\_ \_ 讀取檔案對應** 的相同方式。

如果您想要讀取或寫入物件的 SACL，可以向檔案對應物件要求 **存取 \_ 系統 \_ 安全性** 存取權。 如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](../secauthz/sacl-access-right.md)許可權[的存取控制清單](../secauthz/access-control-lists.md)。
