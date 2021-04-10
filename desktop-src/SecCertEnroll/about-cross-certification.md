---
description: 「交叉認證」可讓一個公開金鑰基礎結構中的實體 (PKI) ，以信任另一個 PKI 中的實體。
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: 交叉認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193904"
---
# <a name="cross-certification"></a>交叉認證

「交叉認證」可讓一個公開金鑰基礎結構中的實體 (PKI) ，以信任另一個 PKI 中的實體。 在每個 PKI 的憑證授權單位單位 (CAs) 之間，此相互信任關係通常受到交叉憑證協定的支援。 合約會建立各方的責任和責任。

兩個 ca 之間的相互信任關係需要每個 CA 對另一個 CA 發出憑證，以建立雙向的關聯性。 因為不同的 Pki 可能是憑證階層，所以信任的路徑不是階層 (任何治理 CAs 都不屬於其他) 。 在兩個 Ca 建立並指定信任條款和互相發行的憑證之後，個別 Pki 內的實體可以與憑證中指定的原則互動。

![交叉認證圖表](images/cross-certification.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[信任模型](about-trust-models.md)
</dt> </dl>

 

 



