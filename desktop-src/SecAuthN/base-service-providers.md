---
description: 這些服務提供者提供基本的智慧卡功能。
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: 基底服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07fab7f7406b4932ed5c08ab2c8743f8ebde57893aed4564f8fdf40758b5af4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883568"
---
# <a name="base-service-providers"></a>基底服務提供者

這些 [*服務提供者*](/windows/desktop/SecGloss/c-gly) 提供基本的 [*智慧卡*](/windows/desktop/SecGloss/s-gly) 功能。 它們可用來存取單一智慧卡功能，或可結合其 COM 介面，在單一服務提供者內提供數個功能。 這些服務提供者是用於開發其他服務提供者其他功能的組建區塊。

下列工作可由智慧卡 SDK 提供的基底服務提供者介面執行。



| 工作                                                                                                                   | 基底服務提供者介面         | DLL      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| 連線至智慧卡、執行交易、關閉連接等。                                         | [**ISCard**](iscard.md)                 | SCardSSP |
| 維護命令 APDU 和 [*回復 apdu*](/windows/desktop/SecGloss/r-gly)。          | [**ISCardCmd**](iscardcmd.md)           | SCardSSP |
| 查詢 [*智慧卡資料庫*](/windows/desktop/SecGloss/s-gly)。 | [**ISCardDatabase**](iscarddatabase.md) | SCardSSP |
| 找出智慧卡或讀卡機。                                                                                         | [**ISCardLocate**](iscardlocate.md)     | SCardSSP |
| 建立 ISO7816-4 命令 APDU。                                                                                       | [**ISCardISO7816**](iscardiso7816.md)   | SCardSSP |
| 使用 Visual Basic 相容的類型包裝 Istream 緩衝區。                                                         | [**IByteBuffer**](ibytebuffer.md)       | SCardSSP |



 

下列程式顯示這些基底服務提供者介面的一般使用方法。 在此範例中，會使用 [**ISCard**](iscard.md)、 [**ISCardISO7816**](iscardiso7816.md)和 [**ISCardCmd**](iscardcmd.md) 介面來執行交易。

**執行交易**

1.  針對所需的所有基底服務提供者介面建立實例 (例如， [**ISCard**](iscard.md)、 [**ISCardISO7816**](iscardiso7816.md)和 [**ISCardCmd**](iscardcmd.md)) 。
2.  使用 [**ISCard**](iscard.md)介面中的方法，連線特定的智慧卡。
3.  使用 [**ISCardISO7816**](iscardiso7816.md) 和 [**ISCardCmd**](iscardcmd.md) 物件，藉由呼叫 **ISCardISO7816** 方法來建立 ISO 7816-4 命令。 此命令會包含在 **ISCardCmd** 中做為命令 APDU。
4.  藉由呼叫 [**ISCard**](iscard.md) transaction 方法並傳遞所建立的 [**ISCardCmd**](iscardcmd.md) 物件，以使用卡片進行交易。 當交易完成時，結果會儲存在 **ISCardCmd** 回復 APDU 中。
5.  解讀 [**ISCardCmd**](iscardcmd.md) 回復 APDU 並重複。
6.  在作業完成時釋放所有介面。

如需在 Dll 內建立的 APDU 命令的詳細資訊，請參閱 [建立 ISO7816-4 APDU 命令](building-an-iso7816-4-apdu-command.md)。

 

 
