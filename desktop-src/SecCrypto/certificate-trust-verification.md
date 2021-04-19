---
description: 簽署訊息的收件者與訊息的簽署者之間必須存在信任。
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: 憑證信任驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b711e0a86dcc5ae9cdedea278d6a3a698dfd633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980580"
---
# <a name="certificate-trust-verification"></a>憑證信任驗證

簽署訊息的收件者與訊息的簽署者之間必須存在信任。 建立此信任的其中一種方法是透過 [*憑證*](../secgloss/c-gly.md)，這是一份電子檔，可驗證實體或人員是否為他們宣稱的身分。 憑證會由其他雙方所信任的協力廠商發行至實體。 因此，簽署訊息的每個收件者都會決定簽署者憑證的簽發者是否值得信任。 [*CryptoAPI*](../secgloss/c-gly.md) 已實行一種方法，可讓應用程式開發人員建立應用程式，以根據預先定義的受信任憑證或 [*根*](../secgloss/r-gly.md)清單來自動驗證憑證。 這份受信任的實體清單 (稱為主體) 稱為「 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 。

下列使用 CTL 的範例牽涉到內部網路 (內部網路) 系統管理員想要控制哪些外部來源受到信任。 在此情況下，系統管理員可以建立受信任的憑證或根清單、簽署它，然後以 CTL 的形式將清單提供給網路上的所有用戶端。 設計用來使用這項 CryptoAPI 功能的應用程式，只會接受已簽署的訊息，或是由清單中的實體所簽署的已下載軟體。

如需這些函式的清單，請參閱 [憑證驗證功能](cryptography-functions.md)。

 

 
