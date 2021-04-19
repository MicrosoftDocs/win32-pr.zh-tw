---
description: '深入瞭解： JetGetObjectInfo 方法 (JET_SESID、JET_DBID、JET_objtyp、字串、JET_OBJECTINFO) '
title: 'JetGetObjectInfo 方法 (JET_SESID、JET_DBID、JET_objtyp、字串、JET_OBJECTINFO) '
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_objtyp,System.String,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100733
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01311dcfbba226405a3c46c1be4c4553eac4eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972186"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objtyp-string-jet_objectinfo"></a><span data-ttu-id="9d2be-103">JetGetObjectInfo 方法 (JET_SESID、JET_DBID、JET_objtyp、字串、JET_OBJECTINFO) </span><span class="sxs-lookup"><span data-stu-id="9d2be-103">Api.JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</span></span>

<span data-ttu-id="9d2be-104">抓取資料庫物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9d2be-104">Retrieves information about database objects.</span></span>

<span data-ttu-id="9d2be-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9d2be-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9d2be-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9d2be-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9d2be-107">語法</span><span class="sxs-lookup"><span data-stu-id="9d2be-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    objtyp As JET_objtyp, _
    objectName As String, _
    <OutAttribute> ByRef objectinfo As JET_OBJECTINFO _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objtyp As JET_objtyp
Dim objectName As String
Dim objectinfo As JET_OBJECTINFOApi.JetGetObjectInfo(sesid, dbid, _
    objtyp, objectName, objectinfo)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_objtyp objtyp,
    string objectName,
    out JET_OBJECTINFO objectinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="9d2be-108">參數</span><span class="sxs-lookup"><span data-stu-id="9d2be-108">Parameters</span></span>

  - <span data-ttu-id="9d2be-109">sesid</span><span class="sxs-lookup"><span data-stu-id="9d2be-109">sesid</span></span>  
    <span data-ttu-id="9d2be-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9d2be-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9d2be-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="9d2be-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d2be-112">dbid</span><span class="sxs-lookup"><span data-stu-id="9d2be-112">dbid</span></span>  
    <span data-ttu-id="9d2be-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9d2be-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="9d2be-114">要使用的資料庫。</span><span class="sxs-lookup"><span data-stu-id="9d2be-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d2be-115">objtyp</span><span class="sxs-lookup"><span data-stu-id="9d2be-115">objtyp</span></span>  
    <span data-ttu-id="9d2be-116">類型： [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9d2be-116">Type: [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="9d2be-117">物件的類型。</span><span class="sxs-lookup"><span data-stu-id="9d2be-117">The type of the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d2be-118">objectName</span><span class="sxs-lookup"><span data-stu-id="9d2be-118">objectName</span></span>  
    <span data-ttu-id="9d2be-119">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9d2be-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9d2be-120">要取得其資訊的物件名稱。</span><span class="sxs-lookup"><span data-stu-id="9d2be-120">The object name about which to retrieve information.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d2be-121">objectinfo</span><span class="sxs-lookup"><span data-stu-id="9d2be-121">objectinfo</span></span>  
    <span data-ttu-id="9d2be-122">類型： [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="9d2be-122">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span></span>  
    
    <span data-ttu-id="9d2be-123">填入資料庫中物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9d2be-123">Filled in with information about the objects in the database.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d2be-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d2be-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9d2be-125">參考</span><span class="sxs-lookup"><span data-stu-id="9d2be-125">Reference</span></span>

[<span data-ttu-id="9d2be-126">Api 類別</span><span class="sxs-lookup"><span data-stu-id="9d2be-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9d2be-127">Api 成員</span><span class="sxs-lookup"><span data-stu-id="9d2be-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9d2be-128">JetGetObjectInfo 多載</span><span class="sxs-lookup"><span data-stu-id="9d2be-128">JetGetObjectInfo overload</span></span>](./api.jetgetobjectinfo-method.md)

[<span data-ttu-id="9d2be-129">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9d2be-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
