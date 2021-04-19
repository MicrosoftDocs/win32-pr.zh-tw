---
description: 深入瞭解： JET_RECSIZE 結構
title: 'JET_RECSIZE 結構 (的結構) '
TOCTitle: JET_RECSIZE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize(v=EXCHG.10)
ms:contentKeyID: 39509765
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e741d91187a138d7b8d9a57d0c4e76f54979d99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970365"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="5ce91-103">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="5ce91-103">JET_RECSIZE structure</span></span>

<span data-ttu-id="5ce91-104">[JetGetRecordSize (JET_SESID、JET_TABLEID、JET_RECSIZE、GetRecordSizeGrbit) ](./vistaapi.jetgetrecordsize-method.md)用來傳回有關使用者資料空間中記錄的使用需求、設定的資料行數目、值數目，以及 ESENT 記錄結構額外負荷空間的資訊。</span><span class="sxs-lookup"><span data-stu-id="5ce91-104">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="5ce91-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="5ce91-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="5ce91-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5ce91-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce91-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ce91-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_RECSIZE _
    Implements IEquatable(Of JET_RECSIZE)
'Usage
Dim instance As JET_RECSIZE
```

``` csharp
[SerializableAttribute]
public struct JET_RECSIZE : IEquatable<JET_RECSIZE>
```

## <a name="thread-safety"></a><span data-ttu-id="5ce91-108">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="5ce91-108">Thread safety</span></span>

<span data-ttu-id="5ce91-109">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="5ce91-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5ce91-110">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="5ce91-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ce91-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ce91-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5ce91-112">參考</span><span class="sxs-lookup"><span data-stu-id="5ce91-112">Reference</span></span>

[<span data-ttu-id="5ce91-113">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="5ce91-113">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="5ce91-114">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="5ce91-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
