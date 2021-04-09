---
title: 遞增編碼範例
description: 下一節會提供範例，說明如何使用類型編碼的遞增樣式序列化控制碼。
ms.assetid: c50c0de3-aabb-4166-93dc-67b0fee66635
keywords:
- 使用遞增編碼的遠端程序呼叫 RPC、工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16c9cb61e6b2bf55b29fb02e39f41dd7a61c8317
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932561"
---
# <a name="examples-of-incremental-encoding"></a><span data-ttu-id="46ec5-104">遞增編碼範例</span><span class="sxs-lookup"><span data-stu-id="46ec5-104">Examples of Incremental Encoding</span></span>

<span data-ttu-id="46ec5-105">下一節會提供範例，說明如何使用類型編碼的遞增樣式序列化控制碼。</span><span class="sxs-lookup"><span data-stu-id="46ec5-105">The following section provides an example of how to use the incremental style serializing handle for type encoding.</span></span>

``` syntax
/* This is an acf file. MooType is defined in the idl file */

[    explicit_handle
]
interface regress
{
typedef [ encode,decode ] MooType;
}
```

<span data-ttu-id="46ec5-106">下列摘要表示相關的應用程式片段。</span><span class="sxs-lookup"><span data-stu-id="46ec5-106">The following excerpt represents the relevant application fragments.</span></span>


```C++
if (MesEncodeIncrementalHandleCreate (State, AllocFn, WriteFn, 
    &Handle) == RPC_S_OK)
{
//...
/* The serialize works from the beginning of the buffer because
    the handle is in the initial state. The Moo_Encode does the
    following:
    - sizes *pMooObject for marshalling,
    - calls AllocFn with the size obtained,
    - marshalls into the buffer returned by Alloc, and
    - calls WriteFn with the filled buffer 
*/

Moo_Encode ( Handle, pMooObject );
...
}
if (MesIncrementalHandleReset (Handle, NULL, NULL, NULL, ReadFn,
    MES_DECODE ) == RPC_OK)
{
/*The ReadFn is needed to reset the handle. The arguments
    that are NULL do not change. You can also call 
    MesDecodeIncrementalHandleCreate (State, ReadFn, &Handle);
    The Moo_Decode does the following:
    - calls Read with the appropriate size of data to read and
        receives a buffer with the data
    - unmarshalls the object from the buffer into *pMooObject 
*/

Moo_Decode ( Handle, pMooObject );
//...
MesHandleFree ( Handle );
}
```



 

 




