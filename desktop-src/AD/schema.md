---
title: '架構 (AD DS) '
description: Active Directory 架構會實作為一組儲存在目錄中的物件類別實例。
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory 架構 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "103679456"
---
# <a name="schema-ad-ds"></a>架構 (AD DS) 

Active Directory 架構會實作為一組儲存在目錄中的物件類別實例。 這與多個具有架構的目錄不同，但會將它儲存為在啟動時讀取的文字檔。 在目錄中儲存架構有許多優點。 例如，使用者應用程式可以讀取它以探索可用的物件和屬性。

Active Directory 架構可以動態更新。 也就是說，應用程式可以使用新的屬性和類別來延伸架構，並立即使用延伸模組。 架構更新是藉由建立或修改儲存在目錄中的架構物件來完成。 如同 Active Directory 中的每個物件，存取控制清單 (Acl) 保護架構物件，因此授權的使用者只會改變架構。

如需詳細資訊，請參閱 [Active Directory 架構](active-directory-schema.md)。

 

 




