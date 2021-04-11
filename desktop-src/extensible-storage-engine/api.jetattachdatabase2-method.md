---
description: 深入瞭解： JetAttachDatabase2 方法
title: JetAttachDatabase2 方法
TOCTitle: 'JetAttachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55107224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 33d91f0746b3ebf178bd61de58919ab99d85b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690063"
---
# <a name="apijetattachdatabase2-method"></a><span data-ttu-id="2743e-103">JetAttachDatabase2 方法</span><span class="sxs-lookup"><span data-stu-id="2743e-103">Api.JetAttachDatabase2 method</span></span>

<span data-ttu-id="2743e-104">附加資料庫檔案以與資料庫實例搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2743e-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="2743e-105">若要使用資料庫，就必須使用 [JetOpenDatabase (JET_SESID、string、string、JET_DBID、OpenDatabaseGrbit) ](./api.jetopendatabase-method.md)來開啟它。</span><span class="sxs-lookup"><span data-stu-id="2743e-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="2743e-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2743e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2743e-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2743e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2743e-108">語法</span><span class="sxs-lookup"><span data-stu-id="2743e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase2(sesid, _
    database, maxPages, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="2743e-109">參數</span><span class="sxs-lookup"><span data-stu-id="2743e-109">Parameters</span></span>

  - <span data-ttu-id="2743e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="2743e-110">sesid</span></span>  
    <span data-ttu-id="2743e-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2743e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2743e-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="2743e-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2743e-113">[資料庫]</span><span class="sxs-lookup"><span data-stu-id="2743e-113">database</span></span>  
    <span data-ttu-id="2743e-114">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2743e-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2743e-115">要附加的資料庫。</span><span class="sxs-lookup"><span data-stu-id="2743e-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="2743e-116">maxPages</span><span class="sxs-lookup"><span data-stu-id="2743e-116">maxPages</span></span>  
    <span data-ttu-id="2743e-117">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2743e-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2743e-118">資料庫的大小上限（資料庫頁面）。</span><span class="sxs-lookup"><span data-stu-id="2743e-118">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="2743e-119">傳遞0表示沒有強制執行的最大值。</span><span class="sxs-lookup"><span data-stu-id="2743e-119">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="2743e-120">grbit</span><span class="sxs-lookup"><span data-stu-id="2743e-120">grbit</span></span>  
    <span data-ttu-id="2743e-121">型別： [AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="2743e-121">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2743e-122">附加選項。</span><span class="sxs-lookup"><span data-stu-id="2743e-122">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2743e-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="2743e-123">Return value</span></span>

<span data-ttu-id="2743e-124">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2743e-124">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="2743e-125">ESENT 警告碼。</span><span class="sxs-lookup"><span data-stu-id="2743e-125">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2743e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2743e-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2743e-127">參考</span><span class="sxs-lookup"><span data-stu-id="2743e-127">Reference</span></span>

[<span data-ttu-id="2743e-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="2743e-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2743e-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="2743e-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2743e-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2743e-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
