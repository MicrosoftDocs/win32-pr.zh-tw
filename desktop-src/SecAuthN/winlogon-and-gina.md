---
description: Winlogon、GINA 和網路提供者都是互動式登入模型的部分。
ms.assetid: d049d83f-b962-4c47-a79a-da556831e319
title: Winlogon 和 GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cc39b905d6a49eb84ccab164f99481561133e6cdd9ea40cfd0b1067315569a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915067"
---
# <a name="winlogon-and-gina"></a>Winlogon 和 GINA

[*Winlogon*](../secgloss/w-gly.md)、 [*GINA*](../secgloss/g-gly.md)和網路提供者都是互動式登入模型的部分。 互動式登入程式通常是由 Winlogon、MSGina.dll 和網路提供者控制。 若要變更互動式登入程式，可以使用自訂的 GINA DLL 來取代 MSGina.dll。

若要與 Winlogon、GINA 和網路提供者合作，您應該具備 Windows 安全性架構的公司知識，特別是關於 [*權杖*](../secgloss/a-gly.md)、[*驗證套件*](../secgloss/a-gly.md)和相關事項。

> [!Note]  
> Windows Vista 會忽略 GINA dll。

 

如需特定函數和結構的詳細資訊，請參閱 [驗證參考](authentication-reference.md)。 這個參考章節包含 GINA DLL 必須執行之函式的描述、GINA DLL 可呼叫的 Winlogon 支援函式，以及用來在 Winlogon 和 GINA 之間傳遞資訊的資料結構。

您可以在平臺軟體發展工具組 (SDK) 安全性範例中找到範例 GINA 程式碼。 這些範例包含用來執行 GINA 存根和 GINA 掛勾的 C 程式碼。 如需有關自訂 GINA DLL 開發的詳細資訊，請將電子郵件訊息傳送至： ginareqs@microsoft.com 。

如需 Windows 所支援之驗證模型的相關資訊，以及有關 [*本地安全機構*](../secgloss/l-gly.md) (lsa) 服務和 [*驗證封裝*](../secgloss/a-gly.md)介面的詳細資訊，請參閱 [lsa 驗證](lsa-authentication.md)。

如需有關與安全性原則管理相關之本地安全機構的各方面的資訊，包括與其他電腦和網域的信任關係、許可權指派、審核產生控制、系統協助工具，以及其他類似的主題，請參閱 [LSA 原則](../secmgmt/lsa-policy.md)。

如需 Winlogon 和 GINA 的相關資訊，請參閱下列主題。



| 主題                                                                              | 描述                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Winlogon](winlogon.md)                                                           | Winlogon 針對 GINA DLL 提供一組支援功能。<br/>                                                                                                                                                                 |
| [吉娜](gina.md)                                                                   | GINA DLL 提供可自訂的使用者識別和驗證程式。<br/>                                                                                                                                            |
| [終端機服務 GINA 函式](terminal-services-gina-functions.md)           | 啟用終端機服務時，GINA 必須呼叫 Winlogon 支援函式來完成數個工作。<br/>                                                                                                                   |
| [與網路提供者的互動](interaction-with-network-providers.md)       | 您可以將系統設定為支援零個或更多的網路提供者。<br/>                                                                                                                                                          |
| [責任和功能](responsibilities-and-features.md)                 | 互動式登入程式的每個部分都有一組責任。<br/>                                                                                                                                                      |
| [Winlogon 與 GINA 之間的互動](interaction-between-winlogon-and-gina.md) | Winlogon 的狀態會決定呼叫哪個 GINA 函式來處理任何指定的 [*安全注意順序*](../secgloss/s-gly.md) (SAS) 事件。<br/> |
| [Winlogon 通知套件](winlogon-notification-packages.md)               | 您可以執行通知套件來監視及回應 Winlogon 事件。<br/>                                                                                                                                            |



 

 

 
