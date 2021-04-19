---
description: 深入瞭解： JetGetCurrentIndex 方法
title: JetGetCurrentIndex 方法
TOCTitle: 'JetGetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bacc6973b1a105e128533a1116abdeb4c6cfafa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986317"
---
# <a name="apijetgetcurrentindex-method"></a><span data-ttu-id="bac8c-103">JetGetCurrentIndex 方法</span><span class="sxs-lookup"><span data-stu-id="bac8c-103">Api.JetGetCurrentIndex method</span></span>

<span data-ttu-id="bac8c-104">Ddetermines 指定資料指標目前索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="bac8c-104">Ddetermines the name of the current index of a given cursor.</span></span> <span data-ttu-id="bac8c-105">這個名稱也用來在稍後使用 [JetSetCurrentIndex (JET_SESID、JET_TABLEID、String) ](./api.jetsetcurrentindex-method.md)，重新選取該索引做為目前的索引。</span><span class="sxs-lookup"><span data-stu-id="bac8c-105">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex(JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span></span> <span data-ttu-id="bac8c-106">它也可以用來使用 JetGetTableIndexInfo 探索該索引的屬性。</span><span class="sxs-lookup"><span data-stu-id="bac8c-106">It can also be used to discover the properties of that index using JetGetTableIndexInfo.</span></span>

<span data-ttu-id="bac8c-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bac8c-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bac8c-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bac8c-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bac8c-109">語法</span><span class="sxs-lookup"><span data-stu-id="bac8c-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef indexName As String, _
    maxNameLength As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim maxNameLength As IntegerApi.JetGetCurrentIndex(sesid, tableid, _
    indexName, maxNameLength)
```

``` csharp
public static void JetGetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string indexName,
    int maxNameLength
)
```

#### <a name="parameters"></a><span data-ttu-id="bac8c-110">參數</span><span class="sxs-lookup"><span data-stu-id="bac8c-110">Parameters</span></span>

  - <span data-ttu-id="bac8c-111">sesid</span><span class="sxs-lookup"><span data-stu-id="bac8c-111">sesid</span></span>  
    <span data-ttu-id="bac8c-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bac8c-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bac8c-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="bac8c-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bac8c-114">tableid</span><span class="sxs-lookup"><span data-stu-id="bac8c-114">tableid</span></span>  
    <span data-ttu-id="bac8c-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bac8c-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bac8c-116">要取得索引名稱的資料指標。</span><span class="sxs-lookup"><span data-stu-id="bac8c-116">The cursor to get the index name for.</span></span>

<!-- end list -->

  - <span data-ttu-id="bac8c-117">IndexName</span><span class="sxs-lookup"><span data-stu-id="bac8c-117">indexName</span></span>  
    <span data-ttu-id="bac8c-118">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="bac8c-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="bac8c-119">傳回索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="bac8c-119">Returns the name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="bac8c-120">maxNameLength</span><span class="sxs-lookup"><span data-stu-id="bac8c-120">maxNameLength</span></span>  
    <span data-ttu-id="bac8c-121">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bac8c-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bac8c-122">索引名稱的最大長度。</span><span class="sxs-lookup"><span data-stu-id="bac8c-122">The maximum length of the index name.</span></span> <span data-ttu-id="bac8c-123">索引名稱不能超過 [NameMost](./systemparameters.namemost-field.md) 個字元。</span><span class="sxs-lookup"><span data-stu-id="bac8c-123">Index names are no more than [NameMost](./systemparameters.namemost-field.md) characters.</span></span>

## <a name="see-also"></a><span data-ttu-id="bac8c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bac8c-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bac8c-125">參考</span><span class="sxs-lookup"><span data-stu-id="bac8c-125">Reference</span></span>

[<span data-ttu-id="bac8c-126">Api 類別</span><span class="sxs-lookup"><span data-stu-id="bac8c-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bac8c-127">Api 成員</span><span class="sxs-lookup"><span data-stu-id="bac8c-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bac8c-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bac8c-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
