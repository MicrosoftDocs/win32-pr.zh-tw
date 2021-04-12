---
description: 深入瞭解： JetStopBackupInstance 方法
title: JetStopBackupInstance 方法
TOCTitle: 'JetStopBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetStopBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetstopbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100825
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetStopBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetStopBackupInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69b6b98b21dba4cffb37827b2965b4e62197121f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195210"
---
# <a name="apijetstopbackupinstance-method"></a><span data-ttu-id="f4cc0-103">JetStopBackupInstance 方法</span><span class="sxs-lookup"><span data-stu-id="f4cc0-103">Api.JetStopBackupInstance method</span></span>

<span data-ttu-id="f4cc0-104">防止串流備份相關的活動在特定執行中的實例上繼續執行，因此以可預測的方式結束資料流程備份。</span><span class="sxs-lookup"><span data-stu-id="f4cc0-104">Prevents streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="f4cc0-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f4cc0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f4cc0-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f4cc0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f4cc0-107">語法</span><span class="sxs-lookup"><span data-stu-id="f4cc0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetStopBackupInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetStopBackupInstance(instance)
```

``` csharp
public static void JetStopBackupInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="f4cc0-108">參數</span><span class="sxs-lookup"><span data-stu-id="f4cc0-108">Parameters</span></span>

  - <span data-ttu-id="f4cc0-109">instance</span><span class="sxs-lookup"><span data-stu-id="f4cc0-109">instance</span></span>  
    <span data-ttu-id="f4cc0-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f4cc0-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="f4cc0-111">要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="f4cc0-111">The instance to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4cc0-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4cc0-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f4cc0-113">參考</span><span class="sxs-lookup"><span data-stu-id="f4cc0-113">Reference</span></span>

[<span data-ttu-id="f4cc0-114">Api 類別</span><span class="sxs-lookup"><span data-stu-id="f4cc0-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f4cc0-115">Api 成員</span><span class="sxs-lookup"><span data-stu-id="f4cc0-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f4cc0-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f4cc0-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
