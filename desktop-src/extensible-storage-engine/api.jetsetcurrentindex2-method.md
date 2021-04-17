---
description: 深入瞭解： JetSetCurrentIndex2 方法
title: JetSetCurrentIndex2 方法
TOCTitle: 'JetSetCurrentIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex2(v=EXCHG.10)
ms:contentKeyID: 55100798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e08e1fe5027641348259381d74b34ce16b034e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386137"
---
# <a name="apijetsetcurrentindex2-method"></a><span data-ttu-id="1a190-103">JetSetCurrentIndex2 方法</span><span class="sxs-lookup"><span data-stu-id="1a190-103">Api.JetSetCurrentIndex2 method</span></span>

<span data-ttu-id="1a190-104">設定資料指標的目前索引。</span><span class="sxs-lookup"><span data-stu-id="1a190-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="1a190-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a190-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a190-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1a190-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a190-107">語法</span><span class="sxs-lookup"><span data-stu-id="1a190-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbitApi.JetSetCurrentIndex2(sesid, _
    tableid, index, grbit)
```

``` csharp
public static void JetSetCurrentIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1a190-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a190-108">Parameters</span></span>

  - <span data-ttu-id="1a190-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1a190-109">sesid</span></span>  
    <span data-ttu-id="1a190-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a190-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1a190-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1a190-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a190-112">tableid</span><span class="sxs-lookup"><span data-stu-id="1a190-112">tableid</span></span>  
    <span data-ttu-id="1a190-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a190-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1a190-114">要在其上設定索引的資料指標。</span><span class="sxs-lookup"><span data-stu-id="1a190-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a190-115">索引</span><span class="sxs-lookup"><span data-stu-id="1a190-115">index</span></span>  
    <span data-ttu-id="1a190-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1a190-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1a190-117">要選取之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a190-117">The name of the index to be selected.</span></span> <span data-ttu-id="1a190-118">如果這是 null 或空白，則會選取主要索引。</span><span class="sxs-lookup"><span data-stu-id="1a190-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a190-119">grbit</span><span class="sxs-lookup"><span data-stu-id="1a190-119">grbit</span></span>  
    <span data-ttu-id="1a190-120">型別： [SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="1a190-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1a190-121">設定索引選項。</span><span class="sxs-lookup"><span data-stu-id="1a190-121">Set index options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a190-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a190-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a190-123">參考</span><span class="sxs-lookup"><span data-stu-id="1a190-123">Reference</span></span>

[<span data-ttu-id="1a190-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1a190-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1a190-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1a190-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1a190-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1a190-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
