---
description: 深入瞭解： JetRestoreInstance 方法
title: JetRestoreInstance 方法
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973030"
---
# <a name="apijetrestoreinstance-method"></a><span data-ttu-id="5576a-103">JetRestoreInstance 方法</span><span class="sxs-lookup"><span data-stu-id="5576a-103">Api.JetRestoreInstance method</span></span>

<span data-ttu-id="5576a-104">還原和復原實例（包括所有附加的資料庫）的資料流程備份。</span><span class="sxs-lookup"><span data-stu-id="5576a-104">Restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="5576a-105">它是設計來搭配使用 [JetBackupInstance (JET_INSTANCE、String、BackupGrbit JET_PFNSTATUS) ](./api.jetbackupinstance-method.md) 函數所建立的備份。</span><span class="sxs-lookup"><span data-stu-id="5576a-105">It is designed to work with a backup created with the [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) function.</span></span> <span data-ttu-id="5576a-106">這是最簡單且最具封裝的還原功能。</span><span class="sxs-lookup"><span data-stu-id="5576a-106">This is the simplest and most encapsulated restore function.</span></span>

<span data-ttu-id="5576a-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5576a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5576a-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5576a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5576a-109">語法</span><span class="sxs-lookup"><span data-stu-id="5576a-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="5576a-110">參數</span><span class="sxs-lookup"><span data-stu-id="5576a-110">Parameters</span></span>

  - <span data-ttu-id="5576a-111">instance</span><span class="sxs-lookup"><span data-stu-id="5576a-111">instance</span></span>  
    <span data-ttu-id="5576a-112">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5576a-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="5576a-113">要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="5576a-113">The instance to use.</span></span> <span data-ttu-id="5576a-114">不應初始化實例。</span><span class="sxs-lookup"><span data-stu-id="5576a-114">The instance should not be initialized.</span></span> <span data-ttu-id="5576a-115">還原檔案將會初始化實例。</span><span class="sxs-lookup"><span data-stu-id="5576a-115">Restoring the files will initialize the instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="5576a-116">source</span><span class="sxs-lookup"><span data-stu-id="5576a-116">source</span></span>  
    <span data-ttu-id="5576a-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5576a-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5576a-118">備份的位置。</span><span class="sxs-lookup"><span data-stu-id="5576a-118">Location of the backup.</span></span> <span data-ttu-id="5576a-119">應使用 [JetBackupInstance (JET_INSTANCE、String、BackupGrbit JET_PFNSTATUS) ](./api.jetbackupinstance-method.md)建立備份。</span><span class="sxs-lookup"><span data-stu-id="5576a-119">The backup should have been created with [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="5576a-120">目的地</span><span class="sxs-lookup"><span data-stu-id="5576a-120">destination</span></span>  
    <span data-ttu-id="5576a-121">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5576a-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5576a-122">將從備份組複製和復原資料庫檔案的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="5576a-122">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="5576a-123">如果設定為 null，則會將資料庫檔案複製並復原到原始位置。</span><span class="sxs-lookup"><span data-stu-id="5576a-123">If this is set to null, the database files will be copied and recovered to their original location.</span></span>

<!-- end list -->

  - <span data-ttu-id="5576a-124">statusCallback</span><span class="sxs-lookup"><span data-stu-id="5576a-124">statusCallback</span></span>  
    <span data-ttu-id="5576a-125">類型： [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="5576a-125">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="5576a-126">選擇性狀態通知回呼。</span><span class="sxs-lookup"><span data-stu-id="5576a-126">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="5576a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5576a-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5576a-128">參考</span><span class="sxs-lookup"><span data-stu-id="5576a-128">Reference</span></span>

[<span data-ttu-id="5576a-129">Api 類別</span><span class="sxs-lookup"><span data-stu-id="5576a-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5576a-130">Api 成員</span><span class="sxs-lookup"><span data-stu-id="5576a-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5576a-131">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5576a-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
