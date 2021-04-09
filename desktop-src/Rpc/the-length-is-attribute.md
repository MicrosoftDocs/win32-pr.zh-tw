---
title: Length_is 屬性
description: '\ Size \_ 是 \ 屬性，可讓您指定陣列的大小上限。'
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f49ad63b2546d39dcc00d251f39143b7eec354c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682980"
---
# <a name="the-length_is-attribute"></a><span data-ttu-id="491ab-104">\[長度 \_ 為 \] 屬性</span><span class="sxs-lookup"><span data-stu-id="491ab-104">The \[length\_is\] Attribute</span></span>

<span data-ttu-id="491ab-105">[ \[ [**大小 \_ 為**](/windows/desktop/Midl/size-is)] \] 屬性可讓您指定陣列的大小上限。</span><span class="sxs-lookup"><span data-stu-id="491ab-105">The \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute lets you specify the maximum size of the array.</span></span> <span data-ttu-id="491ab-106">當這是唯一的屬性時，就會傳送陣列的所有元素。</span><span class="sxs-lookup"><span data-stu-id="491ab-106">When this is the only attribute, all elements of the array are transmitted.</span></span> <span data-ttu-id="491ab-107">您可以不傳送陣列的所有元素，而是使用 [ \[ [**長度 \_ 為**](/windows/desktop/Midl/length-is)] 屬性來指定傳送的元素，如下所示 \] ：</span><span class="sxs-lookup"><span data-stu-id="491ab-107">Instead of sending all elements of the array, you can specify the transmitted elements using the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute, as follows:</span></span>

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

<span data-ttu-id="491ab-108">大小描述配置，且長度描述傳輸。</span><span class="sxs-lookup"><span data-stu-id="491ab-108">Size describes allocation while length describes transmission.</span></span> <span data-ttu-id="491ab-109">傳送的元素數目必須一律小於或等於配置的元素數目。</span><span class="sxs-lookup"><span data-stu-id="491ab-109">The number of elements transmitted must always be less than or equal to the number of elements allocated.</span></span> <span data-ttu-id="491ab-110">與 length 相關聯的值一律小於或等於 **size \_**。 **\_**</span><span class="sxs-lookup"><span data-stu-id="491ab-110">The value associated with **length\_is** is always less than or equal to **size\_is**.</span></span>

 

 