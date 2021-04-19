---
description: Schannel 針對這些函式的輸入緩衝區中包含的不完整或超過的資訊，有一組定義完善的行為。
ms.assetid: 5fad1e76-6520-4ff7-b2b0-2cc2061062a1
title: Schannel 傳回的額外緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c9ce7a468b1b04389ad19f91785b64fb50e74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984681"
---
# <a name="extra-buffers-returned-by-schannel"></a>Schannel 傳回的額外緩衝區

建立 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 時，必須在用戶端與伺服器之間傳送資訊，而且之後，因為安全訊息是使用 Schannel 提供的加密和解密功能來交換的。 下列函式可用來完成這些工作：

-   [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
-   [**DecryptMessage (一般)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

Schannel 針對這些函式的輸入緩衝區中包含的不完整或超過的資訊，有一組定義完善的行為。 用戶端與伺服器之間的資訊會以下列方式交換：

1.  本機合作物件會藉由呼叫 SSPI 函式並傳入資訊，與 Schannel 互動。 一般而言，資訊是從遠端方收到的。
2.  函數會傳回包含資訊的狀態碼和輸出緩衝區。
3.  根據狀態碼，輸出緩衝區會透過某些通訊機制傳送給遠端方。
4.  遠端方會讀取由本機合作物件傳送的資訊。
5.  迴圈會重複，並將本機和遠端物件交換。  (遠端方呼叫 SSPI 函式，並傳入上一個步驟中讀取的資訊。 ) 

當 SSPI 函式的輸入緩衝區剛好包含所需的資訊時，一切都會如預期般運作。 不過，因為某些通訊協定的資料流程導向本質，所以可能不會發生這種情況;從遠端物件接收的資訊區塊可能包含比所需或更多的資料，而不是在單一函式呼叫中可由 Schannel 處理的資料。

如果輸入緩衝區包含太少的資訊，則函式會傳回 SEC \_ E \_ 未完成的 \_ 訊息。 呼叫端必須從遠端方取得額外的資料，然後再次呼叫函式。

當輸入緩衝區包含太多資訊時，Schannel 不會將此視為錯誤。 函式會盡可能處理最多的輸入，並傳回該處理活動的狀態碼。 此外，Schannel 會傳回之 SECBUFFER 額外類型的輸出緩衝區，以指出輸入緩衝區中是否有未處理的資訊 \_ 。 測試此類型緩衝區的輸出緩衝區是偵測這種情況的唯一方法。 額外緩衝區結構的 **cbBuffer** 欄位指出未處理多少位元組的輸入。

> [!Note]  
> 額外緩衝區的 **pvBuffer** 欄位不包含一份多餘的資料。

 

如果您收到來自 SSPI 函式的額外緩衝區，您必須從輸入緩衝區移除已處理的資訊，然後再次呼叫該函式。 Schannel 通常會傳回額外的緩衝區，而不會傳回輸出緩衝區中的任何其他緩衝區。

 

 
