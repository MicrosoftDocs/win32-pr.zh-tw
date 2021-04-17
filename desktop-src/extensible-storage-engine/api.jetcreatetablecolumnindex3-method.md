---
description: 深入瞭解： JetCreateTableColumnIndex3 方法
title: JetCreateTableColumnIndex3 方法
TOCTitle: 'JetCreateTableColumnIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetablecolumnindex3(v=EXCHG.10)
ms:contentKeyID: 55100678
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a967db8f6a322ac29ba8a1e9352972ff1f4f4b76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468857"
---
# <a name="apijetcreatetablecolumnindex3-method"></a><span data-ttu-id="09c48-103">JetCreateTableColumnIndex3 方法</span><span class="sxs-lookup"><span data-stu-id="09c48-103">Api.JetCreateTableColumnIndex3 method</span></span>

<span data-ttu-id="09c48-104">建立資料表，並在該資料表上加入資料行和索引。</span><span class="sxs-lookup"><span data-stu-id="09c48-104">Creates a table, adds columns, and indices on that table.</span></span>

<span data-ttu-id="09c48-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09c48-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="09c48-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="09c48-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09c48-107">語法</span><span class="sxs-lookup"><span data-stu-id="09c48-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTableColumnIndex3 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablecreate As JET_TABLECREATE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablecreate As JET_TABLECREATEApi.JetCreateTableColumnIndex3(sesid, _
    dbid, tablecreate)
```

``` csharp
public static void JetCreateTableColumnIndex3(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLECREATE tablecreate
)
```

#### <a name="parameters"></a><span data-ttu-id="09c48-108">參數</span><span class="sxs-lookup"><span data-stu-id="09c48-108">Parameters</span></span>

  - <span data-ttu-id="09c48-109">sesid</span><span class="sxs-lookup"><span data-stu-id="09c48-109">sesid</span></span>  
    <span data-ttu-id="09c48-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09c48-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="09c48-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="09c48-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="09c48-112">dbid</span><span class="sxs-lookup"><span data-stu-id="09c48-112">dbid</span></span>  
    <span data-ttu-id="09c48-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09c48-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="09c48-114">要加入新資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="09c48-114">The database to which to add the new table.</span></span>

<!-- end list -->

  - <span data-ttu-id="09c48-115">tablecreate</span><span class="sxs-lookup"><span data-stu-id="09c48-115">tablecreate</span></span>  
    <span data-ttu-id="09c48-116">類型： [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="09c48-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span></span>  
    
    <span data-ttu-id="09c48-117">描述要建立之資料表的物件。</span><span class="sxs-lookup"><span data-stu-id="09c48-117">Object describing the table to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="09c48-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09c48-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09c48-119">參考</span><span class="sxs-lookup"><span data-stu-id="09c48-119">Reference</span></span>

[<span data-ttu-id="09c48-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="09c48-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="09c48-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="09c48-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="09c48-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="09c48-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
