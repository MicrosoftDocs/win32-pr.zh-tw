---
description: 建立憑證要求的程式牽涉到收集要求者的特定資訊。
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: 建立憑證要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607ebbfd5d230c216c2b7ebc4d3b217e1f8c0d2a375d39cdd6b311ec145be361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768878"
---
# <a name="creating-the-certificate-request"></a>建立憑證要求

建立憑證要求的程式牽涉到收集要求者的特定資訊。 通常，這是透過某種使用者介面 (UI) 來完成，不過，您可以直接從資料庫取得資訊，而不需要 UI。 所需的資訊層級是由 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 的原則所設定。

必要資訊的範例如下所示：

-   一般名稱
-   單位名稱
-   公司名稱
-   City
-   狀態
-   國家/地區

> [!Note]  
> 介面是設計來針對每個 xenroll.dll 實例提出單一要求。 您必須建立個別的 xenroll.dll 實例，才能建立每個 [*憑證要求*](../secgloss/c-gly.md)。

 

如需如何使用憑證註冊控制項以特定程式設計語言要求憑證的詳細資訊，請參閱下列主題：

-   [C + + 中的要求範例](request-sample-in-c-.md)
-   [VBScript 中的要求範例](request-sample-in-vbscript.md)

 

 
