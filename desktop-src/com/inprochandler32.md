---
title: InprocHandler32
description: InprocHandler32 指定應用程式是否在 HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID 登錄機碼中使用自訂處理常式。
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- InprocHandler32 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd686657f9ce8f91938ccbf190a295a86e3d3b6480815c521c69f96c859fd621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919115"
---
# <a name="inprochandler32"></a>InprocHandler32

指定應用程式是否使用自訂處理常式。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值，可指定應用程式所使用的自訂處理常式。 如果未使用自訂處理常式，則應該將專案設定為 Ole32.dll。

如果容器正在搜尋自訂處理常式的登錄，16位版本的優先順序會和16位容器相同，且32位版本的優先順序會與32位容器相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**InprocHandler**](inprochandler.md)
</dt> </dl>

 

 




