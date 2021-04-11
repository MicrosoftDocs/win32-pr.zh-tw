---
description: 深入瞭解： JET_OPENTEMPORARYTABLE prgcolumnid 屬性
title: 'JET_OPENTEMPORARYTABLE. prgcolumnid 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'prgcolumnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.prgcolumnid(v=EXCHG.10)
ms:contentKeyID: 55104133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd6516e01d08de32f7962a48d2caca69ddbf0427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945180"
---
# <a name="jet_opentemporarytableprgcolumnid-property"></a><span data-ttu-id="4fc8c-103">JET_OPENTEMPORARYTABLE prgcolumnid 屬性</span><span class="sxs-lookup"><span data-stu-id="4fc8c-103">JET_OPENTEMPORARYTABLE.prgcolumnid property</span></span>

<span data-ttu-id="4fc8c-104">取得或設定輸出緩衝區，此緩衝區會接收建立臨時表時所產生之資料行識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="4fc8c-104">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="4fc8c-105">此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。</span><span class="sxs-lookup"><span data-stu-id="4fc8c-105">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="4fc8c-106">因此，這個緩衝區的大小必須對應到 [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md)的大小。</span><span class="sxs-lookup"><span data-stu-id="4fc8c-106">As a result, the size of this buffer must correspond to the size of [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md).</span></span>

<span data-ttu-id="4fc8c-107">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="4fc8c-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="4fc8c-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4fc8c-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc8c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fc8c-109">Syntax</span></span>

``` vb
'Declaration
Public Property prgcolumnid As JET_COLUMNID()
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_COLUMNID()

value = instance.prgcolumnid

instance.prgcolumnid = value
```

``` csharp
public JET_COLUMNID[] prgcolumnid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="4fc8c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="4fc8c-110">Property value</span></span>

<span data-ttu-id="4fc8c-111">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="4fc8c-111">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="4fc8c-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fc8c-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4fc8c-113">參考</span><span class="sxs-lookup"><span data-stu-id="4fc8c-113">Reference</span></span>

[<span data-ttu-id="4fc8c-114">JET_OPENTEMPORARYTABLE 類別</span><span class="sxs-lookup"><span data-stu-id="4fc8c-114">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="4fc8c-115">JET_OPENTEMPORARYTABLE 成員</span><span class="sxs-lookup"><span data-stu-id="4fc8c-115">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="4fc8c-116">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="4fc8c-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
