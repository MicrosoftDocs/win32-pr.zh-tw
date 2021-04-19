---
description: 深入瞭解： JetSetCurrentIndex 方法
title: JetSetCurrentIndex 方法
TOCTitle: 'JetSetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed3c069962fe879e250f90e34744780dfe2eb862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978171"
---
# <a name="apijetsetcurrentindex-method"></a><span data-ttu-id="69c0b-103">JetSetCurrentIndex 方法</span><span class="sxs-lookup"><span data-stu-id="69c0b-103">Api.JetSetCurrentIndex method</span></span>

<span data-ttu-id="69c0b-104">設定資料指標的目前索引。</span><span class="sxs-lookup"><span data-stu-id="69c0b-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="69c0b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69c0b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69c0b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="69c0b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69c0b-107">語法</span><span class="sxs-lookup"><span data-stu-id="69c0b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As StringApi.JetSetCurrentIndex(sesid, tableid, _
    index)
```

``` csharp
public static void JetSetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index
)
```

#### <a name="parameters"></a><span data-ttu-id="69c0b-108">參數</span><span class="sxs-lookup"><span data-stu-id="69c0b-108">Parameters</span></span>

  - <span data-ttu-id="69c0b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="69c0b-109">sesid</span></span>  
    <span data-ttu-id="69c0b-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69c0b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="69c0b-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="69c0b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="69c0b-112">tableid</span><span class="sxs-lookup"><span data-stu-id="69c0b-112">tableid</span></span>  
    <span data-ttu-id="69c0b-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69c0b-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="69c0b-114">要在其上設定索引的資料指標。</span><span class="sxs-lookup"><span data-stu-id="69c0b-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="69c0b-115">索引</span><span class="sxs-lookup"><span data-stu-id="69c0b-115">index</span></span>  
    <span data-ttu-id="69c0b-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="69c0b-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="69c0b-117">要選取之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="69c0b-117">The name of the index to be selected.</span></span> <span data-ttu-id="69c0b-118">如果這是 null 或空白，則會選取主要索引。</span><span class="sxs-lookup"><span data-stu-id="69c0b-118">If this is null or empty the primary index will be selected.</span></span>

## <a name="see-also"></a><span data-ttu-id="69c0b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69c0b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69c0b-120">參考</span><span class="sxs-lookup"><span data-stu-id="69c0b-120">Reference</span></span>

[<span data-ttu-id="69c0b-121">Api 類別</span><span class="sxs-lookup"><span data-stu-id="69c0b-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="69c0b-122">Api 成員</span><span class="sxs-lookup"><span data-stu-id="69c0b-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="69c0b-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="69c0b-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
