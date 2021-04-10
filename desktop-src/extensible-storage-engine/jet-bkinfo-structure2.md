---
description: 深入瞭解： JET_BKINFO 結構
title: JET_BKINFO 結構
TOCTitle: JET_BKINFO structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo(v=EXCHG.10)
ms:contentKeyID: 39511166
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c3b0d3178abaa90fe507c06a2a997472492643c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194613"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="a11a7-103">JET_BKINFO 結構</span><span class="sxs-lookup"><span data-stu-id="a11a7-103">JET_BKINFO structure</span></span>

<span data-ttu-id="a11a7-104">保存有關特定備份事件的資料集合。</span><span class="sxs-lookup"><span data-stu-id="a11a7-104">Holds a collection of data about a specific backup event.</span></span>

<span data-ttu-id="a11a7-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a11a7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a11a7-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a11a7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a11a7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a11a7-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKINFO _
    Implements IEquatable(Of JET_BKINFO), INullableJetStruct
'Usage
Dim instance As JET_BKINFO
```

``` csharp
[SerializableAttribute]
public struct JET_BKINFO : IEquatable<JET_BKINFO>, 
    INullableJetStruct
```

## <a name="thread-safety"></a><span data-ttu-id="a11a7-108">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="a11a7-108">Thread safety</span></span>

<span data-ttu-id="a11a7-109">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a11a7-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a11a7-110">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="a11a7-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a11a7-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a11a7-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a11a7-112">參考</span><span class="sxs-lookup"><span data-stu-id="a11a7-112">Reference</span></span>

[<span data-ttu-id="a11a7-113">JET_BKINFO 成員</span><span class="sxs-lookup"><span data-stu-id="a11a7-113">JET_BKINFO members</span></span>](./jet-bkinfo-members.md)

[<span data-ttu-id="a11a7-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a11a7-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
