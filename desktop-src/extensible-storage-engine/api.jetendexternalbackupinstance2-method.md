---
description: 深入瞭解： JetEndExternalBackupInstance2 方法
title: JetEndExternalBackupInstance2 方法
TOCTitle: 'JetEndExternalBackupInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance2(v=EXCHG.10)
ms:contentKeyID: 55100692
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71a405c5e0ba3a398071cc317e0d42dd98c4953d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191249"
---
# <a name="apijetendexternalbackupinstance2-method"></a><span data-ttu-id="6d712-103">JetEndExternalBackupInstance2 方法</span><span class="sxs-lookup"><span data-stu-id="6d712-103">Api.JetEndExternalBackupInstance2 method</span></span>

<span data-ttu-id="6d712-104">結束外部備份會話。</span><span class="sxs-lookup"><span data-stu-id="6d712-104">Ends an external backup session.</span></span> <span data-ttu-id="6d712-105">此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。</span><span class="sxs-lookup"><span data-stu-id="6d712-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="6d712-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6d712-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6d712-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6d712-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6d712-108">語法</span><span class="sxs-lookup"><span data-stu-id="6d712-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As EndExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As EndExternalBackupGrbitApi.JetEndExternalBackupInstance2(instance, _
    grbit)
```

``` csharp
public static void JetEndExternalBackupInstance2(
    JET_INSTANCE instance,
    EndExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6d712-109">參數</span><span class="sxs-lookup"><span data-stu-id="6d712-109">Parameters</span></span>

  - <span data-ttu-id="6d712-110">instance</span><span class="sxs-lookup"><span data-stu-id="6d712-110">instance</span></span>  
    <span data-ttu-id="6d712-111">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6d712-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="6d712-112">要結束備份的實例。</span><span class="sxs-lookup"><span data-stu-id="6d712-112">The instance to end the backup for.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d712-113">grbit</span><span class="sxs-lookup"><span data-stu-id="6d712-113">grbit</span></span>  
    <span data-ttu-id="6d712-114">型別： [EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="6d712-114">Type: [Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6d712-115">指定備份如何結束的選項。</span><span class="sxs-lookup"><span data-stu-id="6d712-115">Options that specify how the backup ended.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d712-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d712-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6d712-117">參考</span><span class="sxs-lookup"><span data-stu-id="6d712-117">Reference</span></span>

[<span data-ttu-id="6d712-118">Api 類別</span><span class="sxs-lookup"><span data-stu-id="6d712-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6d712-119">Api 成員</span><span class="sxs-lookup"><span data-stu-id="6d712-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6d712-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6d712-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
