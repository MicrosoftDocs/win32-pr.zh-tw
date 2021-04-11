---
title: 防止多個上傳
description: 當您上傳檔案時，BITS 會建立會話識別碼，以識別 BITS 用戶端和 BITS 伺服器的上傳會話。
ms.assetid: 97283f8e-d2fa-4383-9b92-a05f46680443
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae59bb1d605af7e4dd53b0c1d66618b6816e7886
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020897"
---
# <a name="preventing-multiple-uploads"></a>防止多個上傳

當您上傳檔案時，BITS 會建立會話識別碼，以識別 BITS 用戶端和 BITS 伺服器的上傳會話。 如果 BITS 用戶端與伺服器之間的連接在 BITS 上傳檔案時中斷，用戶端會使用會話識別碼來嘗試繼續上傳。

如果 BITS 用戶端連接到與之前相同的伺服器，伺服器將會辨識會話識別碼，而上傳將會從中中斷點繼續。 但是，如果用戶端連接到不同的伺服器，用戶端就必須從頭開始上傳，因為新的伺服器沒有會話內容或先前上傳的資料。 當 BITS 伺服器裝載于 web 伺服陣列，且未設定 BITS IIS 擴充屬性（ [BITSHostId](bits-iis-extension-properties.md)）時，bits 可能會連接到不同的伺服器。 BITSHostId 屬性會強制 BITS 用戶端連接到先前伺服器的唯一位址，而非共用伺服器位址，以防止重新開機。

BITS 伺服器將只會嘗試將上傳檔案一次傳送至伺服器應用程式，但可能會有可能傳送一次以上的檔案。 例如，如果 BITS 伺服器將檔案傳送至伺服器應用程式，然後在等候伺服器應用程式的回復時終止，則可能會發生這種情況。 BITS 用戶端會收到來自 HTTP 層的錯誤碼，並在延遲後重試上傳。 如果伺服器保持離線的時間超過 [BITSHostIdFallbackTimeout](bits-iis-extension-properties.md) timeout，用戶端最後會再次將要求傳送至共用伺服器位址;不同的 BITS 伺服器將會收到檔案，然後再將它傳遞給伺服器應用程式。

即使是單一前端伺服器，也會發生類似的情況。 例如，當用戶端將整個檔案上傳到伺服器時，最終區塊會導致伺服器將檔案轉寄至伺服器應用程式。 如果 BITS 伺服器或伺服器應用程式在處理檔案之後，但在通知傳送至用戶端之前終止，則用戶端會收到錯誤碼，並于稍後重試。 當用戶端重試時，BITS 伺服器會看到最後一個區塊已上傳，並再次將檔案轉寄至伺服器應用程式。 如果接收上傳檔案多次是您的伺服器應用程式的問題，您應該考慮在資料中包含交易識別碼。

 

 




