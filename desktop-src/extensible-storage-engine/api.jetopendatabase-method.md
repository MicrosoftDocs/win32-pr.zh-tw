---
description: 深入瞭解： JetOpenDatabase 方法
title: JetOpenDatabase 方法
TOCTitle: 'JetOpenDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopendatabase(v=EXCHG.10)
ms:contentKeyID: 55100768
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faaff0eec2b5bc8a2c2f2a72a61f9f6a23f7d972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195029"
---
# <a name="apijetopendatabase-method"></a><span data-ttu-id="b7c48-103">JetOpenDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="b7c48-103">Api.JetOpenDatabase method</span></span>

<span data-ttu-id="b7c48-104">開啟先前附加了 [JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) ](./api.jetattachdatabase-method.md)的資料庫，以搭配資料庫會話使用。</span><span class="sxs-lookup"><span data-stu-id="b7c48-104">Opens a database previously attached with [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md), for use with a database session.</span></span> <span data-ttu-id="b7c48-105">您可以針對相同的資料庫多次呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="b7c48-105">This function can be called multiple times for the same database.</span></span>

<span data-ttu-id="b7c48-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7c48-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7c48-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b7c48-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c48-108">語法</span><span class="sxs-lookup"><span data-stu-id="b7c48-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    connect As String, _
    <OutAttribute> ByRef dbid As JET_DBID, _
    grbit As OpenDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim connect As String
Dim dbid As JET_DBID
Dim grbit As OpenDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetOpenDatabase(sesid, _
    database, connect, dbid, grbit)
```

``` csharp
public static JET_wrn JetOpenDatabase(
    JET_SESID sesid,
    string database,
    string connect,
    out JET_DBID dbid,
    OpenDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b7c48-109">參數</span><span class="sxs-lookup"><span data-stu-id="b7c48-109">Parameters</span></span>

  - <span data-ttu-id="b7c48-110">sesid</span><span class="sxs-lookup"><span data-stu-id="b7c48-110">sesid</span></span>  
    <span data-ttu-id="b7c48-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b7c48-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b7c48-112">開啟資料庫的會話。</span><span class="sxs-lookup"><span data-stu-id="b7c48-112">The session that is opening the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c48-113">[資料庫]</span><span class="sxs-lookup"><span data-stu-id="b7c48-113">database</span></span>  
    <span data-ttu-id="b7c48-114">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b7c48-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b7c48-115">要開啟的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b7c48-115">The database to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c48-116">連線</span><span class="sxs-lookup"><span data-stu-id="b7c48-116">connect</span></span>  
    <span data-ttu-id="b7c48-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b7c48-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b7c48-118">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="b7c48-118">Reserved for future use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c48-119">dbid</span><span class="sxs-lookup"><span data-stu-id="b7c48-119">dbid</span></span>  
    <span data-ttu-id="b7c48-120">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b7c48-120">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="b7c48-121">傳回附加資料庫的 dbid。</span><span class="sxs-lookup"><span data-stu-id="b7c48-121">Returns the dbid of the attached database.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7c48-122">grbit</span><span class="sxs-lookup"><span data-stu-id="b7c48-122">grbit</span></span>  
    <span data-ttu-id="b7c48-123">型別： [OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="b7c48-123">Type: [Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit](./opendatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b7c48-124">開啟資料庫選項。</span><span class="sxs-lookup"><span data-stu-id="b7c48-124">Open database options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b7c48-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7c48-125">Return value</span></span>

<span data-ttu-id="b7c48-126">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b7c48-126">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="b7c48-127">ESENT 警告碼。</span><span class="sxs-lookup"><span data-stu-id="b7c48-127">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b7c48-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7c48-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7c48-129">參考</span><span class="sxs-lookup"><span data-stu-id="b7c48-129">Reference</span></span>

[<span data-ttu-id="b7c48-130">Api 類別</span><span class="sxs-lookup"><span data-stu-id="b7c48-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b7c48-131">Api 成員</span><span class="sxs-lookup"><span data-stu-id="b7c48-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b7c48-132">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b7c48-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
