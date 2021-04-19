---
description: 深入瞭解： Windows8Api. JetOpenTemporaryTable2 方法
title: 'Windows8Api. JetOpenTemporaryTable2 方法 (Windows8 的) '
TOCTitle: 'JetOpenTemporaryTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetopentemporarytable2(v=EXCHG.10)
ms:contentKeyID: 55107829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ebb96af18e655c9f9304e2fe7a339663c0206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982290"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="4fb4d-103">Windows8Api. JetOpenTemporaryTable2 方法</span><span class="sxs-lookup"><span data-stu-id="4fb4d-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="4fb4d-104">使用單一索引建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="4fb4d-105">臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="4fb4d-106">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="4fb4d-107">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="4fb4d-108">另請參閱[JetOpenTempTable (JET_SESID、 \[ \] 、int32、TempTableGrbit、JET_TABLEID、 \[ \]) ](./api.jetopentemptable-method.md)、"JetOpenTempTable2"、 [JetOpenTempTable3 (JET_SESID、 \[ \] 、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID \[ \]) ](./api.jetopentemptable3-method.md)。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="4fb4d-109">[JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) ](./vistaapi.jetopentemporarytable-method.md)。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="4fb4d-110">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4fb4d-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="4fb4d-111">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb4d-112">語法</span><span class="sxs-lookup"><span data-stu-id="4fb4d-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable2 ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEWindows8Api.JetOpenTemporaryTable2(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable2(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="4fb4d-113">參數</span><span class="sxs-lookup"><span data-stu-id="4fb4d-113">Parameters</span></span>

  - <span data-ttu-id="4fb4d-114">sesid</span><span class="sxs-lookup"><span data-stu-id="4fb4d-114">sesid</span></span>  
    <span data-ttu-id="4fb4d-115">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4fb4d-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4fb4d-116">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4fb4d-117">temporarytable</span><span class="sxs-lookup"><span data-stu-id="4fb4d-117">temporarytable</span></span>  
    <span data-ttu-id="4fb4d-118">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="4fb4d-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="4fb4d-119">要在輸入上建立之臨時表的描述。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="4fb4d-120">在成功呼叫之後，結構會包含臨時表和資料行標識的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="4fb4d-121">使用 [JetCloseTable (JET_SESID，JET_TABLEID) ](./api.jetclosetable-method.md) 在完成時釋放臨時表。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fb4d-122">備註</span><span class="sxs-lookup"><span data-stu-id="4fb4d-122">Remarks</span></span>

<span data-ttu-id="4fb4d-123">使用 [JetOpenTemporaryTable (JET_SESID，JET_OPENTEMPORARYTABLE) ](./vistaapi.jetopentemporarytable-method.md) 舊版的 Esent。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fb4d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fb4d-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4fb4d-125">參考</span><span class="sxs-lookup"><span data-stu-id="4fb4d-125">Reference</span></span>

[<span data-ttu-id="4fb4d-126">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="4fb4d-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="4fb4d-127">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="4fb4d-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="4fb4d-128">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="4fb4d-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
