---
description: 憑證鏈是憑證的階層集合，會導致使用者或電腦回到信任的根目錄，通常是組織 (CA) 的根憑證授權單位。
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: 憑證鏈結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a6227746690468e934475904fcc0bd895d995e2a674b9a4c6e9d01bc792fdba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904857"
---
# <a name="certificate-chain"></a>憑證鏈結

憑證鏈是憑證的階層集合，會導致使用者或電腦回到信任的根目錄，通常是組織 (CA) 的根憑證授權單位。 因為所有的合作物件都有信任根憑證，所以合作物件可以藉由驗證憑證鏈來得到終端實體憑證的信任。 驗證通常需要建立鏈中的每個憑證：

-   是由先前憑證中的公開金鑰簽署。
-   尚未過期。
-   尚未撤銷。
-   符合先前憑證所指定的原則。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[憑證階層](about-certificate-hierarchy.md)
</dt> <dt>

[交叉認證](about-cross-certification.md)
</dt> <dt>

[信任模型](about-trust-models.md)
</dt> </dl>

 

 



