---
description: '深入瞭解： JetGetDatabaseInfo 方法 (JET_SESID、JET_DBID、JET_DBINFOMISC JET_DbInfo) '
title: 'JetGetDatabaseInfo 方法 (JET_SESID、JET_DBID、JET_DBINFOMISC JET_DbInfo) '
TOCTitle: JetGetDatabaseInfo method (JET_SESID, JET_DBID, JET_DBINFOMISC, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_DBINFOMISC@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabaseinfo(v=EXCHG.10)
ms:contentKeyID: 55100710
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 402cf796f75cc6d9ec8a272281b767cc068a455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026146"
---
# <a name="apijetgetdatabaseinfo-method-jet_sesid-jet_dbid-jet_dbinfomisc-jet_dbinfo"></a><span data-ttu-id="66e40-103">JetGetDatabaseInfo 方法 (JET_SESID、JET_DBID、JET_DBINFOMISC JET_DbInfo) </span><span class="sxs-lookup"><span data-stu-id="66e40-103">Api.JetGetDatabaseInfo method (JET_SESID, JET_DBID, JET_DBINFOMISC, JET_DbInfo)</span></span>

<span data-ttu-id="66e40-104">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="66e40-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="66e40-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66e40-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="66e40-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="66e40-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66e40-107">語法</span><span class="sxs-lookup"><span data-stu-id="66e40-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    <OutAttribute> ByRef dbinfomisc As JET_DBINFOMISC, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim dbinfomisc As JET_DBINFOMISC
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseInfo(sesid, dbid, _
    dbinfomisc, infoLevel)
```

``` csharp
public static void JetGetDatabaseInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    out JET_DBINFOMISC dbinfomisc,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="66e40-108">參數</span><span class="sxs-lookup"><span data-stu-id="66e40-108">Parameters</span></span>

  - <span data-ttu-id="66e40-109">sesid</span><span class="sxs-lookup"><span data-stu-id="66e40-109">sesid</span></span>  
    <span data-ttu-id="66e40-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66e40-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="66e40-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="66e40-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="66e40-112">dbid</span><span class="sxs-lookup"><span data-stu-id="66e40-112">dbid</span></span>  
    <span data-ttu-id="66e40-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66e40-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="66e40-114">資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="66e40-114">The database identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="66e40-115">dbinfomisc</span><span class="sxs-lookup"><span data-stu-id="66e40-115">dbinfomisc</span></span>  
    <span data-ttu-id="66e40-116">類型： [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span><span class="sxs-lookup"><span data-stu-id="66e40-116">Type: [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span></span>  
    
    <span data-ttu-id="66e40-117">要擷取的值。</span><span class="sxs-lookup"><span data-stu-id="66e40-117">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="66e40-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="66e40-118">infoLevel</span></span>  
    <span data-ttu-id="66e40-119">類型： [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="66e40-119">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="66e40-120">要取出的特定資料。</span><span class="sxs-lookup"><span data-stu-id="66e40-120">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="66e40-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66e40-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66e40-122">參考</span><span class="sxs-lookup"><span data-stu-id="66e40-122">Reference</span></span>

[<span data-ttu-id="66e40-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="66e40-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="66e40-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="66e40-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="66e40-125">JetGetDatabaseInfo 多載</span><span class="sxs-lookup"><span data-stu-id="66e40-125">JetGetDatabaseInfo overload</span></span>](./api.jetgetdatabaseinfo-method.md)

[<span data-ttu-id="66e40-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="66e40-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
