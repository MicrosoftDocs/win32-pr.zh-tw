---
description: 深入瞭解： JetBeginExternalBackupInstance 方法
title: JetBeginExternalBackupInstance 方法
TOCTitle: 'JetBeginExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100659
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c42f5d1f62de0af7582247fb47d407f82981a42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943309"
---
# <a name="apijetbeginexternalbackupinstance-method"></a><span data-ttu-id="7b865-103">JetBeginExternalBackupInstance 方法</span><span class="sxs-lookup"><span data-stu-id="7b865-103">Api.JetBeginExternalBackupInstance method</span></span>

<span data-ttu-id="7b865-104">當引擎和資料庫在線上且作用中時，起始外部備份。</span><span class="sxs-lookup"><span data-stu-id="7b865-104">Initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="7b865-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b865-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7b865-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7b865-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b865-107">語法</span><span class="sxs-lookup"><span data-stu-id="7b865-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginExternalBackupInstance ( _
    instance As JET_INSTANCE, _
    grbit As BeginExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As BeginExternalBackupGrbitApi.JetBeginExternalBackupInstance(instance, _
    grbit)
```

``` csharp
public static void JetBeginExternalBackupInstance(
    JET_INSTANCE instance,
    BeginExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7b865-108">參數</span><span class="sxs-lookup"><span data-stu-id="7b865-108">Parameters</span></span>

  - <span data-ttu-id="7b865-109">instance</span><span class="sxs-lookup"><span data-stu-id="7b865-109">instance</span></span>  
    <span data-ttu-id="7b865-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b865-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7b865-111">準備備份的實例。</span><span class="sxs-lookup"><span data-stu-id="7b865-111">The instance prepare for backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b865-112">grbit</span><span class="sxs-lookup"><span data-stu-id="7b865-112">grbit</span></span>  
    <span data-ttu-id="7b865-113">型別： [BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="7b865-113">Type: [Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7b865-114">備份選項。</span><span class="sxs-lookup"><span data-stu-id="7b865-114">Backup options.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b865-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b865-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b865-116">參考</span><span class="sxs-lookup"><span data-stu-id="7b865-116">Reference</span></span>

[<span data-ttu-id="7b865-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="7b865-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7b865-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="7b865-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7b865-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7b865-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
