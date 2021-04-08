---
title: 使用 ADSI 擴充功能重新使用 COM 匯總規則
description: 以下是 COM 匯總和 ADSI 擴充規則的簡短評論。
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- 延伸 ADSI、COM 匯總規則
- COM 匯總 ADSI
- 利用 ADSI 擴充功能來重新使用 COM 匯總規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683097"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a>使用 ADSI 擴充功能重新使用 COM 匯總規則

以下是 COM 匯總和 ADSI 擴充規則的簡短評論。

-   **CreateInstance** 方法會傳回 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面的指標，如下所示，不會將任何函式呼叫委派給匯總工具。

    [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法會傳回它所支援之介面的指標，以及它不支援的介面錯誤。

    [**IUnknown：： AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)方法會遞增匯總延伸模組物件本身的參考計數。

    [**IUnkown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法會遞減匯總延伸模組物件本身的參考計數，並在參考計數為0時終結本身。

-   在 [](/windows/win32/api/unknwn/nn-unknwn-iunknown) \_ **CreateInstance** 方法的執行期間，擴充物件應儲存匯總工具的 IUnknown 指標，例如 m pOuterUnknown。
-   擴充功能物件支援的所有介面（包括 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)）都應該繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)，這會將所有函式呼叫委派回匯總工具。
    -   [**IUnknown：： queryinterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫 "m \_ POuterUnknown->QueryInterface"
    -   [**IUnknown：： AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 會呼叫 "m \_ POuterUnknown->AddRef"
    -   [**IUnkown：： release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 呼叫 "m \_ POuterUnknown->版本"

延伸模組寫入器可以選擇任何想要的內部執行，前提是它們遵循標準 COM 匯總規則。 請注意，擴充物件不需要做為獨立物件。 延伸模組是設計來做為匯總。 不過，您可以撰寫延伸模組，以做為獨立物件和匯總。

除了標準的 COM 匯總支援，擴充物件也可支援 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) 以取得更先進的功能。 如果支援晚期繫結，則延伸模組應：

-   將 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 的函式委派回匯總工具。
-   在 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)中執行 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。

 

 