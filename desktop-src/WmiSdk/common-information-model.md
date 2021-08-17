---
description: 通用訊息模型 (CIM) 是一種可延伸的物件導向資料模型，包含企業中許多不同部分的資訊。
ms.assetid: 3e619cb7-18a9-40ff-82fe-c10eb5090a93
ms.tgt_platform: multiple
title: 通用訊息模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d095dfb7f05b7637ac027e6ea02eeba2e10e12845670aebd635e50e8c3265fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131640"
---
# <a name="common-information-model"></a>通用訊息模型

通用訊息模型 (CIM) 是一種可延伸的物件導向資料模型，包含企業中許多不同部分的資訊。 [CIM](https://www.dmtf.org/standards/cim)是分散式管理工作強制 ([DMTF](https://www.dmtf.org/)) 所維護的跨平臺標準。 開發人員透過 WMI 即可使用 CIM 來建立代表硬碟、應用程式、網路路由器或甚至是使用者定義的技術 (如空調網路) 的類別。 透過檢視和變更 CIM 類別，管理員即可控制企業的各個層面。 例如，管理員可以查詢代表桌面工作站的 CIM 類型執行個體。 然後管理員即可執行指令碼來修改 CIM 工作站執行個體。 WMI 會將對工作站 CIM 類別執行個體所做的任何變更轉譯為對實際工作站的變更。

CIM 是與語言無關的程式設計模型，使用物件導向技術來描述企業。 使用三個層級的父系/子系繼承時，CIM 可以同時描述企業的一般和特定層面。 CIM 也會使用稱為「關聯」的技術，將企業模型的不同部分連結在一起，並使用架構來區別不同的管理環境。

CIM 的設計目的是要在管理環境中提供一致的邏輯和實體物件的觀點。 CIM 使用稱為「類別」的物件導向結構來代表 managed 物件。 就像 c + + 或 COM 類別一樣，CIM 類別可以包含屬性來描述行為的資料和方法。 就像一組 COM 類別一樣，CIM 未系結至任何平臺。 不過，WMI 包含 CIM 的延伸模組，可描述 Microsoft Windows 作業系統平臺。

CIM 會定義三種層級的類別：

-   核心

    核心類別代表適用于所有管理區域的 managed 物件。 這些類別提供分析和描述受管理系統的基本詞彙。 [**\_ \_ 參數**](--parameters.md)和 [**\_ \_ SystemSecurity**](--systemsecurity.md)類別是核心類別的範例。

-   通用

    通用類別代表適用于特定管理區域的 managed 物件。 不過，通用類別與特定的執行或技術無關。 常見類別是核心類別的延伸。 [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem)類別是常見類別的範例。

-   Extended

    擴充類別代表屬於通用類別的技術特有新增的 managed 物件。 擴充類別通常會套用至特定的平臺，例如 UNIX 或 Microsoft Win32 環境。 Win32 無系統程式類別是擴充類別的範例。 [**\_**](/windows/desktop/CIMWin32Prov/win32-computersystem)

開發人員可以從另一個類別衍生一個類別。 衍生類別代表父類別的特殊案例，並繼承父系的所有屬性和方法。 例如， [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) UnitaryComputerSystem 會繼承自 [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem)。 繼承關聯性可以使用系統屬性 **\_ \_ 衍生**、 **\_ \_ 時代** 和 **\_ \_ 超類別** 來決定。 **\_ \_ 衍生** 系統屬性是一個字串陣列，其中列出整個繼承鏈（最多至和包含根類別，也包含在 **\_ \_ 時代** 中）。 **\_ \_ 超級類別** 系統屬性會顯示目前類別的直屬父代。

WMI 也支援關聯。 關聯是兩個或多個不同 WMI 類別之間的關聯性。 例如，執行中的工作站通常有處理器。 WMI 關聯類別 [win32 \_ ComputerSystemProcessor](/windows/desktop/CIMWin32Prov/win32-computersystemprocessor) 會將工作站類別 [**win32 \_ 電腦**](/windows/desktop/CIMWin32Prov/win32-computersystem) 和 processor 類別 [**win32 \_ 處理器**](/windows/desktop/CIMWin32Prov/win32-processor)建立關聯。 不過，關聯類別不需要將兩個相依類別結合在一起。 事實上，關聯類別的主要目的是要顯示不一定彼此相依之類別之間的關聯性。 如需詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。

最後，WMI 支援架構的概念。 在 WMI 的內容中，架構是一組類別，用來描述特定的管理環境。 Microsoft Windows 軟體開發套件 (SDK) 會使用兩個架構： CIM 架構和 Win32 架構。 CIM 架構類別名稱是以 [cim \_](cimclas.md)開頭，而 win32 架構類別名稱是以 [**win32 \_**](/windows/desktop/CIMWin32Prov/win32-provider)開頭。 CIM 架構包含核心和通用類別的定義，而 Win32 架構則包含 Win32 環境通用的擴充類別的定義。 不過，協力廠商可以建立自己的架構來描述廠商特定的需求。 因為架構是設計成可無限擴充的，所以開發人員一律可以新增類別來描述現有環境中的新受管理物件。 但為了簡單起見，大部分的廠商都選擇建立可從 CIM 或 Win32 架構繼承屬性的架構。

 

 
