---
title: InprocHandler
description: InprocHandler 指定應用程式是否在 HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID 登錄機碼中使用自訂處理常式。
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404731"
---
# <a name="inprochandler"></a>InprocHandler

指定應用程式是否使用自訂處理常式。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值，可指定應用程式所使用的自訂處理常式。 如果未使用自訂處理常式，則應該將專案設定為 Ole32.dll。

如果容器正在搜尋自訂處理常式的登錄，16位版本的優先順序會和16位容器相同，且32位版本的優先順序會與32位容器相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




