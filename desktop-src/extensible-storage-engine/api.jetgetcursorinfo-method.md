---
description: 深入瞭解： JetGetCursorInfo 方法
title: JetGetCursorInfo 方法
TOCTitle: 'JetGetCursorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcursorinfo(v=EXCHG.10)
ms:contentKeyID: 55100707
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7144283a062b0097d6866e74d1c263bb130c5e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026148"
---
# <a name="apijetgetcursorinfo-method"></a><span data-ttu-id="ec5a5-103">JetGetCursorInfo 方法</span><span class="sxs-lookup"><span data-stu-id="ec5a5-103">Api.JetGetCursorInfo method</span></span>

<span data-ttu-id="ec5a5-104">根據記錄目前的更新狀態，判斷資料指標的目前記錄更新是否會導致寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-104">Determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="ec5a5-105">即使 JetGetCursorInfo 成功傳回，還是可能會傳回寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-105">It is possible that a write conflict will ultimately be returned even if JetGetCursorInfo returns successfully.</span></span> <span data-ttu-id="ec5a5-106">因為另一個會話可能會在目前的會話可以更新相同記錄之前更新記錄。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-106">because another session may update the record before the current session is able to update the same record.</span></span>

<span data-ttu-id="ec5a5-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ec5a5-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ec5a5-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ec5a5-109">語法</span><span class="sxs-lookup"><span data-stu-id="ec5a5-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCursorInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetGetCursorInfo(sesid, tableid)
```

``` csharp
public static void JetGetCursorInfo(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="ec5a5-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec5a5-110">Parameters</span></span>

  - <span data-ttu-id="ec5a5-111">sesid</span><span class="sxs-lookup"><span data-stu-id="ec5a5-111">sesid</span></span>  
    <span data-ttu-id="ec5a5-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ec5a5-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ec5a5-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ec5a5-114">tableid</span><span class="sxs-lookup"><span data-stu-id="ec5a5-114">tableid</span></span>  
    <span data-ttu-id="ec5a5-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ec5a5-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ec5a5-116">要檢查的資料指標。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-116">The cursor to check.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec5a5-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec5a5-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec5a5-118">參考</span><span class="sxs-lookup"><span data-stu-id="ec5a5-118">Reference</span></span>

[<span data-ttu-id="ec5a5-119">Api 類別</span><span class="sxs-lookup"><span data-stu-id="ec5a5-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ec5a5-120">Api 成員</span><span class="sxs-lookup"><span data-stu-id="ec5a5-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ec5a5-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ec5a5-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
