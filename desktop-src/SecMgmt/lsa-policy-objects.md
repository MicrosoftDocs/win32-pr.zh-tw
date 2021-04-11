---
description: LSA 會將本機安全性原則資訊儲存在一組物件中。 您的應用程式可以藉由存取這些物件來查詢或編輯本機安全性原則。
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: LSA 原則物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944357"
---
# <a name="lsa-policy-objects"></a>LSA 原則物件

LSA 會將本機安全性原則資訊儲存在一組物件中。 您的應用程式可以藉由存取這些物件來查詢或編輯本機安全性原則。

此集合是由下列四個物件所組成：

-   [原則](policy-object.md) 包含全域原則資訊。
-   [TrustedDomain](trusteddomain-object.md) 包含受信任網域的相關資訊。
-   [帳戶](account-object.md) 包含使用者、群組或本機群組帳戶的相關資訊。
-   [私用資料](private-data-object.md) 報含受保護的資訊，例如伺服器帳戶密碼。 這項資訊會儲存為加密字串。

如需如何使用 LSA 原則函式來管理這些物件中所儲存資訊的詳細資訊，請參閱 [使用 Lsa 原則](using-lsa-policy.md)。

 

 



