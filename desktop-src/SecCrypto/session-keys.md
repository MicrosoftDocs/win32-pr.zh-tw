---
description: 工作階段金鑰是為了在單一通訊會話中使用而產生的金鑰。
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: 工作階段金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981035"
---
# <a name="session-keys"></a>工作階段金鑰

[*工作階段金鑰*](../secgloss/s-gly.md) 是為了在單一通訊會話中使用而產生的金鑰。 工作階段金鑰會經常變更，並在不再需要時捨棄。 例如，TLS 針對每個連線使用不同的工作階段金鑰，而 S/MIME 針對每個電子郵件訊息使用個別的工作階段金鑰。 通常會使用 [*對稱金鑰*](../secgloss/s-gly.md) 做為工作階段金鑰。

工作階段金鑰是暫時性的。 應用程式可以儲存這些金鑰以供稍後使用，或傳輸給其他使用者。 如需詳細資訊，請參閱 [密碼編譯金鑰儲存和交換](cryptographic-key-storage-and-exchange.md)。

 

 
