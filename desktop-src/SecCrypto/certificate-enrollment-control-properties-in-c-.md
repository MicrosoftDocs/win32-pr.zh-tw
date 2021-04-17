---
description: 傳回 HRESULT。 在此 HRESULT 中，S 的值 \_ 表示已成功執行方法。
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: C + + 中的憑證註冊控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511216"
---
# <a name="certificate-enrollment-control-properties-in-c"></a>C + + 中的憑證註冊控制項屬性

當您在 c + + 中設定或取出憑證註冊控制項屬性時，方法呼叫會傳回 **HRESULT**。 在此 **HRESULT** 中，S 的值 \_ 表示已成功執行方法。

以 c + + 撰寫的程式可透過下列形式的方法呼叫來抓取憑證註冊控制項屬性。


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



其中 *propertyName* 會指定所要存取的屬性名稱，而 *pPropValue* 則是適當資料類型之變數的指標。 成功完成此方法呼叫之後， *pPropValue* 會指向包含 *propertyName* 屬性值的變數。

例如，若要取出 **RootStoreType** 屬性的值，請使用下列程式碼。


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



以 c + + 撰寫的程式可以藉由呼叫下列格式的方法來設定憑證註冊控制項屬性。


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



其中 *propertyName* 指定要存取的屬性名稱，而 *PropValue* 是適當資料類型的值。 成功完成此方法呼叫之後， *propertyName* 屬性的新值將會是 *PropValue*。

例如，若要設定 **RootStoreType** 的屬性值，可以使用下列程式碼。


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



