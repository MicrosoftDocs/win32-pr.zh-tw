---
description: 串流內容會處理安全的資料流程導向通訊協定，例如 SSL 或 PCT。
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: 資料流程內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53103dc1269c05e5a2c162133d21e167d8035c2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943844"
---
# <a name="stream-contexts"></a>資料流程內容

串流內容會處理安全的資料流程導向通訊協定，例如 SSL 或 PCT。 為了共用相同的介面和類似的認證管理，SSPI 提供資料流程內容支援。 [*安全性通訊協定*](../secgloss/s-gly.md)結合了串流驗證配置和記錄格式。

為了提供資料流程導向的通訊協定，支援串流內容的 [*安全性套件*](../secgloss/s-gly.md) 具有下列處理常式特性：

-   封裝會設定 SECPKG \_ 旗 \_ 標資料流程旗標，表示它支援資料流程語義。
-   傳輸應用程式會要求資料流程語義，方法 \_ 是 \_ \_ \_ 在 InitializeSecurityCoNtext 的呼叫中設定 ISC 要求資料流程和 ASC 要求資料流程旗標 [**(一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 和 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 函數。
-   應用程式會使用 [**SecPkgCoNtext \_ StreamSizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes)結構來呼叫 [**QueryCoNtextAttributes (一般)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa)函式，以查詢要提供的緩衝區數目以及要為標頭或結尾保留的大小的 [*安全性內容*](../secgloss/s-gly.md)。
-   應用程式會在實際處理資料時，提供緩衝區描述項給備用。 藉由指定資料流程語義，呼叫端會指出要進行額外處理的意願，讓 [*安全性封裝*](../secgloss/s-gly.md) 可以處理訊息的封鎖。 基本上，在 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函式中，呼叫端會傳入緩衝區清單。 從資料流程導向 (（例如 TCP 埠) ）接收訊息時，呼叫端會傳入緩衝區清單，如下所示。

    | Buffer | 長度         | 緩衝區類型      |
    |--------|----------------|------------------|
    | 1      | 訊息長度 | 之 SECBUFFER \_ 資料  |
    | 2      | 0              | 之 SECBUFFER \_ 空白 |
    | 3      | 0              | 之 SECBUFFER \_ 空白 |
    | 4      | 0              | 之 SECBUFFER \_ 空白 |
    | 5      | 0              | 之 SECBUFFER \_ 空白 |

    

     

    然後，安全性封裝會在 [*BLOB*](../secgloss/b-gly.md)上運作。 如果函數傳回成功，緩衝區清單看起來會像下面這樣。

    

    | Buffer | 長度         | 緩衝區類型                |
    |--------|----------------|----------------------------|
    | 1      | 標頭長度  | 之 SECBUFFER \_ 資料流程 \_ 標頭  |
    | 2      | 資料長度    | 之 SECBUFFER \_ 資料            |
    | 3      | 尾端長度 | 之 SECBUFFER \_ 資料流程 \_ 結尾 |
    | 4      | 0              | 之 SECBUFFER \_ 空白           |
    | 5      | 0              | 之 SECBUFFER \_ 空白           |

    

     

    封裝也可能會傳回 \# 長度為 x 的緩衝區4和緩衝區類型之 secbuffer \_ 額外的，表示此緩衝區中的資料是下一筆記錄的一部分，而且尚未處理。 相反地，如果訊息函式傳回 SEC \_ E \_ 未完成的 \_ 訊息錯誤碼，則傳回的緩衝區清單看起來會像下面這樣。

    

    | Buffer | 長度 | 緩衝區類型        |
    |--------|--------|--------------------|
    | 1      | x      | \_遺漏之 SECBUFFER |

    

     

    這表示需要更多資料來處理記錄。 不同于訊息函式傳回的大部分錯誤，此緩衝區類型並不表示內容已遭入侵。 相反地，它會指出需要更多資料。 [*安全性套件*](../secgloss/s-gly.md) 在這種情況下不能更新其 [*狀態*](../secgloss/s-gly.md) 。

    同樣地，在通訊的寄件者端，呼叫端可以呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函式。 安全性封裝可能需要重新配置緩衝區或複製內容。 呼叫端可以更有效率地提供緩衝區清單，如下所示。

    

    | Buffer | 長度         | 類型                       |
    |--------|----------------|----------------------------|
    | 1      | 標頭長度  | 之 SECBUFFER \_ 資料流程 \_ 標頭  |
    | 2      | 資料長度    | 之 SECBUFFER \_ 資料            |
    | 3      | 尾端長度 | 之 SECBUFFER \_ 資料流程 \_ 結尾 |

    

     

    這可讓呼叫端更有效率地使用緩衝區。 藉由呼叫 [**QueryCoNtextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) 函式來判斷在呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature)之前要保留的空間量，此作業對應用程式和安全性封裝而言會更有效率。

 

 
