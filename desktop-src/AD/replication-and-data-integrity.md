---
title: 複寫與資料完整性
description: Active Directory Domain Services 提供多宿主更新。
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory、使用、複寫和資料完整性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ec62ec3e44b9252d2d186b690105623b338bdaedf6ed15e4a253bfc2f06927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184453"
---
# <a name="replication-and-data-integrity"></a>複寫與資料完整性

Active Directory Domain Services 提供 *多宿主更新*。 多宿主更新表示指定磁碟分割的所有完整複本都是可寫入的， (通用類別目錄伺服器上的部分複本無法寫入。 ) 多宿主更新表示即使某些複本無法運作，也不會封鎖更新。 Active Directory 伺服器會將更新複本的變更傳播至所有其他複本。 複寫是自動且透明的。

如需詳細資訊，請參閱下列主題。

-   [Active Directory Domain Services 中的複寫模型](replication-model-in-active-directory-domain-services.md)
-   [Active Directory Domain Services 中的複寫行為](replication-behavior-in-active-directory-domain-services.md)
-   [偵測和避免複寫延遲](detecting-and-avoiding-replication-latency.md)

 

 




