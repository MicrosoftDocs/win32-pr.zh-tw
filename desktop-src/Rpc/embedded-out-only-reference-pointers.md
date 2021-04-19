---
title: 內嵌的 Out-Only 參考指標
description: 內嵌的 Out-Only 參考指標
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072e9aa3cc3f0f673e4bb737016bc035a3ac496
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969928"
---
# <a name="embedded-out-only-reference-pointers"></a><span data-ttu-id="d8a52-103">內嵌的 Out-Only 參考指標</span><span class="sxs-lookup"><span data-stu-id="d8a52-103">Embedded Out-Only Reference Pointers</span></span>

<span data-ttu-id="d8a52-104">當您 \[ [](/windows/desktop/Midl/out-idl) \] 在 Microsoft RPC 中使用 out only 參考指標時，產生的伺服器 stub 只會配置可從參考指標存取的第一個指標層級。</span><span class="sxs-lookup"><span data-stu-id="d8a52-104">When you use \[[**out**](/windows/desktop/Midl/out-idl)\]-only reference pointers in Microsoft RPC, the generated server stubs allocate only the first level of pointers accessible from the reference pointer.</span></span> <span data-ttu-id="d8a52-105">較深層層級的指標不會由存根配置，但必須由伺服器應用層配置。</span><span class="sxs-lookup"><span data-stu-id="d8a52-105">Pointers at deeper levels are not allocated by the stubs, but must be allocated by the server application layer.</span></span> <span data-ttu-id="d8a52-106">例如，假設介面指定 \[  \] 參考指標的 out 陣列：</span><span class="sxs-lookup"><span data-stu-id="d8a52-106">For example, suppose an interface specifies an \[**out**\]-only array of reference pointers:</span></span>

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

<span data-ttu-id="d8a52-107">在此範例中，伺服器 stub 會為10個指標配置記憶體，並將每個指標的值設定為 null。</span><span class="sxs-lookup"><span data-stu-id="d8a52-107">In this example, the server stub allocates memory for 10 pointers and sets the value of each pointer to null.</span></span> <span data-ttu-id="d8a52-108">伺服器應用程式必須為指標所參考的10個 [**短**](/windows/desktop/Midl/short) 整數配置記憶體，然後設定10個指標以指向整數。</span><span class="sxs-lookup"><span data-stu-id="d8a52-108">The server application must allocate the memory for the 10 [**short**](/windows/desktop/Midl/short) integers referenced by the pointers and then set the 10 pointers to point to the integers.</span></span>

<span data-ttu-id="d8a52-109">當 \[ [](/windows/desktop/Midl/out-idl) \] 僅限輸出的資料結構包含嵌套參考指標時，伺服器存根只會配置參考指標可存取的第一個指標。</span><span class="sxs-lookup"><span data-stu-id="d8a52-109">When the \[[**out**](/windows/desktop/Midl/out-idl)\]-only data structure includes nested reference pointers, the server stubs allocate only the first pointer accessible from the reference pointer.</span></span> <span data-ttu-id="d8a52-110">例如：</span><span class="sxs-lookup"><span data-stu-id="d8a52-110">For example:</span></span>

``` syntax
/* IDL file (fragment) */
typedef struct 
{
    [ref] small * psValue;
} STRUCT1_TYPE;

typedef struct 
{
    [ref] STRUCT1_TYPE * ps1;
} STRUCT_TOP_TYPE;

Proc2([out, ref] STRUCT_TOP_TYPE * psTop);
```

<span data-ttu-id="d8a52-111">在上述範例中，伺服器 stub 會配置指標 *psTop* 和結構結構的 **\_ 最上層 \_ 類型**。</span><span class="sxs-lookup"><span data-stu-id="d8a52-111">In the preceding example, the server stubs allocate the pointer *psTop* and the structure **STRUCT\_TOP\_TYPE**.</span></span> <span data-ttu-id="d8a52-112">**結構 \_ TOP \_ 類型** 中的參考指標 *ps1* 設定為 null。</span><span class="sxs-lookup"><span data-stu-id="d8a52-112">The reference pointer *ps1* in **STRUCT\_TOP\_TYPE** is set to null.</span></span> <span data-ttu-id="d8a52-113">伺服器 stub 不會配置資料結構的每個層級，也不會配置 **STRUCT1 \_ 類型** 或其內嵌指標 *psValue*。</span><span class="sxs-lookup"><span data-stu-id="d8a52-113">The server stub does not allocate every level of the data structure, nor does it allocate the **STRUCT1\_TYPE** or its embedded pointer, *psValue*.</span></span>

 

 