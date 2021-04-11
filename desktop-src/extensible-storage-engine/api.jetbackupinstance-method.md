---
description: 深入瞭解： JetBackupInstance 方法
title: JetBackupInstance 方法
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73c5b44f1f0b69aaed6066635ad4e82690bc3c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111941"
---
# <a name="apijetbackupinstance-method"></a><span data-ttu-id="e199d-103">JetBackupInstance 方法</span><span class="sxs-lookup"><span data-stu-id="e199d-103">Api.JetBackupInstance method</span></span>

<span data-ttu-id="e199d-104">執行實例的串流備份，包括所有附加的資料庫，到目錄中。</span><span class="sxs-lookup"><span data-stu-id="e199d-104">Performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="e199d-105">如果引擎支援多個備份方法，這是最簡單且最簡單的封裝函數。</span><span class="sxs-lookup"><span data-stu-id="e199d-105">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="e199d-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e199d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e199d-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e199d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e199d-108">語法</span><span class="sxs-lookup"><span data-stu-id="e199d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="e199d-109">參數</span><span class="sxs-lookup"><span data-stu-id="e199d-109">Parameters</span></span>

  - <span data-ttu-id="e199d-110">instance</span><span class="sxs-lookup"><span data-stu-id="e199d-110">instance</span></span>  
    <span data-ttu-id="e199d-111">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e199d-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="e199d-112">要備份的實例。</span><span class="sxs-lookup"><span data-stu-id="e199d-112">The instance to backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="e199d-113">目的地</span><span class="sxs-lookup"><span data-stu-id="e199d-113">destination</span></span>  
    <span data-ttu-id="e199d-114">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e199d-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e199d-115">要儲存備份的目錄。</span><span class="sxs-lookup"><span data-stu-id="e199d-115">The directory where the backup is to be stored.</span></span> <span data-ttu-id="e199d-116">如果備份路徑為 null，則使用函式會盡可能截斷記錄。</span><span class="sxs-lookup"><span data-stu-id="e199d-116">If the backup path is null to use the function will truncate the logs, if possible.</span></span>

<!-- end list -->

  - <span data-ttu-id="e199d-117">grbit</span><span class="sxs-lookup"><span data-stu-id="e199d-117">grbit</span></span>  
    <span data-ttu-id="e199d-118">型別： [BackupGrbit](./backupgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="e199d-118">Type: [Microsoft.Isam.Esent.Interop.BackupGrbit](./backupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e199d-119">備份選項。</span><span class="sxs-lookup"><span data-stu-id="e199d-119">Backup options.</span></span>

<!-- end list -->

  - <span data-ttu-id="e199d-120">statusCallback</span><span class="sxs-lookup"><span data-stu-id="e199d-120">statusCallback</span></span>  
    <span data-ttu-id="e199d-121">類型： [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="e199d-121">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="e199d-122">選擇性狀態通知回呼。</span><span class="sxs-lookup"><span data-stu-id="e199d-122">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="e199d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e199d-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e199d-124">參考</span><span class="sxs-lookup"><span data-stu-id="e199d-124">Reference</span></span>

[<span data-ttu-id="e199d-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="e199d-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e199d-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="e199d-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e199d-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e199d-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
