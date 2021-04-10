---
description: 深入瞭解： JET_DBID 結構
title: JET_DBID 結構
TOCTitle: JET_DBID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DBID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid(v=EXCHG.10)
ms:contentKeyID: 39515255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e92373015b64593936ee8d447b619932d168157c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849756"
---
# <a name="jet_dbid-structure"></a><span data-ttu-id="ed6c8-103">JET_DBID 結構</span><span class="sxs-lookup"><span data-stu-id="ed6c8-103">JET_DBID structure</span></span>

<span data-ttu-id="ed6c8-104">JET_DBID 包含資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ed6c8-104">A JET_DBID contains the handle to the database.</span></span> <span data-ttu-id="ed6c8-105">資料庫控制碼是用來管理資料庫的架構。</span><span class="sxs-lookup"><span data-stu-id="ed6c8-105">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="ed6c8-106">它也可以用來管理該資料庫內的資料表。</span><span class="sxs-lookup"><span data-stu-id="ed6c8-106">It can also be used to manage the tables inside of that database.</span></span>

<span data-ttu-id="ed6c8-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed6c8-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ed6c8-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ed6c8-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed6c8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed6c8-109">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_DBID _
    Implements IEquatable(Of JET_DBID), IFormattable
'Usage
Dim instance As JET_DBID
```

``` csharp
public struct JET_DBID : IEquatable<JET_DBID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="ed6c8-110">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="ed6c8-110">Thread safety</span></span>

<span data-ttu-id="ed6c8-111">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ed6c8-111">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ed6c8-112">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ed6c8-112">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed6c8-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed6c8-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed6c8-114">參考</span><span class="sxs-lookup"><span data-stu-id="ed6c8-114">Reference</span></span>

[<span data-ttu-id="ed6c8-115">JET_DBID 成員</span><span class="sxs-lookup"><span data-stu-id="ed6c8-115">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="ed6c8-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ed6c8-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
