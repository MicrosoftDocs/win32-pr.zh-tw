---
description: 深入瞭解： JET_SIGNATURE 結構
title: JET_SIGNATURE 結構
TOCTitle: JET_SIGNATURE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SIGNATURE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature(v=EXCHG.10)
ms:contentKeyID: 39511048
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5c8ce12b23194aea2a45c273e0207f88faad6f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989923"
---
# <a name="jet_signature-structure"></a><span data-ttu-id="82947-103">JET_SIGNATURE 結構</span><span class="sxs-lookup"><span data-stu-id="82947-103">JET_SIGNATURE structure</span></span>

<span data-ttu-id="82947-104">JET_SIGNATURE 結構包含可唯一識別資料庫或記錄檔順序的資訊。</span><span class="sxs-lookup"><span data-stu-id="82947-104">The JET_SIGNATURE structure contains information that uniquely identifies a database or logfile sequence.</span></span>

<span data-ttu-id="82947-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82947-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82947-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="82947-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82947-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="82947-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_SIGNATURE _
    Implements IEquatable(Of JET_SIGNATURE)
'Usage
Dim instance As JET_SIGNATURE
```

``` csharp
[SerializableAttribute]
public struct JET_SIGNATURE : IEquatable<JET_SIGNATURE>
```

## <a name="thread-safety"></a><span data-ttu-id="82947-108">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="82947-108">Thread safety</span></span>

<span data-ttu-id="82947-109">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="82947-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="82947-110">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="82947-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="82947-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82947-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82947-112">參考</span><span class="sxs-lookup"><span data-stu-id="82947-112">Reference</span></span>

[<span data-ttu-id="82947-113">JET_SIGNATURE 成員</span><span class="sxs-lookup"><span data-stu-id="82947-113">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="82947-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="82947-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
