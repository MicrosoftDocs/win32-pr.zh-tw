---
description: 如果 Windows 物件沒有任意的存取控制清單 (DACL) ，則系統允許所有人都能完整存取它。
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: Dacl 和 Ace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28bf351fd59f634a7c7bf960aedac1c76659ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194939"
---
# <a name="dacls-and-aces"></a>Dacl 和 Ace

如果 Windows 物件沒有 [*任意的存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) ，則系統允許所有人都能完整存取它。 如果物件具有 DACL，則系統只允許在 DACL 中 (Ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 所明確允許的存取權。 如果 DACL 中沒有 Ace，系統就不允許存取任何人。 同樣地，如果 DACL 有允許存取一組有限使用者或群組的 Ace，系統會隱含地拒絕所有不包含在 Ace 中的受信任者的存取權。

在大部分的情況下，您可以使用允許存取的 Ace 來控制物件的存取;您不需要明確拒絕對物件的存取。 例外狀況是當 ACE 允許存取群組，而您想要拒絕存取群組的成員時。 若要這樣做，請在群組的「存取允許的 ACE」之前，將使用者的「拒絕存取」 ACE 放在 DACL 中。 請注意， [ace 的順序](order-of-aces-in-a-dacl.md) 很重要，因為系統會依序讀取 ace，直到授與或拒絕存取為止。 使用者的拒絕存取權 ACE 必須先出現;否則，當系統讀取群組的存取權允許 ACE 時，即會將存取權授與受限制的使用者。

下圖顯示的 DACL 會拒絕對一位使用者的存取，並授與對兩個群組的存取權。 群組 A 的成員會藉由將允許群組 A 和許可權的許可權累積給所有人，來取得讀取、寫入和執行存取權限。 例外狀況是 Andrew，因為它是 Everyone 群組的成員，所以遭到拒絕存取的 ACE 拒絕存取。

![根據群組成員資格授與不同存取權限的 dacl](images/accctrl1.png)

 

 
