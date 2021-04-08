---
title: 轉換網域帳戶名稱格式
description: 在主機伺服器上使用服務控制管理員 (SCM) 的 Microsoft Win32 函數使用 \ 0034;網域 \\ 使用者名稱 \ 0034; 服務帳戶的格式。
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681684"
---
# <a name="converting-domain-account-name-formats"></a>轉換網域帳戶名稱格式

在主機伺服器上使用「服務控制管理員」 (SCM) 的 Microsoft Win32 函數會使用「 <domain> \\ <username> 服務帳戶」的格式。 例如，如果您呼叫 [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) 函式來抓取用來執行服務的使用者帳戶，則此函式會傳回 "Fabrikam \\ jeffsmith" 格式的名稱。 若要系結至目錄中的使用者帳戶（例如變更帳戶密碼），需要帳戶的辨別名稱，其格式為 "CN = Jeff Smith，CN = Users，DC = Fabrikam，DC = COM"。

若要在各種名稱格式之間進行轉換，請使用 [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) 函式，此函式可以將名稱轉換為其他格式，例如 (UPN) 的使用者主體名稱。

 

 