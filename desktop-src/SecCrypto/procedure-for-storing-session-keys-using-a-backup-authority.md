---
description: 使用備份授權單位來儲存工作階段金鑰的應用程式，通常會遵循下列步驟。
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: 使用備份授權單位儲存工作階段金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319267"
---
# <a name="storing-session-keys-using-a-backup-authority"></a>使用備份授權單位儲存工作階段金鑰

使用 [*備份授權*](../secgloss/b-gly.md) 單位來儲存工作階段金鑰的應用程式，通常會遵循下列步驟。

**若要使用備份授權單位**

1.  照常加密檔案。
2.  將用來加密檔案的 [*工作階段金鑰*](../secgloss/s-gly.md) 匯出至 [*簡單的金鑰 blob*](../secgloss/s-gly.md)，並指定使用您自己的 [*金鑰交換公開金鑰*](../secgloss/k-gly.md) 來加密金鑰 blob。 將此金鑰 BLOB 儲存在加密的檔案中。
3.  再次匯出工作階段金鑰，這次指定使用備份授權單位的公開金鑰來加密金鑰 BLOB。 將此金鑰 BLOB 連同金鑰的描述、序號等傳送給備份授權單位。

如果遺失 [*金鑰*](../secgloss/k-gly.md) 組，且可以建立金鑰擁有者的身分識別，則可以從 [*備份授權*](../secgloss/b-gly.md) 單位取出金鑰。 建立身分識別的程式取決於特定備份授權單位的原則，而且不牽涉到 CryptoAPI。

針對建立工作階段金鑰所需的程式碼，並將該金鑰匯出至可寫入磁片檔案的 [*簡單金鑰 BLOB*](../secgloss/s-gly.md) ，請參閱 [範例 C 程式：匯出工作階段金鑰](example-c-program-exporting-a-session-key.md)。

 

 
