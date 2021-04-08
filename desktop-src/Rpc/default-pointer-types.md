---
title: 預設指標類型
description: 指標不需要有明確的屬性描述。 未提供明確屬性時，MIDL 編譯器會使用預設指標屬性。
ms.assetid: b90619c3-70b4-44f0-ba37-293595281031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c565fe8019567fd1fe319d7b34287d9729bbe1d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023791"
---
# <a name="default-pointer-types"></a><span data-ttu-id="17dde-104">預設指標類型</span><span class="sxs-lookup"><span data-stu-id="17dde-104">Default Pointer Types</span></span>

<span data-ttu-id="17dde-105">指標不需要有明確的屬性描述。</span><span class="sxs-lookup"><span data-stu-id="17dde-105">Pointers are not required to have an explicit attribute description.</span></span> <span data-ttu-id="17dde-106">未提供明確屬性時，MIDL 編譯器會使用預設指標屬性。</span><span class="sxs-lookup"><span data-stu-id="17dde-106">When an explicit attribute is not provided, the MIDL Compiler uses a default pointer attribute.</span></span>

<span data-ttu-id="17dde-107">未歸屬指標的預設案例如下：</span><span class="sxs-lookup"><span data-stu-id="17dde-107">The default cases for unattributed pointers are the following:</span></span>

-   <span data-ttu-id="17dde-108">出現在參數清單中的最上層指標預設為 \[ [**ref**](/windows/desktop/Midl/ref) \] 指標。</span><span class="sxs-lookup"><span data-stu-id="17dde-108">Top-level pointers that appear in parameter lists default to \[[**ref**](/windows/desktop/Midl/ref)\] pointers.</span></span>
-   <span data-ttu-id="17dde-109">所有其他指標都會預設為 \[ [**指標 \_ 預設**](/windows/desktop/Midl/pointer-default)屬性所指定的類型 \] 。</span><span class="sxs-lookup"><span data-stu-id="17dde-109">All other pointers default to the type specified by the \[[**pointer\_default**](/windows/desktop/Midl/pointer-default)\] attribute.</span></span> <span data-ttu-id="17dde-110">如果未 \[ 提供任何 **指標 \_ 預設** 屬性，當 Midl 編譯器處於 \] Microsoft 擴充模式時，這些指標會預設為 \[ [**唯一**](/windows/desktop/Midl/unique) \] 屬性， [](microsoft-rpc-binding-handle-extensions.md)或 \[ [](/windows/desktop/Midl/ptr) \] 當 midl 編譯器處於 DCE 相容模式時，則會預設為 ptr 屬性。</span><span class="sxs-lookup"><span data-stu-id="17dde-110">When no \[**pointer\_default**\] attribute is supplied, these pointers default to the \[ [**unique**](/windows/desktop/Midl/unique) \] attribute when the MIDL compiler is in [Microsoft Extensions](microsoft-rpc-binding-handle-extensions.md) mode or the \[[**ptr**](/windows/desktop/Midl/ptr)\] attribute when the MIDL compiler is in DCE-compatible mode.</span></span>

<span data-ttu-id="17dde-111">當遠端程式傳回指標時，傳回值必須是 \[ [**唯一**](/windows/desktop/Midl/unique) \] 或完整的 (\[ [**ptr**](/windows/desktop/Midl/ptr) \]) 指標。</span><span class="sxs-lookup"><span data-stu-id="17dde-111">When a remote procedure returns a pointer, the return value must be a \[ [**unique**](/windows/desktop/Midl/unique) \] or full (\[ [**ptr**](/windows/desktop/Midl/ptr) \]) pointer.</span></span>

``` syntax
/* IDL file compiled without /osf */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0),
  pointer_default(ptr)
]
interface MyInterface
{
    typedef long *PLONG;
  
    struct MyCircularList {
        struct MyCircularList *pRight;
        struct MyCircularList *pLeft;
        long Data;
    };

    void Foo1( [in] PLONG p );                   // p is ref
 
    void Foo2( [in] struct MyCircularList *p );  // p is ref, p->pRight and p->pLeft is ptr

    struct MyCircularList *Foo3( void );         // returned pointer is ptr.    
}

[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea46),
  version(1.0)
]
interface MyInterface2
{
    struct MySingleList
       {
       struct MySingleList *pNext;
       long Data;
       };
    void Foo4( [in] struct MySingleList *p );  // p is ref, p->pNext is unique

    struct MySingleList *Foo5( void );         // returned pointer is unique.    
}
```

### <a name="remarks"></a><span data-ttu-id="17dde-112">備註</span><span class="sxs-lookup"><span data-stu-id="17dde-112">Remarks</span></span>

<span data-ttu-id="17dde-113">為確保明確的指標屬性行為，請在定義指標時一律使用明確的指標屬性。</span><span class="sxs-lookup"><span data-stu-id="17dde-113">To ensure unambiguous pointer-attribute behavior, always use explicit pointer attributes when defining a pointer.</span></span>

<span data-ttu-id="17dde-114">建議 **\[** **\]** 只有在需要指標別名時使用 ptr。</span><span class="sxs-lookup"><span data-stu-id="17dde-114">It is recommended that **\[** ptr **\]** is used only when pointer aliasing is required.</span></span>

 

 