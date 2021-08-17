---
description: 當公開金鑰基礎結構中的已發行憑證數目 (PKI) 增加時，單一證書 (頒發機構單位) 可能會變得很難有效追蹤它所發行的憑證。
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: 憑證階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc3420e3f0f09f88b4b9e7157ec8abacc9516520de4472a48189520e3e0e567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904971"
---
# <a name="certificate-hierarchy"></a>憑證階層

當公開金鑰基礎結構中的已發行憑證數目 (PKI) 增加時，單一證書 (頒發機構單位) 可能會變得很難有效追蹤它所發行的憑證。 解決此問題的其中一種方式是建立憑證階層，CA 會將憑證頒發給次級授權單位，進而將授權委派給次級授權單位。 每個 CA 都會將 CA 憑證簽發給次級，以委派授權單位。 鏈中的初始 CA 稱為「根」（root），而且實體不需要與實體所在的不同 [憑證鏈](about-certificate-chain.md) 上的任何 CA 建立信任關係。

下圖顯示由一個根 CA 組成的憑證階層、兩個附屬於根 CA 的 Ca， (一個用於行銷部門，另一個用於製造部門) ，另一個則是附屬於這些 CA 的 ca。

![憑證階層圖](images/certificate-hierarchy.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[信任模型](about-trust-models.md)
</dt> </dl>

 

 



