---
title: Max_is 屬性
description: 您可以使用 \ max 為 \ 屬性來指定陣列索引編號的有效範圍 \_ 。
ms.assetid: b629e3cf-544d-47ee-8f8f-b049f693897c
keywords:
- max_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8901f952a55de6b81143b0e615c878d8599fb354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186081"
---
# <a name="the-max_is-attribute"></a>\[Max \_ 為 \] 屬性

您可以使用 \[ [**max \_ 為**](/windows/desktop/Midl/max-is)屬性，指定陣列索引編號的有效範圍 \] 。

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(5.0)
]
interface arraytest
{
  void fArray5([in] short sMax,
               [in, out, max_is(sMax)]  char achArray[]);
}
```

 

 