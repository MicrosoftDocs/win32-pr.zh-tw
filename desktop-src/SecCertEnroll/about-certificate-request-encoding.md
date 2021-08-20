---
description: 在 Microsoft PKI 中，會將憑證要求從用戶端電腦傳送到憑證授權單位單位 (Ca) 為包含一連串編碼資料結構的二進位字串。
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: 憑證要求編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6bb65b496264fcd1f9667416c78d5d8cf246f1c9aa4cf736990a1f61669f19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904847"
---
# <a name="certificate-request-encoding"></a>憑證要求編碼

在 Microsoft PKI 中，會將憑證要求從用戶端電腦傳送到憑證授權單位單位 (Ca) 為包含一連串編碼資料結構的二進位字串。 憑證註冊 API 使用抽象語法標記法 (一)  (asn.1) 來描述及編碼這些結構。 基於本檔的目的，您可以在概念上將 asn.1 分為語法規則， (ISO 8824) 來描述資料結構，以及指定資料如何編碼以進行網路傳輸的編碼規則 (ISO 8825) 。 如需詳細資訊，請參閱下列主題：

-   [ASN. 1 語法和編碼簡介](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [ASN. 1 類型系統](about-asn-1-type-system.md)
-   [可辨別編碼規則](distinguished-encoding-rules.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於憑證註冊 API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



