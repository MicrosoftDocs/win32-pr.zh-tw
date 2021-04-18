---
title: 介面主體中的資料類型
description: 介面主體（以大括弧 ( ) 括住）包含將在遠端程序呼叫中使用的資料類型，以及將從遠端執行之函式的原型。
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- 介面 MIDL、資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968420"
---
# <a name="data-types-in-the-interface-body"></a><span data-ttu-id="e48fb-104">介面主體中的資料類型</span><span class="sxs-lookup"><span data-stu-id="e48fb-104">Data Types in the Interface Body</span></span>

<span data-ttu-id="e48fb-105">介面主體（以大括弧 ( {} ) 括住）包含將在遠端程序呼叫中使用的資料類型，以及將從遠端執行之函式的原型。</span><span class="sxs-lookup"><span data-stu-id="e48fb-105">The interface body, which is enclosed in braces ({ }), contains the data types that will be used in remote procedure calls and prototypes for the functions that will be executed remotely.</span></span> <span data-ttu-id="e48fb-106">介面主體可以包含 imports、pragma、常數宣告、型別宣告和函式宣告。</span><span class="sxs-lookup"><span data-stu-id="e48fb-106">An interface body can contain imports, pragmas, constant declarations, type declarations, and function declarations.</span></span> <span data-ttu-id="e48fb-107">除了在憑證相容性模式中，MIDL 編譯器也允許變數定義形式的隱含宣告。</span><span class="sxs-lookup"><span data-stu-id="e48fb-107">Except in OSF-compatibility mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="e48fb-108">請注意，RPC 介面的憑證-DCE 規格不允許單一 IDL 檔案中有多個介面。</span><span class="sxs-lookup"><span data-stu-id="e48fb-108">Note that the OSF-DCE specification for RPC interfaces does not allow multiple interfaces in a single IDL file.</span></span> <span data-ttu-id="e48fb-109">因此，如果您要在 MIDL 的憑證相容性模式中進行編譯 ( [**/osf**](-osf.md)) ，您的 IDL 檔案只能包含一個介面。</span><span class="sxs-lookup"><span data-stu-id="e48fb-109">Therefore, if you are compiling in MIDL's OSF-compatibility mode ( [**/osf**](-osf.md)), your IDL file can contain only one interface.</span></span>

<span data-ttu-id="e48fb-110">如需使用 MIDL 編譯器來產生類型程式庫的詳細資訊，請參閱使用 [Midl 產生類型程式庫](generating-a-type-library-with-midl-2.md)。</span><span class="sxs-lookup"><span data-stu-id="e48fb-110">For details on using the MIDL compiler to produce type libraries, see [Generating a Type Library with MIDL](generating-a-type-library-with-midl-2.md).</span></span>

<span data-ttu-id="e48fb-111">在 Microsoft RPC 中，IDL 檔案可以包含多個介面，且這些介面可在定義) 的 IDL 檔案內 (向前宣告。</span><span class="sxs-lookup"><span data-stu-id="e48fb-111">In Microsoft RPC, an IDL file can contain multiple interfaces and these interfaces can be forward declared (within the IDL file that defines them).</span></span> <span data-ttu-id="e48fb-112">例如：</span><span class="sxs-lookup"><span data-stu-id="e48fb-112">For example:</span></span>

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




