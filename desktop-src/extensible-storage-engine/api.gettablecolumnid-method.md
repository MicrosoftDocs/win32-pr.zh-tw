---
description: 深入瞭解： GetTableColumnid 方法
title: GetTableColumnid 方法
TOCTitle: 'GetTableColumnid method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumnid(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumnid(v=EXCHG.10)
ms:contentKeyID: 55107215
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec91b014401709b6312b3363d8dae9e7da3d200e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510859"
---
# <a name="apigettablecolumnid-method"></a><span data-ttu-id="0c9fe-103">GetTableColumnid 方法</span><span class="sxs-lookup"><span data-stu-id="0c9fe-103">Api.GetTableColumnid method</span></span>

<span data-ttu-id="0c9fe-104">取得指定之資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="0c9fe-104">Get the columnid of the specified column.</span></span>

<span data-ttu-id="0c9fe-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c9fe-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c9fe-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0c9fe-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9fe-107">語法</span><span class="sxs-lookup"><span data-stu-id="0c9fe-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumnid ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String _
) As JET_COLUMNID
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim returnValue As JET_COLUMNID

returnValue = Api.GetTableColumnid(sesid, _
    tableid, columnName)
```

``` csharp
public static JET_COLUMNID GetTableColumnid(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName
)
```

#### <a name="parameters"></a><span data-ttu-id="0c9fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="0c9fe-108">Parameters</span></span>

  - <span data-ttu-id="0c9fe-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0c9fe-109">sesid</span></span>  
    <span data-ttu-id="0c9fe-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c9fe-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0c9fe-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="0c9fe-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c9fe-112">tableid</span><span class="sxs-lookup"><span data-stu-id="0c9fe-112">tableid</span></span>  
    <span data-ttu-id="0c9fe-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c9fe-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0c9fe-114">包含資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="0c9fe-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c9fe-115">columnName</span><span class="sxs-lookup"><span data-stu-id="0c9fe-115">columnName</span></span>  
    <span data-ttu-id="0c9fe-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0c9fe-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0c9fe-117">資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="0c9fe-117">The name of the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0c9fe-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c9fe-118">Return value</span></span>

<span data-ttu-id="0c9fe-119">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c9fe-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
<span data-ttu-id="0c9fe-120">資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c9fe-120">The id of the column.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0c9fe-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c9fe-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c9fe-122">參考</span><span class="sxs-lookup"><span data-stu-id="0c9fe-122">Reference</span></span>

[<span data-ttu-id="0c9fe-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="0c9fe-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0c9fe-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="0c9fe-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0c9fe-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0c9fe-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
