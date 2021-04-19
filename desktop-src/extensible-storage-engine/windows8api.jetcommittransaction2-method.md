---
description: 深入瞭解： Windows8Api. JetCommitTransaction2 方法
title: 'Windows8Api. JetCommitTransaction2 方法 (Windows8 的) '
TOCTitle: 'JetCommitTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcommittransaction2(v=EXCHG.10)
ms:contentKeyID: 55104454
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80ddc0670b60a3f2a280ff2aca3f051242c453ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974965"
---
# <a name="windows8apijetcommittransaction2-method"></a><span data-ttu-id="8ad83-103">Windows8Api. JetCommitTransaction2 方法</span><span class="sxs-lookup"><span data-stu-id="8ad83-103">Windows8Api.JetCommitTransaction2 method</span></span>

<span data-ttu-id="8ad83-104">認可目前儲存點期間對資料庫狀態所做的變更，並將其遷移至先前的儲存點。</span><span class="sxs-lookup"><span data-stu-id="8ad83-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="8ad83-105">如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="8ad83-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="8ad83-106">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8ad83-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="8ad83-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8ad83-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8ad83-108">語法</span><span class="sxs-lookup"><span data-stu-id="8ad83-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction2 ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_IDWindows8Api.JetCommitTransaction2(sesid, _
    grbit, durableCommit, commitId)
```

``` csharp
public static void JetCommitTransaction2(
    JET_SESID sesid,
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a><span data-ttu-id="8ad83-109">參數</span><span class="sxs-lookup"><span data-stu-id="8ad83-109">Parameters</span></span>

  - <span data-ttu-id="8ad83-110">sesid</span><span class="sxs-lookup"><span data-stu-id="8ad83-110">sesid</span></span>  
    <span data-ttu-id="8ad83-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8ad83-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8ad83-112">認可交易的會話。</span><span class="sxs-lookup"><span data-stu-id="8ad83-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ad83-113">grbit</span><span class="sxs-lookup"><span data-stu-id="8ad83-113">grbit</span></span>  
    <span data-ttu-id="8ad83-114">型別： [CommitTransactionGrbit](./committransactiongrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="8ad83-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8ad83-115">認可選項。</span><span class="sxs-lookup"><span data-stu-id="8ad83-115">Commit options.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ad83-116">durableCommit</span><span class="sxs-lookup"><span data-stu-id="8ad83-116">durableCommit</span></span>  
    <span data-ttu-id="8ad83-117">類型： [TimeSpan](/dotnet/api/system.timespan)</span><span class="sxs-lookup"><span data-stu-id="8ad83-117">Type: [System.TimeSpan](/dotnet/api/system.timespan)</span></span>  
    
    <span data-ttu-id="8ad83-118">認可延遲交易的持續時間。</span><span class="sxs-lookup"><span data-stu-id="8ad83-118">Duration to commit lazy transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="8ad83-119">commitId</span><span class="sxs-lookup"><span data-stu-id="8ad83-119">commitId</span></span>  
    <span data-ttu-id="8ad83-120">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="8ad83-120">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="8ad83-121">與此認可記錄相關聯的認可識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ad83-121">Commit-id associated with this commit record.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ad83-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ad83-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8ad83-123">參考</span><span class="sxs-lookup"><span data-stu-id="8ad83-123">Reference</span></span>

[<span data-ttu-id="8ad83-124">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="8ad83-124">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="8ad83-125">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="8ad83-125">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="8ad83-126">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="8ad83-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
