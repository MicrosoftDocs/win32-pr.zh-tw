---
description: TAPI 3.1 引進了以 COM 為基礎的電話控制。 假設您熟悉 COM、OLE Automation 和腳本，就像是 TAPI 3 物件模型的知識一樣。 TAPI 2 電話控制功能的知識也很有説明。
ms.assetid: e56aef54-e358-429b-9f0f-c8776507d95f
title: 電話控制項和 Phone 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e9344d54a63efcf1692af361a5f8e88121981e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981529"
---
# <a name="phone-control-and-the-phone-object"></a>電話控制項和 Phone 物件

TAPI 3.1 引進了以 COM 為基礎的電話控制。 假設您熟悉 COM、OLE Automation 和腳本，就像是 TAPI 3 物件模型的知識一樣。 TAPI 2 電話控制功能的知識也很有説明。

手機控制是在三個功能層級上執行，每個都是以上一個層級為基礎：

-   電話物件。 第一個層級定義 TAPI 2.x 的電話裝置 (Api、常數和以 "phone" 開頭的訊息 ) 會在 TAPI 3.1 物件模型中公開。 這牽涉到從 TAPI 3.1 公開的新電話物件，並以 [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) 作為新物件的預設介面。 **ITPhone** 介面及其相關聯的常數、列舉型別和事件，通常會公開與 TAPI 2.x 函式、常數、結構和以 "phone" 一字開頭的訊息相同層級的詳細資料和功能。 此層級也牽涉到數個現有 TAPI 3.x 物件上的新介面，以加速建立電話物件，以及關聯電話物件與其相關的其他物件。
-   自動電話控制和通話處理。 第二個層級是由稱為 [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) 的額外介面和其相關聯的常數、列舉型別和事件所組成。 這是 phone 物件上的次要介面。 如果手機裝置是以擁有者許可權開啟，請在 [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)介面上使用 **QueryInterface** 方法來取得 **ITAutomatedPhoneControl** 介面指標。
-   Windows 2000 電話撥號程式。 第三個層級包含 Windows 2000 Phone 撥號程式應用程式的變更，以執行特定的使用者互動。

Microsoft 或協力廠商開發人員可以使用 TAPI 3.1 物件模型，來實行更先進的應用程式或與電話相關的服務，包括可讓通用序列匯流排 (USB) 的服務，例如，即使沒有任何使用者登入，或未明確啟動任何其他 TAPI 應用程式，仍可用於電話。

在 TAPI 3.0 中，電話 MSP 嘗試改善與用於 TAPI 3.0 通話的線路相關聯的電話裝置。 此開發旨在支援具有軟體可切換 speakerphones 的數據機。 使用此數據機類型的 TAPI 3.1 應用程式應該使用 TAPI 3.1 phone 物件來操作數據機 hookswitch 狀態。

如需詳細資訊以及與 Phone 物件相關聯之所有介面的清單，請參閱 [電話物件介面](phone-object-interfaces.md)。 電話控制介面公開的方法可讓您使用 COM 來控制電話組。

 

 



