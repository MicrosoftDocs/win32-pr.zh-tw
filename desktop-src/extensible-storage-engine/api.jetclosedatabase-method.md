---
description: 深入瞭解： JetCloseDatabase 方法
title: JetCloseDatabase 方法
TOCTitle: 'JetCloseDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.CloseDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosedatabase(v=EXCHG.10)
ms:contentKeyID: 55100662
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b39d830c34f2d772730d7ea1c65ec4adf3c3d4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511143"
---
# <a name="apijetclosedatabase-method"></a><span data-ttu-id="22356-103">JetCloseDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="22356-103">Api.JetCloseDatabase method</span></span>

<span data-ttu-id="22356-104">關閉先前以 JetOpenDatabase 開啟的資料庫檔案 [ (JET_SESID、字串、字串、JET_DBID、OpenDatabaseGrbit) ](./api.jetopendatabase-method.md) 或使用 [JetCreateDatabase (JET_SESID、字串、字串、JET_DBID、CreateDatabaseGrbit) ](./api.jetcreatedatabase-method.md)建立。</span><span class="sxs-lookup"><span data-stu-id="22356-104">Closes a database file that was previously opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md) or created with [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="22356-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="22356-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="22356-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="22356-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="22356-107">語法</span><span class="sxs-lookup"><span data-stu-id="22356-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    grbit As CloseDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim grbit As CloseDatabaseGrbitApi.JetCloseDatabase(sesid, dbid, _
    grbit)
```

``` csharp
public static void JetCloseDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    CloseDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="22356-108">參數</span><span class="sxs-lookup"><span data-stu-id="22356-108">Parameters</span></span>

  - <span data-ttu-id="22356-109">sesid</span><span class="sxs-lookup"><span data-stu-id="22356-109">sesid</span></span>  
    <span data-ttu-id="22356-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="22356-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="22356-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="22356-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="22356-112">dbid</span><span class="sxs-lookup"><span data-stu-id="22356-112">dbid</span></span>  
    <span data-ttu-id="22356-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="22356-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="22356-114">要關閉的資料庫。</span><span class="sxs-lookup"><span data-stu-id="22356-114">The database to close.</span></span>

<!-- end list -->

  - <span data-ttu-id="22356-115">grbit</span><span class="sxs-lookup"><span data-stu-id="22356-115">grbit</span></span>  
    <span data-ttu-id="22356-116">型別： [CloseDatabaseGrbit](./closedatabasegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="22356-116">Type: [Microsoft.Isam.Esent.Interop.CloseDatabaseGrbit](./closedatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="22356-117">關閉選項。</span><span class="sxs-lookup"><span data-stu-id="22356-117">Close options.</span></span>

## <a name="see-also"></a><span data-ttu-id="22356-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22356-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22356-119">參考</span><span class="sxs-lookup"><span data-stu-id="22356-119">Reference</span></span>

[<span data-ttu-id="22356-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="22356-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="22356-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="22356-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="22356-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="22356-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
