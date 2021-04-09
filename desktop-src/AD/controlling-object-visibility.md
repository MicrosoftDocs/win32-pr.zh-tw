---
title: 控制物件可見度
description: Active Directory Domain Services 可讓您隱藏物件，使其無法被拒絕特定許可權的使用者使用。
ms.assetid: 3a65ec79-7de0-4d14-b980-1ca6a972ac70
ms.tgt_platform: multiple
keywords:
- 控制物件可見度 Active Directory
- Active Directory Active Directory，使用控制物件可見度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b1ab364f0711174d5ac1dd1e4fbe98303c50b3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023275"
---
# <a name="controlling-object-visibility"></a>控制物件可見度

Active Directory Domain Services 可讓您隱藏物件，使其無法被拒絕特定許可權的使用者使用。 如果隱藏物件，以使用者認證執行的應用程式將無法列舉或系結至物件。

如果使用者被授與廣告直接在容器上 [**\_ \_ ACTRL \_ DS \_ 清單**](/windows/win32/api/iads/ne-iads-ads_rights_enum) 存取控制許可權，使用者可以查看容器的任何子物件。 同樣地，如果使用者被拒，ADS 會直接在容器上 **\_ \_ ACTRL \_ DS \_ 清單** 存取控制，使用者就無法查看容器的任何子物件。 這允許隱藏整個容器的內容。

Active Directory 伺服器也可以藉由將 [**dSHeuristics**](/windows/desktop/ADSchema/a-dsheuristics) 屬性的第三個字元設定為 "1"，而成為特殊的清單物件模式。 您可以藉由將 **dSHeuristics** 屬性的第三個字元設定為 "0" 來停用清單物件模式。 當 Active Directory 伺服器處於 [清單物件] 模式時，如果使用者已被授與父物件的 [**ADS \_ right \_ ACTRL \_ DS \_ 清單**](/windows/win32/api/iads/ne-iads-ads_rights_enum) ，仍會顯示該物件。 但是，如果使用者已被拒，在父系上的 **ads \_ right \_ ACTRL \_ ds \_ 清單** 中，如果使用者在父系和子物件上被授與 **ads \_ right \_ DS \_ 清單 \_ 物件** ，仍然可以看到特定的子物件。 清單物件模式允許系統管理員授與或拒絕使用者或群組個別物件的存取權。 應謹慎使用清單物件模式，因為它需要目錄服務所進行的存取檢查呼叫數目明顯較高，以判斷使用者是否可以看到物件。 因此，它可能會對從 Active Directory Domain Services 流覽或讀取物件的效能造成負面影響。

 

 