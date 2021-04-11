---
description: 深入瞭解： JetTruncateLogInstance 方法
title: JetTruncateLogInstance 方法
TOCTitle: 'JetTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jettruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55100815
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc1693b3f84cd594bfeca81a8e854e49e28d955f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945284"
---
# <a name="apijettruncateloginstance-method"></a><span data-ttu-id="79148-103">JetTruncateLogInstance 方法</span><span class="sxs-lookup"><span data-stu-id="79148-103">Api.JetTruncateLogInstance method</span></span>

<span data-ttu-id="79148-104">在 JetBeginExternalBackup 所起始的備份期間，用來刪除目前的備份成功完成後，將不再需要的任何交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="79148-104">Used during a backup initiated by JetBeginExternalBackup to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="79148-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="79148-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="79148-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="79148-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="79148-107">語法</span><span class="sxs-lookup"><span data-stu-id="79148-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTruncateLogInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTruncateLogInstance(instance)
```

``` csharp
public static void JetTruncateLogInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="79148-108">參數</span><span class="sxs-lookup"><span data-stu-id="79148-108">Parameters</span></span>

  - <span data-ttu-id="79148-109">instance</span><span class="sxs-lookup"><span data-stu-id="79148-109">instance</span></span>  
    <span data-ttu-id="79148-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79148-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="79148-111">要截斷的實例。</span><span class="sxs-lookup"><span data-stu-id="79148-111">The instance to truncate.</span></span>

## <a name="see-also"></a><span data-ttu-id="79148-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79148-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="79148-113">參考</span><span class="sxs-lookup"><span data-stu-id="79148-113">Reference</span></span>

[<span data-ttu-id="79148-114">Api 類別</span><span class="sxs-lookup"><span data-stu-id="79148-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="79148-115">Api 成員</span><span class="sxs-lookup"><span data-stu-id="79148-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="79148-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="79148-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
