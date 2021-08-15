---
description: 新物件的 DACL
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: 新物件的 DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cfd5b8f8c16919260c4dace5394f864fe987885a7f2203b2b41162b7c41e701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782137"
---
# <a name="dacl-for-a-new-object"></a>新物件的 DACL

系統會使用下列演算法來建立最新安全物件類型的 DACL：

1.  物件的 DACL 是物件的建立者所指定之 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 中的 dacl。 除非在 \_ \_ 安全描述項的控制位中設定 SE DACL 保護的位，否則系統會將任何可繼承的 ace 合併至指定的 dacl。
2.  如果建立者未指定安全描述項，系統會從可繼承的 Ace 建立物件的 DACL。
3.  如果未指定任何安全描述項，而且沒有可繼承的 Ace，則物件的 DACL 是建立者之 [*主要*](/windows/desktop/SecGloss/p-gly) 或模擬 [*權杖*](/windows/desktop/SecGloss/i-gly) 中的預設 dacl。
4.  如果沒有指定、繼承或預設的 DACL，系統就會建立沒有 DACL 的物件，讓每個人都能完全存取該物件。

系統會使用不同的演算法來建立新 Active Directory 物件的 DACL。 如需詳細資訊，請參閱 [如何在新的目錄物件上設定安全描述項](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects)。

 

 
