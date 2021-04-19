---
description: 深入瞭解： JetGetAttachInfoInstance 方法
title: JetGetAttachInfoInstance 方法
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967103"
---
# <a name="apijetgetattachinfoinstance-method"></a><span data-ttu-id="c74b3-103">JetGetAttachInfoInstance 方法</span><span class="sxs-lookup"><span data-stu-id="c74b3-103">Api.JetGetAttachInfoInstance method</span></span>

<span data-ttu-id="c74b3-104">在 JetBeginExternalBackupInstance (JET_INSTANCE 所起始的備份期間使用 [，BeginExternalBackupGrbit) ](./api.jetbeginexternalbackupinstance-method.md) 來查詢實例，以取得應該成為備份檔案集一部分的資料庫檔案名。</span><span class="sxs-lookup"><span data-stu-id="c74b3-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="c74b3-105">系統只會考慮目前使用 [JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) ](./api.jetattachdatabase-method.md) 連接到實例的資料庫。</span><span class="sxs-lookup"><span data-stu-id="c74b3-105">Only databases that are currently attached to the instance using [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will be considered.</span></span> <span data-ttu-id="c74b3-106">之後可能會使用[JetOpenFileInstance (JET_INSTANCE、字串、JET_HANDLE、int64、int64) ](./api.jetopenfileinstance-method.md)和使用[JetReadFileInstance (JET_INSTANCE、JET_HANDLE、 \[ \] 、int32、int32) ](./api.jetreadfileinstance-method.md)來開啟這些檔案。</span><span class="sxs-lookup"><span data-stu-id="c74b3-106">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="c74b3-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c74b3-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c74b3-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c74b3-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c74b3-109">語法</span><span class="sxs-lookup"><span data-stu-id="c74b3-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="c74b3-110">參數</span><span class="sxs-lookup"><span data-stu-id="c74b3-110">Parameters</span></span>

  - <span data-ttu-id="c74b3-111">instance</span><span class="sxs-lookup"><span data-stu-id="c74b3-111">instance</span></span>  
    <span data-ttu-id="c74b3-112">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c74b3-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="c74b3-113">要取得資訊的實例。</span><span class="sxs-lookup"><span data-stu-id="c74b3-113">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="c74b3-114">files</span><span class="sxs-lookup"><span data-stu-id="c74b3-114">files</span></span>  
    <span data-ttu-id="c74b3-115">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c74b3-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c74b3-116">傳回 null 結束字串的清單，這些字串會描述應該是備份檔案集一部分的資料庫檔案集。</span><span class="sxs-lookup"><span data-stu-id="c74b3-116">Returns a list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="c74b3-117">此緩衝區中傳回的字串清單，與登錄所用的多重字串格式相同。</span><span class="sxs-lookup"><span data-stu-id="c74b3-117">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="c74b3-118">每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="c74b3-118">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="c74b3-119">maxChars</span><span class="sxs-lookup"><span data-stu-id="c74b3-119">maxChars</span></span>  
    <span data-ttu-id="c74b3-120">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c74b3-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c74b3-121">要取出的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="c74b3-121">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="c74b3-122">actualChars</span><span class="sxs-lookup"><span data-stu-id="c74b3-122">actualChars</span></span>  
    <span data-ttu-id="c74b3-123">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c74b3-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c74b3-124">檔案清單的實際大小。</span><span class="sxs-lookup"><span data-stu-id="c74b3-124">Actual size of the file list.</span></span> <span data-ttu-id="c74b3-125">如果大於 maxChars，表示清單已被截斷。</span><span class="sxs-lookup"><span data-stu-id="c74b3-125">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="c74b3-126">備註</span><span class="sxs-lookup"><span data-stu-id="c74b3-126">Remarks</span></span>

<span data-ttu-id="c74b3-127">請務必注意，如果輸出緩衝區太小而無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="c74b3-127">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="c74b3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c74b3-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c74b3-129">參考</span><span class="sxs-lookup"><span data-stu-id="c74b3-129">Reference</span></span>

[<span data-ttu-id="c74b3-130">Api 類別</span><span class="sxs-lookup"><span data-stu-id="c74b3-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c74b3-131">Api 成員</span><span class="sxs-lookup"><span data-stu-id="c74b3-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c74b3-132">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c74b3-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
