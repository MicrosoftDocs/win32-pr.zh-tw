---
description: 深入瞭解： GetColumnDictionary 方法
title: GetColumnDictionary 方法
TOCTitle: 'GetColumnDictionary method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getcolumndictionary(v=EXCHG.10)
ms:contentKeyID: 55100653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab359c5b8b163ce67f576f35250dd521eb14472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991804"
---
# <a name="apigetcolumndictionary-method"></a><span data-ttu-id="1806d-103">GetColumnDictionary 方法</span><span class="sxs-lookup"><span data-stu-id="1806d-103">Api.GetColumnDictionary method</span></span>

<span data-ttu-id="1806d-104">建立將資料行名稱對應至其資料行識別碼的字典。</span><span class="sxs-lookup"><span data-stu-id="1806d-104">Creates a dictionary which maps column names to their column IDs.</span></span>

<span data-ttu-id="1806d-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1806d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1806d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1806d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1806d-107">語法</span><span class="sxs-lookup"><span data-stu-id="1806d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetColumnDictionary ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IDictionary(Of String, JET_COLUMNID)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IDictionary(Of String, JET_COLUMNID)

returnValue = Api.GetColumnDictionary(sesid, _
    tableid)
```

``` csharp
public static IDictionary<string, JET_COLUMNID> GetColumnDictionary(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="1806d-108">參數</span><span class="sxs-lookup"><span data-stu-id="1806d-108">Parameters</span></span>

  - <span data-ttu-id="1806d-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1806d-109">sesid</span></span>  
    <span data-ttu-id="1806d-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1806d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1806d-111">要使用的 sesid。</span><span class="sxs-lookup"><span data-stu-id="1806d-111">The sesid to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1806d-112">tableid</span><span class="sxs-lookup"><span data-stu-id="1806d-112">tableid</span></span>  
    <span data-ttu-id="1806d-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1806d-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1806d-114">要取得其資訊的資料表。</span><span class="sxs-lookup"><span data-stu-id="1806d-114">The table to retrieve the information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1806d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1806d-115">Return value</span></span>

<span data-ttu-id="1806d-116">型別： [system.object](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span><span class="sxs-lookup"><span data-stu-id="1806d-116">Type: [System.Collections.Generic.IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span></span>  
<span data-ttu-id="1806d-117">將資料行名稱對應至資料行識別碼的字典。</span><span class="sxs-lookup"><span data-stu-id="1806d-117">A dictionary mapping column names to column IDs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1806d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1806d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1806d-119">參考</span><span class="sxs-lookup"><span data-stu-id="1806d-119">Reference</span></span>

[<span data-ttu-id="1806d-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1806d-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1806d-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1806d-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1806d-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1806d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
