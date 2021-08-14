---
description: 新物件的 SACL
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: 新物件的 SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f9833fcfb45a612b6135579e44aca6f219661fd2aeb2998b899e5794fa7bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413838"
---
# <a name="sacl-for-a-new-object"></a>新物件的 SACL

系統會使用下列演算法，為大部分的新安全物件類型建立 SACL：

1.  物件的 SACL 是物件的建立者所指定之 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 中的 sacl。 除非在 \_ \_ 安全描述項的控制位中設定了 SE 的 sacl 保護位，否則系統會將任何可繼承的 ace 合併為指定的 SACL。 \_ \_ \_ \_ \_ \_ \_ 即使設定了 SE \_ SACL 保護的位，父物件的系統資源屬性 ace 和系統範圍原則識別碼 ace 也會合並到新的物件 \_ 。
2.  如果建立者未指定安全描述項，系統會從可繼承的 Ace 建立物件的 SACL。
3.  如果沒有指定或繼承的 SACL，物件就不會有 SACL。

若要為新物件指定 SACL，物件的建立者必須 \_ 啟用 SE 安全性 \_ 名稱[許可權](privileges.md)。 如果新物件的指定 SACL 只包含系統 \_ 資源 \_ 屬性 \_ ace，則 \_ \_ 不需要 SE 安全性名稱的許可權。 如果物件的 SACL 是從繼承的 Ace 建立的，則建立者不需要此許可權。

系統會使用不同的演算法來建立新 Active Directory 物件的 SACL。 如需詳細資訊，請參閱 [如何在新的目錄物件上設定安全描述項](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects)。

 

 
