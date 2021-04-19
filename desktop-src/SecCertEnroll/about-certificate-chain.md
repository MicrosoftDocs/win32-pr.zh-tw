---
description: 憑證鏈是憑證的階層集合，會導致使用者或電腦回到信任的根目錄，通常是組織 (CA) 的根憑證授權單位。
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: 憑證鏈結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982094"
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

 

 



