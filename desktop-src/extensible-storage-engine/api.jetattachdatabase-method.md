---
description: 深入瞭解： JetAttachDatabase 方法
title: JetAttachDatabase 方法
TOCTitle: 'JetAttachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100652
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0447d4e6c5e8474c4d82340e35a23692096305bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111944"
---
# <a name="apijetattachdatabase-method"></a><span data-ttu-id="2d91f-103">JetAttachDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="2d91f-103">Api.JetAttachDatabase method</span></span>

<span data-ttu-id="2d91f-104">附加資料庫檔案以與資料庫實例搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2d91f-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="2d91f-105">若要使用資料庫，就必須使用 [JetOpenDatabase (JET_SESID、string、string、JET_DBID、OpenDatabaseGrbit) ](./api.jetopendatabase-method.md)來開啟它。</span><span class="sxs-lookup"><span data-stu-id="2d91f-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="2d91f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2d91f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2d91f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2d91f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2d91f-108">語法</span><span class="sxs-lookup"><span data-stu-id="2d91f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase(sesid, _
    database, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase(
    JET_SESID sesid,
    string database,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="2d91f-109">參數</span><span class="sxs-lookup"><span data-stu-id="2d91f-109">Parameters</span></span>

  - <span data-ttu-id="2d91f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="2d91f-110">sesid</span></span>  
    <span data-ttu-id="2d91f-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2d91f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2d91f-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="2d91f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2d91f-113">[資料庫]</span><span class="sxs-lookup"><span data-stu-id="2d91f-113">database</span></span>  
    <span data-ttu-id="2d91f-114">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2d91f-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2d91f-115">要附加的資料庫。</span><span class="sxs-lookup"><span data-stu-id="2d91f-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="2d91f-116">grbit</span><span class="sxs-lookup"><span data-stu-id="2d91f-116">grbit</span></span>  
    <span data-ttu-id="2d91f-117">型別： [AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="2d91f-117">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2d91f-118">附加選項。</span><span class="sxs-lookup"><span data-stu-id="2d91f-118">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2d91f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d91f-119">Return value</span></span>

<span data-ttu-id="2d91f-120">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2d91f-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="2d91f-121">ESENT 警告碼。</span><span class="sxs-lookup"><span data-stu-id="2d91f-121">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d91f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d91f-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2d91f-123">參考</span><span class="sxs-lookup"><span data-stu-id="2d91f-123">Reference</span></span>

[<span data-ttu-id="2d91f-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="2d91f-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2d91f-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="2d91f-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2d91f-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2d91f-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
