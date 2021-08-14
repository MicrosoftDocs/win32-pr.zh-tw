---
title: Active Directory Domain Services 的複寫模型功能
description: 在 Active Directory Domain Services 中使用的複寫模型稱為「聚合」的多重主要鬆散一致性。
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services，複寫模型
- 複寫模型功能 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd113ffe4182be47c9e8c84404fc748e417e78c866e41298ad19d8e7a0dec555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189529"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a>Active Directory Domain Services 的複寫模型功能

在 Active Directory Domain Services 中使用的複寫模型稱為「聚合」的 *多重主要鬆散一致性*。 在此模型中，目錄可以有多個複本;複寫系統會將任何指定複本所做的變更傳播到所有其他複本。 在任何特定時間，複本不保證會彼此一致 ( 「鬆散一致性」 ) ，因為變更可以隨時套用至任何複本 ( 「多宿主」 ) 。 如果允許系統達到穩定狀態，但未發生任何新的更新，並且已完全複寫所有先前的更新，則所有複本都保證會在同一組值 ( 「會合」 ) 。

 

 




