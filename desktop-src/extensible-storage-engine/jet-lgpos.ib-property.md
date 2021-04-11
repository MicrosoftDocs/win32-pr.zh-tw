---
description: 深入瞭解： JET_LGPOS ib 屬性
title: JET_LGPOS ib 屬性
TOCTitle: 'ib property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_LGPOS.ib
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.ib(v=EXCHG.10)
ms:contentKeyID: 39512783
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.ib
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.set_ib
- Microsoft.Isam.Esent.Interop.JET_LGPOS.get_ib
- Microsoft.Isam.Esent.Interop.JET_LGPOS.ib
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 330b18005ac1cc4fca085eeae2233a5851d03f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320492"
---
# <a name="jet_lgposib-property"></a><span data-ttu-id="4dd02-103">JET_LGPOS ib 屬性</span><span class="sxs-lookup"><span data-stu-id="4dd02-103">JET_LGPOS.ib property</span></span>

<span data-ttu-id="4dd02-104">取得或設定這個記錄位置所表示的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="4dd02-104">Gets or sets the byte offset represented by this log position.</span></span> <span data-ttu-id="4dd02-105">此位移是在磁區內。</span><span class="sxs-lookup"><span data-stu-id="4dd02-105">This offset is inside of the sector.</span></span>

<span data-ttu-id="4dd02-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4dd02-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4dd02-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4dd02-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd02-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dd02-108">Syntax</span></span>

``` vb
'Declaration
Public Property ib As Integer
    Get
    Set
'Usage
Dim instance As JET_LGPOS
Dim value As Integer

value = instance.ib

instance.ib = value
```

``` csharp
public int ib { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="4dd02-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="4dd02-109">Property value</span></span>

<span data-ttu-id="4dd02-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4dd02-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="4dd02-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dd02-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4dd02-112">參考</span><span class="sxs-lookup"><span data-stu-id="4dd02-112">Reference</span></span>

[<span data-ttu-id="4dd02-113">JET_LGPOS 結構</span><span class="sxs-lookup"><span data-stu-id="4dd02-113">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="4dd02-114">JET_LGPOS 成員</span><span class="sxs-lookup"><span data-stu-id="4dd02-114">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="4dd02-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4dd02-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
