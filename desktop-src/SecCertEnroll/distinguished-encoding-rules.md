---
description: 抽象語法標記法 (一)  (asn.1) 會定義下列規則集，以管理在電腦之間傳送的資料結構如何進行編碼和解碼。
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: 可辨別編碼規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d592fdfbb2532f5c718aadaaf32e63f352ed6ab427e9908465fcb5998839f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883068"
---
# <a name="distinguished-encoding-rules"></a>可辨別編碼規則

抽象語法標記法 (一)  (asn.1) 會定義下列規則集，以管理在電腦之間傳送的資料結構如何進行編碼和解碼。

-    (BER) 的基本編碼規則
-   標準編碼規則 (CER) 
-   可辨別編碼規則 (DER) 
-   每個)  (壓縮的編碼規則

原始規則集是由 BER 規格所定義。 CER 和 DER 之後是以 BER 的特製化子集的方式開發。 針對使用 BER 或其變體傳輸資料所需的頻寬量，以回應用心發問也。 每個可節省大量費用。

為了滿足 x.509 規格的安全資料傳輸需求而建立了 DER。 憑證註冊 API 會以獨佔方式使用 DER。 如需詳細資訊，請參閱下列主題。

-   [DER 傳送語法](about-der-transfer-syntax.md)
-   [以 DER 編碼的 ASN. 1 類型](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASN. 1 類型系統](about-asn-1-type-system.md)
</dt> <dt>

[憑證要求編碼](about-certificate-request-encoding.md)
</dt> <dt>

[ASN. 1 語法和編碼簡介](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



