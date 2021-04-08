---
title: 晚期繫結支援
description: 當晚期繫結支援就緒時，每個函式呼叫都必須經過 ADSI IDispatch 介面，然後再重新路由至適當的延伸模組。
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- 擴充功能 ADSI，晚期繫結支援
- ADSI ADSI，範例程式碼 Visual Basic，晚期繫結支援
- binding AD，晚期繫結支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e4dd1de0000d9edbe3e73cbc47b81d094d48c2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683110"
---
# <a name="late-binding-support"></a>晚期繫結支援

當晚期繫結支援就緒時，每個函式呼叫都必須經過 ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面，然後再重新路由至適當的延伸模組。

請考慮下列程式碼範例。


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



沒有明確呼叫 **QueryInterface** 方法可取得延伸模組。 延伸模組必須將其 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 呼叫重新路由傳送至 ADSI **IDispatch** 介面。 ADSI 會進行決策並解決發生的任何衝突，然後使用名為 [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)的介面重新路由回適當的延伸模組。 因此，任何支援晚期繫結的延伸模組都必須執行 **IADsExtension**。

 

 