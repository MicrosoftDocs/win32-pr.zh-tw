---
title: PutEx 方法
description: IADs PutEx 方法會使用屬性名稱，將具有單一或多個值的屬性儲存至屬性快取中。
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PutEx ADSI，關於
- ADSI ADSI，範例程式碼 Visual Basic，使用 PutEx 方法
- 屬性 ADSI，將單一或多重值屬性儲存至屬性快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea698c2dd14f3ddf8f3ad97459fad598006db22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839124"
---
# <a name="the-putex-method"></a>PutEx 方法

[**IADs：:P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex)方法會使用屬性名稱，將具有單一或多個值的屬性儲存至屬性快取中。 這會覆寫目前在屬性快取中的任何值。 在 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 發生之前，快取中的值不會寫入基礎目錄服務。 **PutEx** 的第一個引數會指出您是否要取代或加入屬性的任何現有值。 在下列範例中，當呼叫 **PutEx** 時，會在快取中清除 **description** 屬性的任何現有值，並在呼叫 **SetInfo** 時于伺服器上清除。


```VB
Dim x As IADs
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------
' Assume the otherHomePhoneNumber has the following values:
' 111-1111, 222-2222
'----------------------------------------------
x.PutEx ADS_PROPERTY_APPEND, "OtherhomePhone", Array("333-3333" )  
x.SetInfo              'Now the values are 111-1111,222-222,333-3333.
 
x.PutEx ADS_PROPERTY_DELETE, "OtherHomePhone", Array("111-1111", "222-2222")
x.SetInfo              'Now the values are 333-3333.
x.PutEx ADS_PROPERTY_UPDATE, "OtherHomePhone", Array("888-8888", "999-9999")
x.SetInfo              'Now the values are 888-8888,999-9999.
x.PutEx ADS_PROPERTY_CLEAR, "OtherHomePhone",  vbNull
x.SetInfo              'Now the property has no value.
```



 

 




