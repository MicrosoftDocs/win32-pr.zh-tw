---
description: 深入瞭解： JetDeleteIndex 方法
title: JetDeleteIndex 方法
TOCTitle: 'JetDeleteIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeleteindex(v=EXCHG.10)
ms:contentKeyID: 55100682
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de04966aae4aee3f4ab7b14a846b898f55f887be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511140"
---
# <a name="apijetdeleteindex-method"></a><span data-ttu-id="1ae9a-103">JetDeleteIndex 方法</span><span class="sxs-lookup"><span data-stu-id="1ae9a-103">Api.JetDeleteIndex method</span></span>

<span data-ttu-id="1ae9a-104">從資料庫資料表中刪除索引。</span><span class="sxs-lookup"><span data-stu-id="1ae9a-104">Deletes an index from a database table.</span></span>

<span data-ttu-id="1ae9a-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ae9a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ae9a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1ae9a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae9a-107">語法</span><span class="sxs-lookup"><span data-stu-id="1ae9a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As StringApi.JetDeleteIndex(sesid, tableid, _
    index)
```

``` csharp
public static void JetDeleteIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index
)
```

#### <a name="parameters"></a><span data-ttu-id="1ae9a-108">參數</span><span class="sxs-lookup"><span data-stu-id="1ae9a-108">Parameters</span></span>

  - <span data-ttu-id="1ae9a-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1ae9a-109">sesid</span></span>  
    <span data-ttu-id="1ae9a-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1ae9a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1ae9a-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1ae9a-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ae9a-112">tableid</span><span class="sxs-lookup"><span data-stu-id="1ae9a-112">tableid</span></span>  
    <span data-ttu-id="1ae9a-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1ae9a-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1ae9a-114">要刪除索引之資料表上的資料指標。</span><span class="sxs-lookup"><span data-stu-id="1ae9a-114">A cursor on the table to delete the index from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ae9a-115">索引</span><span class="sxs-lookup"><span data-stu-id="1ae9a-115">index</span></span>  
    <span data-ttu-id="1ae9a-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1ae9a-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1ae9a-117">要刪除的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae9a-117">The name of the index to be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ae9a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ae9a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ae9a-119">參考</span><span class="sxs-lookup"><span data-stu-id="1ae9a-119">Reference</span></span>

[<span data-ttu-id="1ae9a-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1ae9a-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1ae9a-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1ae9a-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1ae9a-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1ae9a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
