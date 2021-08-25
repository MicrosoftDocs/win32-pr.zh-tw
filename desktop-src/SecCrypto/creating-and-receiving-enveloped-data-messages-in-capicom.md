---
description: 封包訊息包含加密的訊息、預定收件者的憑證，以及一組加密金鑰，每個收件者各一個。 產生的訊息是 PKCS \# 7/CMS 格式。
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: 在 CAPICOM 中建立及接收封包的資料訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4024516333b7dd416f788f181f2ac36e5e0f4e015953cdab26d08b48da16c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876537"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>在 CAPICOM 中建立及接收封包的資料訊息

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

封包訊息是針對一組收件者加密的訊息。 在 envelopment 程式中，會產生會話加密金鑰，並使用該金鑰來加密訊息。 然後，會使用每個預定收件者憑證的公開金鑰，針對每個收件者個別加密加密金鑰本身。 封包訊息包含加密的訊息、預定收件者的憑證，以及一組加密金鑰，每個收件者各一個。 產生的訊息是 PKCS \# 7/CMS 格式。

下列各節顯示封包訊息工作的程式和範例：

-   [傳送封包的資料訊息](sending-an-enveloped-data-message.md)
-   [接收封包的資料訊息](receiving-an-enveloped-data-message.md)

 

 



