---
description: 深入瞭解： JET_SESID 結構
title: JET_SESID 結構
TOCTitle: JET_SESID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid(v=EXCHG.10)
ms:contentKeyID: 39516065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f547425f40b4336213ef69abe4bba07ee1baa513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973028"
---
# <a name="jet_sesid-structure"></a><span data-ttu-id="4d47f-103">JET_SESID 結構</span><span class="sxs-lookup"><span data-stu-id="4d47f-103">JET_SESID structure</span></span>

<span data-ttu-id="4d47f-104">JET_SESID 包含會話的控制碼，可用於呼叫 JET APIr。</span><span class="sxs-lookup"><span data-stu-id="4d47f-104">A JET_SESID contains a handle to the session to use for calls to the JET APIr-.</span></span>

<span data-ttu-id="4d47f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d47f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d47f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4d47f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d47f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d47f-107">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_SESID _
    Implements IEquatable(Of JET_SESID), IFormattable
'Usage
Dim instance As JET_SESID
```

``` csharp
public struct JET_SESID : IEquatable<JET_SESID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="4d47f-108">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="4d47f-108">Thread safety</span></span>

<span data-ttu-id="4d47f-109">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="4d47f-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4d47f-110">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="4d47f-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d47f-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d47f-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d47f-112">參考</span><span class="sxs-lookup"><span data-stu-id="4d47f-112">Reference</span></span>

[<span data-ttu-id="4d47f-113">JET_SESID 成員</span><span class="sxs-lookup"><span data-stu-id="4d47f-113">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="4d47f-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4d47f-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
