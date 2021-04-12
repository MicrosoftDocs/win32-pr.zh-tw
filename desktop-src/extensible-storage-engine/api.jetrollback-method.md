---
description: 深入瞭解： JetRollback 方法
title: JetRollback 方法
TOCTitle: 'JetRollback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRollback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrollback(v=EXCHG.10)
ms:contentKeyID: 55100794
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9144bade272ddaea7501be5622c7263268c0f1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318199"
---
# <a name="apijetrollback-method"></a><span data-ttu-id="b32bc-103">JetRollback 方法</span><span class="sxs-lookup"><span data-stu-id="b32bc-103">Api.JetRollback method</span></span>

<span data-ttu-id="b32bc-104">復原對資料庫狀態所做的變更，並返回到最後一個儲存點。</span><span class="sxs-lookup"><span data-stu-id="b32bc-104">Undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="b32bc-105">JetRollback 也會關閉儲存點期間開啟的任何資料指標。</span><span class="sxs-lookup"><span data-stu-id="b32bc-105">JetRollback will also close any cursors opened during the save point.</span></span> <span data-ttu-id="b32bc-106">如果最外層的儲存點復原，會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="b32bc-106">If the outermost save point is undone, the session will exit the transaction.</span></span>

<span data-ttu-id="b32bc-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b32bc-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b32bc-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b32bc-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b32bc-109">語法</span><span class="sxs-lookup"><span data-stu-id="b32bc-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRollback ( _
    sesid As JET_SESID, _
    grbit As RollbackTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As RollbackTransactionGrbitApi.JetRollback(sesid, grbit)
```

``` csharp
public static void JetRollback(
    JET_SESID sesid,
    RollbackTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b32bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="b32bc-110">Parameters</span></span>

  - <span data-ttu-id="b32bc-111">sesid</span><span class="sxs-lookup"><span data-stu-id="b32bc-111">sesid</span></span>  
    <span data-ttu-id="b32bc-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b32bc-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b32bc-113">要復原交易的會話。</span><span class="sxs-lookup"><span data-stu-id="b32bc-113">The session to rollback the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="b32bc-114">grbit</span><span class="sxs-lookup"><span data-stu-id="b32bc-114">grbit</span></span>  
    <span data-ttu-id="b32bc-115">型別： [RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="b32bc-115">Type: [Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b32bc-116">復原選項。</span><span class="sxs-lookup"><span data-stu-id="b32bc-116">Rollback options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b32bc-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b32bc-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b32bc-118">參考</span><span class="sxs-lookup"><span data-stu-id="b32bc-118">Reference</span></span>

[<span data-ttu-id="b32bc-119">Api 類別</span><span class="sxs-lookup"><span data-stu-id="b32bc-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b32bc-120">Api 成員</span><span class="sxs-lookup"><span data-stu-id="b32bc-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b32bc-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b32bc-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
