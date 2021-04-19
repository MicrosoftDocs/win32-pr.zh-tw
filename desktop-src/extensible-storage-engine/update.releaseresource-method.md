---
description: 深入瞭解： ReleaseResource 方法
title: ReleaseResource 方法
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104200
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.ReleaseResource
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72a17022ff91f278b6a5ac4f84fc7e2d70bb04bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973093"
---
# <a name="updatereleaseresource-method"></a><span data-ttu-id="abc84-103">ReleaseResource 方法</span><span class="sxs-lookup"><span data-stu-id="abc84-103">Update.ReleaseResource method</span></span>

<span data-ttu-id="abc84-104">當交易在作用中處置時呼叫。</span><span class="sxs-lookup"><span data-stu-id="abc84-104">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="abc84-105">這應該會復原交易。</span><span class="sxs-lookup"><span data-stu-id="abc84-105">This should rollback the transaction.</span></span>

<span data-ttu-id="abc84-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="abc84-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="abc84-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="abc84-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="abc84-108">語法</span><span class="sxs-lookup"><span data-stu-id="abc84-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="see-also"></a><span data-ttu-id="abc84-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abc84-109">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="abc84-110">參考</span><span class="sxs-lookup"><span data-stu-id="abc84-110">Reference</span></span>

[<span data-ttu-id="abc84-111">Update 類別</span><span class="sxs-lookup"><span data-stu-id="abc84-111">Update class</span></span>](./update-class.md)

[<span data-ttu-id="abc84-112">更新成員</span><span class="sxs-lookup"><span data-stu-id="abc84-112">Update members</span></span>](./update-members.md)

[<span data-ttu-id="abc84-113">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="abc84-113">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
