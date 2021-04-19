---
description: 從 PKCS 7 1.5 版衍生的 CMS)  (的密碼編譯訊息語法， \# 是用來雜湊、數位簽署、驗證和加密任意訊息的語法。
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: CMS 新增
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981499"
---
# <a name="cms-additions"></a>CMS 新增

從 PKCS 7 1.5 版衍生的 CMS)  (的密碼編譯訊息語法， \# 是用來 [*雜湊*](../secgloss/h-gly.md)、 [*數位簽署*](../secgloss/d-gly.md)、驗證和加密任意訊息的語法。 可能的話，會保留回溯相容性;不過，已進行變更以容納屬性憑證傳輸和金鑰管理的金鑰協定技術。 CMS 允許多個封裝，讓一個封裝信封可以嵌套在另一個。 此外，另一方可以數位簽署先前封裝的資料;您可以使用訊息內容來簽署任意屬性，例如簽章時間。和屬性（例如 [*副署*](../secgloss/c-gly.md)）可以與簽章相關聯。 CMS 可以支援各種不同的架構來進行以憑證為基礎的金鑰管理。

為了支援其他 CMS 功能，已為基礎資料結構提供了新的欄位。 也加入了新的旗標和參數值。 所有使用 CMS 的資料結構和所有 Api 都是與 PKCS 7 1.5 版回溯相容的 100% \# 。

新增專案包含新增的 [封包資料](enveloped-data-additions.md) 和 [已簽署的資料](signed-data-additions.md)。

 

 
