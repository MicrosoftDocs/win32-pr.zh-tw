---
description: 登入會話是一種計算會話，會在使用者驗證成功時開始，並在使用者登出系統時結束。
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: LSA 登入會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194073"
---
# <a name="lsa-logon-sessions"></a>LSA 登入會話

[*登入會話*](../secgloss/l-gly.md)是一種計算會話，會在使用者驗證成功時開始，並在使用者登出系統時結束。

當使用者成功通過驗證時，驗證套件會建立登入會話，並將資訊傳回給 [*本機安全性授權*](../secgloss/l-gly.md) 單位， (LSA) 用來建立新使用者的 [*權杖*](../secgloss/t-gly.md) 。 此外，此權杖還包含登入會話的 [*本機唯一識別碼*](../secgloss/l-gly.md) (LUID) ，稱為 [*登入識別碼*](../secgloss/l-gly.md)。

建立權杖時，登入會話的 [*參考計數*](../secgloss/r-gly.md) 會遞增。 當建立進程、模擬或其他用途的權杖複本時，也會遞增參考計數。 因為權杖使用已完成，且已刪除權杖的複本，所以會減少登入會話的參考計數。 當參考計數到達零時，就會刪除登入會話。

> [!Note]  
> 如果驗證失敗，則 [*驗證套件*](../secgloss/a-gly.md) 不應建立登入會話。 如果驗證套件必須先建立登入會話，才能對使用者的有效性進行最終判斷，而且如果驗證失敗，則驗證套件必須刪除會話。

 

 

 
