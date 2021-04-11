---
description: Microsoft \_ 針對不需要自訂驗證的本機電腦登入提供 MSV1 0 驗證套件。
ms.assetid: 8b85588d-0a79-43af-b526-7a5fc8248f99
title: MSV1_0 Authentication 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 662ae65f60bec61c30b12271a34dc9d3c2883d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194067"
---
# <a name="msv1_0-authentication-package"></a>MSV1 \_ 0 驗證套件

Microsoft \_ 針對不需要自訂驗證的本機電腦登入提供 MSV1 0 [*驗證套件*](../secgloss/a-gly.md) 。 「 [*本地安全機構*](../secgloss/l-gly.md) 」 (LSA) 會呼叫 MSV1 \_ 0 authentication 封裝，以處理 [*GINA*](../secgloss/g-gly.md) 針對 [*Winlogon*](../secgloss/w-gly.md) 登入程式所收集的登入資料。 MSV1 \_ 0 封裝會檢查本機安全性帳戶管理員 (SAM) 資料庫，以判斷登入資料是否屬於有效的 [*安全性主體*](../secgloss/s-gly.md) ，然後將登入嘗試的結果傳回至 LSA。

MSV1 \_ 0 也支援網域登入。 MSV1 \_ 0 會使用傳遞驗證來處理網域登入，如下圖所示。

![msv1 \- 0 驗證套件](images/lsaint4.png)

在傳遞驗證中，MSV1 0 的本機實例會 \_ 使用 Netlogon 服務來呼叫網域控制站上執行的 MSV1 \_ 0 實例。 網域控制站的 MSV1 0 實例會 \_ 接著檢查網域控制站的 SAM 資料庫，並將登入結果傳回至 \_ 本機電腦上的 MSV1 0 實例。 本機版本的 MSV1 0 會將 \_ 登入結果轉送到本機電腦上的 LSA 實例。

如果網域控制站無法使用，而且 LSA 包含使用者的快取 [*認證*](../secgloss/c-gly.md) ，則 MSV1 0 的本機實例 \_ 可以使用快取的登入資料來驗證使用者。

MSV1 \_ 0 驗證套件也支援 [子驗證套件](subauthentication-packages.md)。 子驗證套件是一個 DLL，可取代 MSV1 0 驗證套件所使用的驗證和驗證準則的一部分 \_ 。

MSV1 \_ 0 authentication 套件會定義 [*主要認證*](../secgloss/p-gly.md) 的索引鍵/字串值組。 主要認證字串會保存從登入期間所提供之資料衍生的認證。 它包含使用者名稱，以及區分大小寫且區分大小寫的使用者密碼格式。

 

 
