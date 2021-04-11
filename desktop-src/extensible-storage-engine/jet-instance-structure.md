---
description: 深入瞭解： JET_INSTANCE 結構
title: JET_INSTANCE 結構
TOCTitle: JET_INSTANCE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INSTANCE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance(v=EXCHG.10)
ms:contentKeyID: 39510997
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a676c0815ba20b725da0216a7c9a145c1c1cfd68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193822"
---
# <a name="jet_instance-structure"></a><span data-ttu-id="c1ce4-103">JET_INSTANCE 結構</span><span class="sxs-lookup"><span data-stu-id="c1ce4-103">JET_INSTANCE structure</span></span>

<span data-ttu-id="c1ce4-104">JET_INSTANCE 包含資料庫實例的控制碼，可用於呼叫 JET API。</span><span class="sxs-lookup"><span data-stu-id="c1ce4-104">A JET_INSTANCE contains a handle to the instance of the database to use for calls to the JET API.</span></span>

<span data-ttu-id="c1ce4-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c1ce4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c1ce4-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c1ce4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c1ce4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1ce4-107">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INSTANCE _
    Implements IEquatable(Of JET_INSTANCE), IFormattable
'Usage
Dim instance As JET_INSTANCE
```

``` csharp
public struct JET_INSTANCE : IEquatable<JET_INSTANCE>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="c1ce4-108">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="c1ce4-108">Thread safety</span></span>

<span data-ttu-id="c1ce4-109">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c1ce4-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c1ce4-110">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="c1ce4-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1ce4-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1ce4-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c1ce4-112">參考</span><span class="sxs-lookup"><span data-stu-id="c1ce4-112">Reference</span></span>

[<span data-ttu-id="c1ce4-113">JET_INSTANCE 成員</span><span class="sxs-lookup"><span data-stu-id="c1ce4-113">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="c1ce4-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c1ce4-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
