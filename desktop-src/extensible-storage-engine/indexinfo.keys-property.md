---
description: 深入瞭解： IndexInfo 的索引鍵屬性
title: IndexInfo 索引鍵屬性
TOCTitle: 'Keys property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.Keys
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.keys(v=EXCHG.10)
ms:contentKeyID: 55103265
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.Keys
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.Keys
- Microsoft.Isam.Esent.Interop.IndexInfo.get_Keys
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d96f9a6e92aeba02bf29ff53fff5f9f4a6c13b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980717"
---
# <a name="indexinfokeys-property"></a><span data-ttu-id="a0818-103">IndexInfo 索引鍵屬性</span><span class="sxs-lookup"><span data-stu-id="a0818-103">IndexInfo.Keys property</span></span>

<span data-ttu-id="a0818-104">取得索引中的唯一索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="a0818-104">Gets the number of unique keys in the index.</span></span> <span data-ttu-id="a0818-105">此值不是最新值，而且只會由 JetComputeStats 更新。</span><span class="sxs-lookup"><span data-stu-id="a0818-105">This value is not current and is only is updated by Api.JetComputeStats.</span></span>

<span data-ttu-id="a0818-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a0818-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a0818-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a0818-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a0818-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0818-108">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property Keys As Integer
    Get
'Usage
Dim instance As IndexInfo
Dim value As Integer

value = instance.Keys
```

``` csharp
public int Keys { get; }
```

#### <a name="property-value"></a><span data-ttu-id="a0818-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="a0818-109">Property value</span></span>

<span data-ttu-id="a0818-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a0818-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a0818-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0818-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0818-112">參考</span><span class="sxs-lookup"><span data-stu-id="a0818-112">Reference</span></span>

[<span data-ttu-id="a0818-113">IndexInfo 類別</span><span class="sxs-lookup"><span data-stu-id="a0818-113">IndexInfo class</span></span>](./indexinfo-class.md)

[<span data-ttu-id="a0818-114">IndexInfo 成員</span><span class="sxs-lookup"><span data-stu-id="a0818-114">IndexInfo members</span></span>](./indexinfo-members.md)

[<span data-ttu-id="a0818-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a0818-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
