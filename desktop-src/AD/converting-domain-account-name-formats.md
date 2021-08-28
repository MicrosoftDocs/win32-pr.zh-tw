---
title: 轉換網域帳戶名稱格式
description: 在主機伺服器上使用服務控制管理員 (SCM) 的 Microsoft Win32 函數使用 \ 0034;網域 \\ 使用者名稱 \ 0034; 服務帳戶的格式。
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aaa1b3664cc0ad372f82b498153862e69013fb1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881604"
---
# <a name="converting-domain-account-name-formats"></a>轉換網域帳戶名稱格式

在主機伺服器上使用「服務控制管理員」 (SCM) 的 Microsoft Win32 函數會 &lt; &gt; \\ &lt; 針對服務帳戶使用「網域使用者名稱」 &gt; 格式。 例如，如果您呼叫 [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) 函式來抓取用來執行服務的使用者帳戶，則此函式會傳回 "Fabrikam \\ jeffsmith" 格式的名稱。 若要系結至目錄中的使用者帳戶（例如變更帳戶密碼），需要帳戶的辨別名稱，其格式為 "CN = Jeff Smith，CN = Users，DC = Fabrikam，DC = COM"。

若要在各種名稱格式之間進行轉換，請使用 [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) 函式，此函式可以將名稱轉換為其他格式，例如 (UPN) 的使用者主體名稱。

 

 
