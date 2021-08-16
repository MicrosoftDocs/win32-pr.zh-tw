---
description: 封包訊息是針對某位或一組收件者加密的訊息。
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: 建立和接收封包的資料訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63abf31d582ae9ae184dc15d85d827a3741d317e3bad75c8b07cce25e457bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768903"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a>建立和接收封包的資料訊息

封包訊息是針對一組收件者加密的訊息。 在 envelopment 程式中，會產生會話加密金鑰，並使用該金鑰來加密訊息。 然後，會使用每個預定收件者憑證的公開金鑰，針對每個收件者個別加密加密金鑰本身。 封包訊息包含加密的訊息、預定收件者的憑證，以及一組加密金鑰，每個收件者各一個。 產生的訊息是 [*PKCS \# 7*](../secgloss/p-gly.md)/CMS 格式。

下列各節顯示封包訊息工作的程式和範例：

-   [編碼封包資料](encoding-enveloped-data.md)
-   [解碼封包資料](decoding-enveloped-data.md)
-   [編碼封包訊息的替代程式碼](alternate-code-for-encoding-an-enveloped-message.md)
-   [範例 C 程式：編碼封包、簽署的訊息](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
