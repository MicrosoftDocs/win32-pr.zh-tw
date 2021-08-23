---
description: Address 物件代表可以進行或接收呼叫的實體。
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Address 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9265663692b77ad8bf7c71b5efabf6485edc747da9cbf68de387df77089305f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872362"
---
# <a name="address-object"></a>Address 物件

Address 物件代表可以進行或接收呼叫的實體。 此物件會公開介面和方法，以允許應用程式執行一些作業，例如：

-   探索指定的位址是否可支援一組特定的媒體類型需求。
-   列舉目前與位址相關聯的呼叫。
-   建立或轉寄呼叫。
-   取得相關聯服務提供者的名稱。
-   如果媒體服務提供者存在，請取得允許詳細終端機操作的介面指標。
-   取得和設定其他資訊，例如訊息是否正在等候。

大部分的位址都與終端機相關聯，但這並不是一致的情況。 例如，在伺服器上提供設備存取權的遠端 TSP，在本機電腦上會有位址，而不是終端機。 Speakerless 數據機也沒有與其位址相關聯的終端機。

如果位址沒有相關聯的終端機，就不會在物件上公開 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) 介面。

[ [選取位址程式](select-an-address.md) 代碼] 範例會顯示取得位址物件指標的基本流程。

如需與 Address 物件相關聯的所有介面清單，請參閱 [Address 物件介面](address-object-interfaces.md) 。

 

 
