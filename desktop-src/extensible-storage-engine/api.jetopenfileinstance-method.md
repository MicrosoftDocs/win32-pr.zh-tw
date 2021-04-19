---
description: 深入瞭解： JetOpenFileInstance 方法
title: JetOpenFileInstance 方法
TOCTitle: 'JetOpenFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.JET_HANDLE@,System.Int64@,System.Int64@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopenfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b58b3a426fd2eb7e33cce1f5f539418bcc993ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990452"
---
# <a name="apijetopenfileinstance-method"></a><span data-ttu-id="57fb5-103">JetOpenFileInstance 方法</span><span class="sxs-lookup"><span data-stu-id="57fb5-103">Api.JetOpenFileInstance method</span></span>

<span data-ttu-id="57fb5-104">開啟連接的資料庫、資料庫修補檔或作用中實例的交易記錄檔，以執行串流模糊備份。</span><span class="sxs-lookup"><span data-stu-id="57fb5-104">Opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="57fb5-105">之後可以使用 JetReadFileInstance，透過傳回的控制碼讀取這些檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="57fb5-105">The data from these files can subsequently be read through the returned handle using JetReadFileInstance.</span></span> <span data-ttu-id="57fb5-106">傳回的控制碼必須使用 JetCloseFileInstance 來關閉。</span><span class="sxs-lookup"><span data-stu-id="57fb5-106">The returned handle must be closed using JetCloseFileInstance.</span></span> <span data-ttu-id="57fb5-107">實例的外部備份必須先前已使用 JetBeginExternalBackupInstance 起始。</span><span class="sxs-lookup"><span data-stu-id="57fb5-107">An external backup of the instance must have been previously initiated using JetBeginExternalBackupInstance.</span></span>

<span data-ttu-id="57fb5-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="57fb5-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="57fb5-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="57fb5-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="57fb5-110">語法</span><span class="sxs-lookup"><span data-stu-id="57fb5-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenFileInstance ( _
    instance As JET_INSTANCE, _
    file As String, _
    <OutAttribute> ByRef handle As JET_HANDLE, _
    <OutAttribute> ByRef fileSizeLow As Long, _
    <OutAttribute> ByRef fileSizeHigh As Long _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As String
Dim handle As JET_HANDLE
Dim fileSizeLow As Long
Dim fileSizeHigh As LongApi.JetOpenFileInstance(instance, _
    file, handle, fileSizeLow, fileSizeHigh)
```

``` csharp
public static void JetOpenFileInstance(
    JET_INSTANCE instance,
    string file,
    out JET_HANDLE handle,
    out long fileSizeLow,
    out long fileSizeHigh
)
```

#### <a name="parameters"></a><span data-ttu-id="57fb5-111">參數</span><span class="sxs-lookup"><span data-stu-id="57fb5-111">Parameters</span></span>

  - <span data-ttu-id="57fb5-112">instance</span><span class="sxs-lookup"><span data-stu-id="57fb5-112">instance</span></span>  
    <span data-ttu-id="57fb5-113">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="57fb5-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="57fb5-114">要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="57fb5-114">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="57fb5-115">file</span><span class="sxs-lookup"><span data-stu-id="57fb5-115">file</span></span>  
    <span data-ttu-id="57fb5-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="57fb5-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="57fb5-117">要開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="57fb5-117">The file to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="57fb5-118">處理</span><span class="sxs-lookup"><span data-stu-id="57fb5-118">handle</span></span>  
    <span data-ttu-id="57fb5-119">類型： [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="57fb5-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="57fb5-120">傳回檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="57fb5-120">Returns a handle to the file.</span></span>

<!-- end list -->

  - <span data-ttu-id="57fb5-121">fileSizeLow</span><span class="sxs-lookup"><span data-stu-id="57fb5-121">fileSizeLow</span></span>  
    <span data-ttu-id="57fb5-122">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="57fb5-122">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="57fb5-123">傳回最不重要的檔案大小32位。</span><span class="sxs-lookup"><span data-stu-id="57fb5-123">Returns the least significant 32 bits of the file size.</span></span>

<!-- end list -->

  - <span data-ttu-id="57fb5-124">fileSizeHigh</span><span class="sxs-lookup"><span data-stu-id="57fb5-124">fileSizeHigh</span></span>  
    <span data-ttu-id="57fb5-125">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="57fb5-125">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="57fb5-126">傳回最大的檔案大小32位。</span><span class="sxs-lookup"><span data-stu-id="57fb5-126">Returns the most significant 32 bits of the file size.</span></span>

## <a name="see-also"></a><span data-ttu-id="57fb5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57fb5-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="57fb5-128">參考</span><span class="sxs-lookup"><span data-stu-id="57fb5-128">Reference</span></span>

[<span data-ttu-id="57fb5-129">Api 類別</span><span class="sxs-lookup"><span data-stu-id="57fb5-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="57fb5-130">Api 成員</span><span class="sxs-lookup"><span data-stu-id="57fb5-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="57fb5-131">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="57fb5-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
