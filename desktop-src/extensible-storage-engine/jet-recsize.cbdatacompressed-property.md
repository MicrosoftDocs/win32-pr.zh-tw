---
description: 深入瞭解： JET_RECSIZE cbDataCompressed 屬性
title: 'JET_RECSIZE. cbDataCompressed 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cbDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cbdatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515358
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbDataCompressed
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 747c2f00077f6a9d13de059f742bacc9a7936d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689588"
---
# <a name="jet_recsizecbdatacompressed-property"></a><span data-ttu-id="04aec-103">JET_RECSIZE cbDataCompressed 屬性</span><span class="sxs-lookup"><span data-stu-id="04aec-103">JET_RECSIZE.cbDataCompressed property</span></span>

<span data-ttu-id="04aec-104">取得記錄中使用者資料的壓縮大小。</span><span class="sxs-lookup"><span data-stu-id="04aec-104">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="04aec-105">如果沒有將內建的 long 值壓縮) ，這就會與 [cbData](./jet-recsize.cbdata-property.md) 相同。</span><span class="sxs-lookup"><span data-stu-id="04aec-105">This is the same as [cbData](./jet-recsize.cbdata-property.md) if no intrinsic long-values are compressed).</span></span>

<span data-ttu-id="04aec-106">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="04aec-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="04aec-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="04aec-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="04aec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="04aec-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbDataCompressed
```

``` csharp
public long cbDataCompressed { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="04aec-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="04aec-109">Property value</span></span>

<span data-ttu-id="04aec-110">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="04aec-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="04aec-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04aec-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="04aec-112">參考</span><span class="sxs-lookup"><span data-stu-id="04aec-112">Reference</span></span>

[<span data-ttu-id="04aec-113">JET_RECSIZE 結構</span><span class="sxs-lookup"><span data-stu-id="04aec-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="04aec-114">JET_RECSIZE 成員</span><span class="sxs-lookup"><span data-stu-id="04aec-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="04aec-115">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="04aec-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
