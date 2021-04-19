---
description: 深入瞭解：資料表類別
title: Table 類別
TOCTitle: Table class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table(v=EXCHG.10)
ms:contentKeyID: 55104053
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ea12d7bd59d946c7375150862cd8fa0c87ba6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973261"
---
# <a name="table-class"></a><span data-ttu-id="f8936-103">Table 類別</span><span class="sxs-lookup"><span data-stu-id="f8936-103">Table class</span></span>

<span data-ttu-id="f8936-104">封裝可處置物件中之 JET_TABLEID 的類別。</span><span class="sxs-lookup"><span data-stu-id="f8936-104">A class that encapsulates a JET_TABLEID in a disposable object.</span></span> <span data-ttu-id="f8936-105">這會開啟現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="f8936-105">This opens an existing table.</span></span> <span data-ttu-id="f8936-106">若要建立資料表，請使用 JetCreateTable 方法。</span><span class="sxs-lookup"><span data-stu-id="f8936-106">To create a table use the JetCreateTable method.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f8936-107">繼承階層</span><span class="sxs-lookup"><span data-stu-id="f8936-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="f8936-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="f8936-108">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f8936-109">EsentResource （.）</span><span class="sxs-lookup"><span data-stu-id="f8936-109">Microsoft.Isam.Esent.Interop.EsentResource</span></span>](./esentresource-class.md)  
    <span data-ttu-id="f8936-110">Microsoft. Esent. Interop. 資料表</span><span class="sxs-lookup"><span data-stu-id="f8936-110">Microsoft.Isam.Esent.Interop.Table</span></span>  

<span data-ttu-id="f8936-111">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8936-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8936-112">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f8936-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8936-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8936-113">Syntax</span></span>

``` vb
'Declaration
Public Class Table _
    Inherits EsentResource
'Usage
Dim instance As Table
```

``` csharp
public class Table : EsentResource
```

## <a name="thread-safety"></a><span data-ttu-id="f8936-114">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="f8936-114">Thread safety</span></span>

<span data-ttu-id="f8936-115">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="f8936-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f8936-116">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="f8936-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8936-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8936-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8936-118">參考</span><span class="sxs-lookup"><span data-stu-id="f8936-118">Reference</span></span>

[<span data-ttu-id="f8936-119">資料表成員</span><span class="sxs-lookup"><span data-stu-id="f8936-119">Table members</span></span>](./table-members.md)

[<span data-ttu-id="f8936-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f8936-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
