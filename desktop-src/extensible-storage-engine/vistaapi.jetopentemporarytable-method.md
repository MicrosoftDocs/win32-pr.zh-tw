---
description: 深入瞭解： VistaApi. JetOpenTemporaryTable 方法
title: 'VistaApi. JetOpenTemporaryTable 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a261494cf8b12039371c445a4cf2124f3ec1c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981159"
---
# <a name="vistaapijetopentemporarytable-method"></a><span data-ttu-id="3edf8-103">VistaApi. JetOpenTemporaryTable 方法</span><span class="sxs-lookup"><span data-stu-id="3edf8-103">VistaApi.JetOpenTemporaryTable method</span></span>

<span data-ttu-id="3edf8-104">使用單一索引建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="3edf8-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="3edf8-105">臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="3edf8-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="3edf8-106">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="3edf8-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="3edf8-107">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="3edf8-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="3edf8-108">另請參閱[JetOpenTempTable (JET_SESID、 \[ \] 、Int32、TempTableGrbit、JET_TABLEID、 \[ \]) ](./api.jetopentemptable-method.md)、 [JetOpenTempTable3 (JET_SESID、 \[ \] 、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、 \[ \]) ](./api.jetopentemptable3-method.md)。</span><span class="sxs-lookup"><span data-stu-id="3edf8-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span>

<span data-ttu-id="3edf8-109">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="3edf8-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="3edf8-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3edf8-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3edf8-111">語法</span><span class="sxs-lookup"><span data-stu-id="3edf8-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="3edf8-112">參數</span><span class="sxs-lookup"><span data-stu-id="3edf8-112">Parameters</span></span>

  - <span data-ttu-id="3edf8-113">sesid</span><span class="sxs-lookup"><span data-stu-id="3edf8-113">sesid</span></span>  
    <span data-ttu-id="3edf8-114">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3edf8-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3edf8-115">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="3edf8-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3edf8-116">temporarytable</span><span class="sxs-lookup"><span data-stu-id="3edf8-116">temporarytable</span></span>  
    <span data-ttu-id="3edf8-117">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="3edf8-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="3edf8-118">要在輸入上建立之臨時表的描述。</span><span class="sxs-lookup"><span data-stu-id="3edf8-118">Description of the temporary table to create on input.</span></span> <span data-ttu-id="3edf8-119">在成功呼叫之後，結構會包含臨時表和資料行標識的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3edf8-119">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="3edf8-120">使用 [JetCloseTable (JET_SESID，JET_TABLEID) ](./api.jetclosetable-method.md) 在完成時釋放臨時表。</span><span class="sxs-lookup"><span data-stu-id="3edf8-120">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="3edf8-121">備註</span><span class="sxs-lookup"><span data-stu-id="3edf8-121">Remarks</span></span>

<span data-ttu-id="3edf8-122">在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="3edf8-122">Introduced in Windows Vista.</span></span> <span data-ttu-id="3edf8-123">針對較早版本的 Esent，請使用[JetOpenTempTable3 (JET_SESID、 \[ \] 、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID \[ \]) ](./api.jetopentemptable3-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="3edf8-123">Use [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="3edf8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3edf8-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3edf8-125">參考</span><span class="sxs-lookup"><span data-stu-id="3edf8-125">Reference</span></span>

[<span data-ttu-id="3edf8-126">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="3edf8-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="3edf8-127">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="3edf8-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="3edf8-128">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="3edf8-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
