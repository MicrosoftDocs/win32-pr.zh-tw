---
title: 釋放 WinSNMP 描述項
description: 根據哪個元件配置描述項的記憶體而定，WinSNMP 程式設計環境會將描述元資源解除配置指派給 WinSNMP 的執行或 WinSNMP 應用程式。
ms.assetid: 3e4cbbc5-18bc-4731-971c-6e533d904f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86081a69cd5455bc3c58ca2bcea50154d75920a17655a1feef30ac2d29675d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009526"
---
# <a name="freeing-winsnmp-descriptors"></a>釋放 WinSNMP 描述項

根據哪個元件配置描述項的記憶體而定，WinSNMP 程式設計環境會將描述元資源解除配置指派給 WinSNMP 的執行或 WinSNMP 應用程式。

若要釋放 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 或 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) 描述項的資源，則適用下列規則：

-   針對輸入參數

    由於 WinSNMP 應用程式會為具有可變長度的輸入物件配置記憶體，因此應用程式必須使用適當的函式釋放該記憶體。 例如，如果應用程式使用 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函式的呼叫來配置資源，則應該使用 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函式來解除配置資源。 如果應用程式使用 [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc) 函式的呼叫來配置資源，它應該呼叫 [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree) 函數。

-   針對輸出參數

    呼叫下列任何函式時，會導致執行配置為 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 或 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) 描述項配置記憶體： [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)、 [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)、 [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)、 [**SnmpCoNtextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)和 [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)。

    因為執行會為這些輸出物件配置記憶體，所以應用程式必須呼叫 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) 函式來解除配置資源。 此函式可讓執行程式釋放為這些結構的 **ptr** 成員所配置的記憶體。

若要釋放 [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)結構的資源，必須檢查 [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)結構的 **語法** 成員，以正確地評估結構的 **值** 成員。 如果 **語法** 成員指出 **值** 成員是 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) 或 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 描述元，且執行配置了描述項的資源，則應用程式必須呼叫 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)。 這可讓實作為釋放記憶體。 如果應用程式佈建了資源，就必須使用適當的函式來釋放記憶體，如先前所述。

如需詳細資訊，請參閱配置 [WinSNMP 記憶體物件](allocating-winsnmp-memory-objects.md)。

 

 