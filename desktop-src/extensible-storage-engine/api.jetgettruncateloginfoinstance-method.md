---
description: 深入瞭解： JetGetTruncateLogInfoInstance 方法
title: JetGetTruncateLogInfoInstance 方法
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195215"
---
# <a name="apijetgettruncateloginfoinstance-method"></a><span data-ttu-id="b7d91-103">JetGetTruncateLogInfoInstance 方法</span><span class="sxs-lookup"><span data-stu-id="b7d91-103">Api.JetGetTruncateLogInfoInstance method</span></span>

<span data-ttu-id="b7d91-104">在 JetBeginExternalBackupInstance (JET_INSTANCE 所起始的備份期間使用 [，BeginExternalBackupGrbit) ](./api.jetbeginexternalbackupinstance-method.md) 來查詢實例，以找出備份順利完成之後可安全刪除的交易記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="b7d91-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="b7d91-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7d91-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7d91-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b7d91-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d91-107">語法</span><span class="sxs-lookup"><span data-stu-id="b7d91-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="b7d91-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7d91-108">Parameters</span></span>

  - <span data-ttu-id="b7d91-109">instance</span><span class="sxs-lookup"><span data-stu-id="b7d91-109">instance</span></span>  
    <span data-ttu-id="b7d91-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b7d91-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b7d91-111">要取得資訊的實例。</span><span class="sxs-lookup"><span data-stu-id="b7d91-111">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7d91-112">files</span><span class="sxs-lookup"><span data-stu-id="b7d91-112">files</span></span>  
    <span data-ttu-id="b7d91-113">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b7d91-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b7d91-114">傳回 null 結束字串的清單，這些字串描述可在備份完成之後安全刪除的資料庫記錄檔集。</span><span class="sxs-lookup"><span data-stu-id="b7d91-114">Returns a list of null terminated strings describing the set of database log files that can be safely deleted after the backup completes.</span></span> <span data-ttu-id="b7d91-115">此緩衝區中傳回的字串清單，與登錄所用的多重字串格式相同。</span><span class="sxs-lookup"><span data-stu-id="b7d91-115">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="b7d91-116">每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="b7d91-116">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7d91-117">maxChars</span><span class="sxs-lookup"><span data-stu-id="b7d91-117">maxChars</span></span>  
    <span data-ttu-id="b7d91-118">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b7d91-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b7d91-119">要取出的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="b7d91-119">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7d91-120">actualChars</span><span class="sxs-lookup"><span data-stu-id="b7d91-120">actualChars</span></span>  
    <span data-ttu-id="b7d91-121">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b7d91-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b7d91-122">檔案清單的實際大小。</span><span class="sxs-lookup"><span data-stu-id="b7d91-122">Actual size of the file list.</span></span> <span data-ttu-id="b7d91-123">如果大於 maxChars，表示清單已被截斷。</span><span class="sxs-lookup"><span data-stu-id="b7d91-123">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d91-124">備註</span><span class="sxs-lookup"><span data-stu-id="b7d91-124">Remarks</span></span>

<span data-ttu-id="b7d91-125">請務必注意，如果輸出緩衝區太小而無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="b7d91-125">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7d91-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7d91-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7d91-127">參考</span><span class="sxs-lookup"><span data-stu-id="b7d91-127">Reference</span></span>

[<span data-ttu-id="b7d91-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="b7d91-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b7d91-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="b7d91-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b7d91-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b7d91-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
