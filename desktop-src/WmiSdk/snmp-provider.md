---
description: " (snmp) 提供者的簡易網路管理通訊協定，可讓用戶端應用程式透過 Windows Management Instrumentation (WMI) 來存取 SNMP 資訊。"
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI 和 SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f1327afe2a86a1f56f40c0a93d904148ccaf1fd0547b6cb623d9eb420c2a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992298"
---
# <a name="wmi-and-snmp"></a>WMI 和 SNMP

 (snmp) 提供者的簡易網路管理通訊協定，可讓用戶端應用程式透過 Windows Management Instrumentation (WMI) 來存取 SNMP 資訊。 SNMP 提供者預設不會安裝。 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

簡易網路管理通訊協定 (SNMP) 使用架構來定義物件。 架構不同于 WMI 中使用的架構。 SNMPv1 和 SNMPv2C 架構稱為 (SMI-S) 管理資訊的結構，並封裝為管理資訊基礎 (MIB) 檔。 MIB 檔案會使用標準語言來定義物件-抽象語法標記法 1 (asn.1) ），以及一些巨集定義，做為描述物件的範本。 宏提供的資訊包括物件名稱、識別碼、語法、描述、存取權限、通訊協定作業和通訊協定編碼。 下表列出 SNMP 提供者如何處理 MIB 物件的不同層面。



| 主題                                                    | 描述                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [通知類型宏](notification-type-macro.md)   | **通知類型** 宏如何從 SNMP 對應至 WMI。  |
| [OBJECT 類型宏](object-type-macro.md)               | **物件類型** 宏如何從 SNMP 對應至 WMI。        |
| [文字慣例宏](textual-convention-macro.md) | **文字慣例** 宏如何從 SNMP 對應至 WMI。 |
| [TRAP 類型宏](trap-type-macro.md)                   | **陷阱類型** 宏如何從 SNMP 對應至 WMI。          |



 

SNMP 提供者隨附可將 MIB 物件轉譯成 WMI 物件的編譯器。 SNMP 編譯器也可以輸出錯誤或其他訊息。 如需詳細資訊，請參閱 [SNMP 編譯器錯誤訊息](snmp-compiler-error-messages.md) 和 [一般資訊訊息](general-information-messages.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 參考](wmi-reference.md)
</dt> <dt>

[WMI 提供者](wmi-providers.md)
</dt> </dl>

 

 



