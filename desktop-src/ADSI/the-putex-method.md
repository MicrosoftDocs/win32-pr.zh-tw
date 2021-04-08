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
# <a name="the-putex-method"></a><span data-ttu-id="1b950-106">PutEx 方法</span><span class="sxs-lookup"><span data-stu-id="1b950-106">The PutEx Method</span></span>

<span data-ttu-id="1b950-107">[**IADs：:P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex)方法會使用屬性名稱，將具有單一或多個值的屬性儲存至屬性快取中。</span><span class="sxs-lookup"><span data-stu-id="1b950-107">The [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the name of a property to save a property with single or multiple values into the property cache.</span></span> <span data-ttu-id="1b950-108">這會覆寫目前在屬性快取中的任何值。</span><span class="sxs-lookup"><span data-stu-id="1b950-108">This overwrites any value currently in the property cache.</span></span> <span data-ttu-id="1b950-109">在 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 發生之前，快取中的值不會寫入基礎目錄服務。</span><span class="sxs-lookup"><span data-stu-id="1b950-109">The values in the cache are not written to the underlying directory service until an [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) occurs.</span></span> <span data-ttu-id="1b950-110">**PutEx** 的第一個引數會指出您是否要取代或加入屬性的任何現有值。</span><span class="sxs-lookup"><span data-stu-id="1b950-110">The first argument of **PutEx** indicates whether you want to replace or add to any existing values for the property.</span></span> <span data-ttu-id="1b950-111">在下列範例中，當呼叫 **PutEx** 時，會在快取中清除 **description** 屬性的任何現有值，並在呼叫 **SetInfo** 時于伺服器上清除。</span><span class="sxs-lookup"><span data-stu-id="1b950-111">In the following example, any existing values of the **description** attribute are erased in the cache when **PutEx** is called, and erased on the server when **SetInfo** is called.</span></span>


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



 

 




