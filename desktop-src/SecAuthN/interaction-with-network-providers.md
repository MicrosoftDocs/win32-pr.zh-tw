---
description: 說明 Winlogon 和網路提供者之間的互動。
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: 與網路提供者的互動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851740"
---
# <a name="interaction-with-network-providers"></a>與網路提供者的互動

您可以將系統設定為支援零個或更多的網路提供者。 這些網路提供者都可以指定需要進行特殊的互動式驗證處理。 這項功能可讓已安裝的網路收集每個網路專屬的識別和驗證資訊，但可讓它們在正常登入期間以及 [*Winlogon*](../secgloss/w-gly.md)的 [*內容*](../secgloss/c-gly.md) 和桌面的安全傘下收集它。

Winlogon 會在許多情況下呼叫網路提供者。 成功登入後，Winlogon 會呼叫網路提供者，讓他們可以收集 [*認證*](../secgloss/c-gly.md) 並驗證使用者的網路。 當使用者變更其密碼時，Winlogon 也會呼叫網路提供者。 這可讓每個使用者維護單一密碼以用於所有網路。

[**WLX \_ MPR \_ 通知 \_ 資訊**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info)結構是用來提供相關 GINA 函式中的識別和驗證資訊。 此結構包含下列成員。



| member             | 描述                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **pszUserName**    | 登入之使用者的帳戶名稱。                                                                                                                                                      |
| **pszDomain**      | 已登入使用者的功能變數名稱。 並非所有的驗證模型都有 (或其對等) 的領域概念，因此這個成員可以是 **Null**。                                              |
| **pszPassword**    | 當使用者在驗證期間提供了純文字密碼時，在此提供它可讓其他網路提供者使用相同的密碼 (來達到單一登入) ，而不會提示使用者。    |
| **pszOldPassword** | 在密碼變更之後，在此提供原始密碼以及 **pszPassword** 成員的新密碼，可讓網路提供者在不提示使用者的情況下升級其密碼。 |



 

[*GINA*](../secgloss/g-gly.md)不需要將此資訊提供給網路提供者。 如果傳遞 **Null** 指標而非有效的結構指標，網路提供者將會提示使用者提供資訊。

 

 
