---
description: 深入瞭解： JetCommitTransaction 方法
title: JetCommitTransaction 方法
TOCTitle: 'JetCommitTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcommittransaction(v=EXCHG.10)
ms:contentKeyID: 55100665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edf0799af53c3da422f92f981f7a28ee7a283d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991669"
---
# <a name="apijetcommittransaction-method"></a><span data-ttu-id="8617a-103">JetCommitTransaction 方法</span><span class="sxs-lookup"><span data-stu-id="8617a-103">Api.JetCommitTransaction method</span></span>

<span data-ttu-id="8617a-104">認可目前儲存點期間對資料庫狀態所做的變更，並將其遷移至先前的儲存點。</span><span class="sxs-lookup"><span data-stu-id="8617a-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="8617a-105">如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="8617a-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="8617a-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8617a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8617a-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8617a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8617a-108">語法</span><span class="sxs-lookup"><span data-stu-id="8617a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbitApi.JetCommitTransaction(sesid, _
    grbit)
```

``` csharp
public static void JetCommitTransaction(
    JET_SESID sesid,
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8617a-109">參數</span><span class="sxs-lookup"><span data-stu-id="8617a-109">Parameters</span></span>

  - <span data-ttu-id="8617a-110">sesid</span><span class="sxs-lookup"><span data-stu-id="8617a-110">sesid</span></span>  
    <span data-ttu-id="8617a-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8617a-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8617a-112">認可交易的會話。</span><span class="sxs-lookup"><span data-stu-id="8617a-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="8617a-113">grbit</span><span class="sxs-lookup"><span data-stu-id="8617a-113">grbit</span></span>  
    <span data-ttu-id="8617a-114">型別： [CommitTransactionGrbit](./committransactiongrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="8617a-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8617a-115">認可選項。</span><span class="sxs-lookup"><span data-stu-id="8617a-115">Commit options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8617a-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8617a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8617a-117">參考</span><span class="sxs-lookup"><span data-stu-id="8617a-117">Reference</span></span>

[<span data-ttu-id="8617a-118">Api 類別</span><span class="sxs-lookup"><span data-stu-id="8617a-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8617a-119">Api 成員</span><span class="sxs-lookup"><span data-stu-id="8617a-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8617a-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8617a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
