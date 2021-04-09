---
description: 網路監視器會呼叫 FormatProperties 函式來格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: 執行 FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112797"
---
# <a name="implementing-formatproperties"></a>執行 FormatProperties

網路監視器會呼叫 [**FormatProperties**](formatproperties.md) 函式來格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。 一般來說，會呼叫 **FormatProperties** 來格式化通訊協定的摘要行，然後格式化框架內的所有通訊協定屬性實例。 不過，網路監視器不會識別針對特定剖析器呼叫 **FormatProperties** 的次數。

呼叫 [**FormatProperties**](formatproperties.md)時，網路監視器為其顯示的每個屬性提供 [**PROPERTYINST**](propertyinst.md) 結構。 **PROPERTYINST** 結構提供要顯示之資料的相關資訊，包括 [**PROPERTYINFO**](propertyinfo.md)結構的指標，此結構會指定用來格式化顯示的資料屬性的函式。

> [!Note]  
> 將屬性加入至剖析器的 [*屬性資料庫*](p.md)時，會指定 [**PROPERTYINFO**](propertyinfo.md)結構。

 

網路監視器識別要針對每個屬性實例呼叫的格式函數。 [**PROPERTYINFO**](propertyinfo.md)結構的 **InstanceData** 成員可以指定下列各項：

-   [**FormatPropertyInstance**](formatpropertyinstance.md)函式，使用網路監視器提供的 [*一般格式*](g.md)器。

    -或-

-   剖析器所提供的自訂格式函數名稱。

[**FormatPropertyInstance**](formatpropertyinstance.md)和自訂格式函數會傳回在網路監視器 UI 的詳細資料窗格中所顯示的格式化資料。

下圖顯示網路監視器如何識別要針對每個屬性實例呼叫的函數。

![網路監視器如何識別要呼叫的函式](images/formatprop1.png)

下列程式識別執行 [**FormatProperties**](formatproperties.md)所需的步驟。

**若要執行 FormatProperties**

-   使用迴圈結構，針對傳遞給 [**FormatProperties**](formatproperties.md)函式之 *lpPropInst* 參數中的剖析器，呼叫每個 [**PROPERTYINST**](propertyinst.md)結構的格式函數。

以下是 [**FormatProperties**](formatproperties.md)的基本執行。

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



