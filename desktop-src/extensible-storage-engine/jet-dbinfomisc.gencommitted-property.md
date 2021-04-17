---
description: 深入瞭解： JET_DBINFOMISC genCommitted 屬性
title: JET_DBINFOMISC genCommitted 屬性
TOCTitle: 'genCommitted property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genCommitted
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.gencommitted(v=EXCHG.10)
ms:contentKeyID: 39513072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genCommitted
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genCommitted
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_genCommitted
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_genCommitted
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a40612c535bed3bbfe345add1fd922b65e450fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511392"
---
# <a name="jet_dbinfomiscgencommitted-property"></a><span data-ttu-id="39c35-103">JET_DBINFOMISC genCommitted 屬性</span><span class="sxs-lookup"><span data-stu-id="39c35-103">JET_DBINFOMISC.genCommitted property</span></span>

<span data-ttu-id="39c35-104">取得認可至資料庫的最大記錄檔產生。</span><span class="sxs-lookup"><span data-stu-id="39c35-104">Gets the maximum log generation committed to the database.</span></span> <span data-ttu-id="39c35-105">通常是目前的記錄產生。</span><span class="sxs-lookup"><span data-stu-id="39c35-105">Typically the current log generation.</span></span>

<span data-ttu-id="39c35-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="39c35-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="39c35-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="39c35-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="39c35-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="39c35-108">Syntax</span></span>

``` vb
'Declaration
Public Property genCommitted As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.genCommitted
```

``` csharp
public int genCommitted { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="39c35-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="39c35-109">Property value</span></span>

<span data-ttu-id="39c35-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="39c35-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="39c35-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39c35-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="39c35-112">參考</span><span class="sxs-lookup"><span data-stu-id="39c35-112">Reference</span></span>

[<span data-ttu-id="39c35-113">JET_DBINFOMISC 類別</span><span class="sxs-lookup"><span data-stu-id="39c35-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="39c35-114">JET_DBINFOMISC 成員</span><span class="sxs-lookup"><span data-stu-id="39c35-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="39c35-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="39c35-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
