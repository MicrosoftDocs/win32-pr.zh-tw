---
description: 當您呼叫 CreateNamedPipe 函式時，可以指定具名管道的安全描述項。 安全描述項可控制具名管道的用戶端和伺服器端的存取。
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: 具名管道安全性和存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cada606d8197ac2f64943aa742bbfd614fa4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987569"
---
# <a name="named-pipe-security-and-access-rights"></a>具名管道安全性和存取權限

Windows 安全性可讓您控制具名管道的存取。 如需安全性的詳細資訊，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。

當您呼叫 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)函式時，可以指定具名管道的 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。 安全描述項可控制具名管道的用戶端和伺服器端的存取。 如果您指定 **Null**，具名管道會取得預設安全描述項。 具名管道之預設安全描述項中的 Acl 會授與 LocalSystem 帳戶、系統管理員和 creator 擁有者的完全控制權。 他們也會將讀取權限授與 Everyone 群組和匿名帳戶的成員。

若要取出具名管道的安全描述項，請呼叫 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 函數。 若要變更具名管道的安全描述項，請呼叫 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

當執行緒呼叫 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) 開啟現有具名管道之伺服器端的控制碼時，系統會先執行存取檢查，再傳回控制碼。 存取檢查會根據具名管道的安全描述項中的 DACL 來比較執行緒的存取權杖和要求的 [存取權限](/windows/desktop/SecAuthZ/access-rights-and-access-masks) 。 除了要求的存取權限之外，DACL 還必須允許呼叫的執行緒檔案 \_ 建立 \_ 管道 \_ 實例存取具名管道。

同樣地，當用戶端呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函式來連接至具名管道的用戶端時，系統會先執行存取檢查，再授與用戶端的存取權。

[**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)函式所傳回的控制碼一律具有同步存取。 它也具有泛型 \_ 讀取、一般 \_ 寫入或兩者（視管道的開啟模式而定）。 以下是每個開啟模式的存取權限。



| 開啟模式                           | 存取權限                                              |
|-------------------------------------|------------------------------------------------------------|
| 管道 \_ 存取 \_ 雙工 (0x00000003)    | 檔案 \_ 一般 \_ 讀取、檔案 \_ 一般 \_ 寫入和同步處理 |
| 管道 \_ 存取 \_ 輸入 (0x00000001)   | 檔案 \_ 一般 \_ 讀取和同步處理                        |
| 管道 \_ 存取 \_ 輸出 (0x00000002)  | 檔案 \_ 一般 \_ 寫入和同步處理                       |



 

\_具名管道的檔案一般 \_ 讀取存取結合了從管道讀取資料、讀取管道屬性、讀取擴充屬性，以及讀取管線的 DACL 的許可權。

\_具名管道的檔案一般 \_ 寫入存取結合了將資料寫入管道的許可權、將資料附加至管線、寫入管道屬性、寫入擴充屬性，以及讀取管線的 DACL。 由於 FILE \_ 附加 \_ 資料和檔案 \_ 建立 \_ 管道 \_ 實例具有相同的定義，因此檔案 \_ 一般 \_ 寫入會啟用建立管道的許可權。 若要避免這個問題，請使用個別的許可權，而不要使用檔案 \_ 一般 \_ 寫入。

\_ \_ 如果您想要讀取或寫入物件的 SACL，您可以向具名管道物件要求存取系統安全性存取權。 如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](/windows/desktop/SecAuthZ/sacl-access-right)許可權[的存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

若要防止不同的終端機服務會話上的遠端使用者或使用者存取具名管道，請在該管道的 DACL 上使用登入 SID。 登入 SID 也會在執行為登入中使用;它是用來保護每個會話物件命名空間的 SID。 如需詳細資訊，請參閱 [在 c + + 中取得登入 SID](/previous-versions//aa446670(v=vs.85))。

 

 
