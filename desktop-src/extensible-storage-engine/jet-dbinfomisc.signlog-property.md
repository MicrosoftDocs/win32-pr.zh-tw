---
description: 深入瞭解： JET_DBINFOMISC signLog 屬性
title: JET_DBINFOMISC signLog 屬性
TOCTitle: 'signLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.signlog(v=EXCHG.10)
ms:contentKeyID: 39511875
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_signLog
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_signLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d75fed42b966cafe159f224667d0d30a85cc1a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112113"
---
# <a name="jet_dbinfomiscsignlog-property"></a><span data-ttu-id="576d9-103">JET_DBINFOMISC signLog 屬性</span><span class="sxs-lookup"><span data-stu-id="576d9-103">JET_DBINFOMISC.signLog property</span></span>

<span data-ttu-id="576d9-104">取得用來修改資料庫之記錄檔的記錄檔簽章。</span><span class="sxs-lookup"><span data-stu-id="576d9-104">Gets the logfile signature of logs used to modify the database.</span></span>

<span data-ttu-id="576d9-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="576d9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="576d9-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="576d9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="576d9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="576d9-107">Syntax</span></span>

``` vb
'Declaration
Public Property signLog As JET_SIGNATURE
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_SIGNATURE

value = instance.signLog
```

``` csharp
public JET_SIGNATURE signLog { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="576d9-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="576d9-108">Property value</span></span>

<span data-ttu-id="576d9-109">類型： [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="576d9-109">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="576d9-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="576d9-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="576d9-111">參考</span><span class="sxs-lookup"><span data-stu-id="576d9-111">Reference</span></span>

[<span data-ttu-id="576d9-112">JET_DBINFOMISC 類別</span><span class="sxs-lookup"><span data-stu-id="576d9-112">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="576d9-113">JET_DBINFOMISC 成員</span><span class="sxs-lookup"><span data-stu-id="576d9-113">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="576d9-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="576d9-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
