---
title: BITS Upload 通訊協定
description: 本節說明 BITS 上傳和上傳-回復工作類型的網路通訊協定。
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01fea1ff4703dba9a0429c0b37e9c34ebe0d0099016af788c972dd8ee9fddef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021235"
---
# <a name="bits-upload-protocol"></a>BITS Upload 通訊協定

本節說明 BITS 上傳和上傳-回復工作類型的網路通訊協定。 BITS 上傳通訊協定會分層在 HTTP 1.1 之上，並使用許多現有的 HTTP 標頭，並定義新的標頭。 BITS 上傳通訊協定支援每個會話單一上傳檔案。

BITS 會使用封包來描述用戶端要求和伺服器回應。 BITS 封包類型標頭會指定正在傳送的封包類型。 每個封包都包含特定標頭。 BITS 會使用 BITS \_ POST 動詞命令來識別 bits 上傳封包。 回應封包一律會使用代表認可的 Ack 封包類型。 Ack 封包會在前一個要求的內容中傳送;一次只能有一個未處理的要求。

針對上傳-回復作業，BITS 會使用此通訊協定來上傳檔案，但不會使用此通訊協定將回復傳送給用戶端。 相反地，BITS 伺服器會將回復檔案的位置傳送至用戶端，而用戶端會建立 BITS 下載作業來下載回復檔案。

使用上傳通訊協定，以您自己的執行取代 BITS 用戶端或伺服器軟體。 如需 BITS 用戶端所傳送的要求封包清單，請參閱 [Bits 要求封包](bits-request-packets.md)。 如需 BITS 伺服器所傳送的回應封包清單，請參閱 [Bits 回應封包](bits-response-packets.md)。

用戶端會決定它如何回應 BITS 伺服器的錯誤或未預期的封包。 如果伺服器收到未預期的封包，伺服器應該傳送具有 400 (錯誤要求) 傳回碼的 Ack 封包。

 

 




