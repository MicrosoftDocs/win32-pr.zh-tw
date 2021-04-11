---
description: 深入瞭解： SystemParameters. CacheSizeMax 屬性
title: SystemParameters. CacheSizeMax 屬性
TOCTitle: 'CacheSizeMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesizemax(v=EXCHG.10)
ms:contentKeyID: 55104037
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7b03df288a0263cf6b79281f5ed79330dfd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194871"
---
# <a name="systemparameterscachesizemax-property"></a><span data-ttu-id="d0416-103">SystemParameters. CacheSizeMax 屬性</span><span class="sxs-lookup"><span data-stu-id="d0416-103">SystemParameters.CacheSizeMax property</span></span>

<span data-ttu-id="d0416-104">取得或設定資料庫頁面快取的大小上限。</span><span class="sxs-lookup"><span data-stu-id="d0416-104">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="d0416-105">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="d0416-105">The size is in database pages.</span></span> <span data-ttu-id="d0416-106">如果此參數保留為其預設值，則在呼叫 JetInit 時，會將快取的大小上限設定為實體記憶體的大小。</span><span class="sxs-lookup"><span data-stu-id="d0416-106">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span>

<span data-ttu-id="d0416-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0416-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d0416-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d0416-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0416-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0416-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSizeMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSizeMax

SystemParameters.CacheSizeMax = value
```

``` csharp
public static int CacheSizeMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="d0416-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="d0416-110">Property value</span></span>

<span data-ttu-id="d0416-111">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d0416-111">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d0416-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0416-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0416-113">參考</span><span class="sxs-lookup"><span data-stu-id="d0416-113">Reference</span></span>

[<span data-ttu-id="d0416-114">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="d0416-114">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="d0416-115">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="d0416-115">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="d0416-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d0416-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
