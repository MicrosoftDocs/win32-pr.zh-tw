---
description: 深入瞭解： JET_DBINFOMISC cbPageSize 屬性
title: JET_DBINFOMISC cbPageSize 屬性
TOCTitle: 'cbPageSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.cbpagesize(v=EXCHG.10)
ms:contentKeyID: 39512879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_cbPageSize
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_cbPageSize
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.cbPageSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae2f718c066c1b0cef347141f08e1ed1254e6bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970165"
---
# <a name="jet_dbinfomisccbpagesize-property"></a><span data-ttu-id="23e14-103">JET_DBINFOMISC cbPageSize 屬性</span><span class="sxs-lookup"><span data-stu-id="23e14-103">JET_DBINFOMISC.cbPageSize property</span></span>

<span data-ttu-id="23e14-104">取得資料庫頁面大小。</span><span class="sxs-lookup"><span data-stu-id="23e14-104">Gets the database page size.</span></span> <span data-ttu-id="23e14-105">值為0表示有 4 Kb 的頁面。</span><span class="sxs-lookup"><span data-stu-id="23e14-105">A value of 0 means 4Kb pages.</span></span>

<span data-ttu-id="23e14-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="23e14-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="23e14-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="23e14-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="23e14-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="23e14-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbPageSize As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.cbPageSize
```

``` csharp
public int cbPageSize { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="23e14-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="23e14-109">Property value</span></span>

<span data-ttu-id="23e14-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="23e14-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="23e14-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23e14-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="23e14-112">參考</span><span class="sxs-lookup"><span data-stu-id="23e14-112">Reference</span></span>

[<span data-ttu-id="23e14-113">JET_DBINFOMISC 類別</span><span class="sxs-lookup"><span data-stu-id="23e14-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="23e14-114">JET_DBINFOMISC 成員</span><span class="sxs-lookup"><span data-stu-id="23e14-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="23e14-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="23e14-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
