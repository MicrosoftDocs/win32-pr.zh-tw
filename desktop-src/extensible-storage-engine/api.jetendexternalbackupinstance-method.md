---
description: 深入瞭解： JetEndExternalBackupInstance 方法
title: JetEndExternalBackupInstance 方法
TOCTitle: 'JetEndExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100691
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16ec4dc235f677ba42b4ae3bae10a79b9d494576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943304"
---
# <a name="apijetendexternalbackupinstance-method"></a><span data-ttu-id="baae9-103">JetEndExternalBackupInstance 方法</span><span class="sxs-lookup"><span data-stu-id="baae9-103">Api.JetEndExternalBackupInstance method</span></span>

<span data-ttu-id="baae9-104">結束外部備份會話。</span><span class="sxs-lookup"><span data-stu-id="baae9-104">Ends an external backup session.</span></span> <span data-ttu-id="baae9-105">此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。</span><span class="sxs-lookup"><span data-stu-id="baae9-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="baae9-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="baae9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="baae9-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="baae9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="baae9-108">語法</span><span class="sxs-lookup"><span data-stu-id="baae9-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetEndExternalBackupInstance(instance)
```

``` csharp
public static void JetEndExternalBackupInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="baae9-109">參數</span><span class="sxs-lookup"><span data-stu-id="baae9-109">Parameters</span></span>

  - <span data-ttu-id="baae9-110">instance</span><span class="sxs-lookup"><span data-stu-id="baae9-110">instance</span></span>  
    <span data-ttu-id="baae9-111">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="baae9-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="baae9-112">要結束備份的實例。</span><span class="sxs-lookup"><span data-stu-id="baae9-112">The instance to end the backup for.</span></span>

## <a name="see-also"></a><span data-ttu-id="baae9-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baae9-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="baae9-114">參考</span><span class="sxs-lookup"><span data-stu-id="baae9-114">Reference</span></span>

[<span data-ttu-id="baae9-115">Api 類別</span><span class="sxs-lookup"><span data-stu-id="baae9-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="baae9-116">Api 成員</span><span class="sxs-lookup"><span data-stu-id="baae9-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="baae9-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="baae9-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
