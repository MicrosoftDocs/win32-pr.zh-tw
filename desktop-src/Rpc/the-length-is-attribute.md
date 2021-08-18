---
title: Length_is 屬性
description: '\ Size \_ 是 \ 屬性，可讓您指定陣列的大小上限。'
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436559961d815adb417d83de5ffa8c06d8497fa0899644411d252c84d6e34ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924257"
---
# <a name="the-length_is-attribute"></a>\[長度 \_ 為 \] 屬性

[ \[ [**大小 \_ 為**](/windows/desktop/Midl/size-is)] \] 屬性可讓您指定陣列的大小上限。 當這是唯一的屬性時，就會傳送陣列的所有元素。 您可以不傳送陣列的所有元素，而是使用 [ \[ [**長度 \_ 為**](/windows/desktop/Midl/length-is)] 屬性來指定傳送的元素，如下所示 \] ：

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(3.0)
]
interface arraytest
{
  void fArray3([in] short sSize,
               [in] short sLength
               [in, out, size_is(sSize), 
                 length_is(sLength)] char achArray[*]);
}
```

大小描述配置，且長度描述傳輸。 傳送的元素數目必須一律小於或等於配置的元素數目。 與 length 相關聯的值一律小於或等於 **size \_**。 **\_**

 

 