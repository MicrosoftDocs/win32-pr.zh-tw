---
description: 深入瞭解： JET_INDEXCREATE cbKeyMost 屬性
title: JET_INDEXCREATE cbKeyMost 屬性
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850731"
---
# <a name="jet_indexcreatecbkeymost-property"></a><span data-ttu-id="a5542-103">JET_INDEXCREATE cbKeyMost 屬性</span><span class="sxs-lookup"><span data-stu-id="a5542-103">JET_INDEXCREATE.cbKeyMost property</span></span>

<span data-ttu-id="a5542-104">取得或設定索引中索引鍵允許的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a5542-104">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="a5542-105">最小支援的金鑰大小為 JET_cbKeyMostMin (255) 這是舊版的最大金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="a5542-105">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="a5542-106">最大索引鍵大小取決於資料庫頁面大小 [DatabasePageSize](./jet-param-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="a5542-106">The maximum key size is dependent on the database page size [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="a5542-107">您可以使用 [KeyMost](./systemparameters.keymost-property.md)抓取最大的索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="a5542-107">The maximum key size can be retrieved with [KeyMost](./systemparameters.keymost-property.md).</span></span> <span data-ttu-id="a5542-108">Windows XP 和 Windows Server 2003 會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="a5542-108">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a5542-109">不同于非受控 API，不需要 **IndexKeyMost ()** (JET_bitIndexKeyMost) ，它會自動加入。</span><span class="sxs-lookup"><span data-stu-id="a5542-109">Unlike the unmanaged API, **IndexKeyMost()** (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span>

<span data-ttu-id="a5542-110">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a5542-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a5542-111">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a5542-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a5542-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5542-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="a5542-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="a5542-113">Property value</span></span>

<span data-ttu-id="a5542-114">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a5542-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5542-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5542-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a5542-116">參考</span><span class="sxs-lookup"><span data-stu-id="a5542-116">Reference</span></span>

[<span data-ttu-id="a5542-117">JET_INDEXCREATE 類別</span><span class="sxs-lookup"><span data-stu-id="a5542-117">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="a5542-118">JET_INDEXCREATE 成員</span><span class="sxs-lookup"><span data-stu-id="a5542-118">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="a5542-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a5542-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
