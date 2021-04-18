---
description: 深入瞭解： SystemParameters. CacheSize 屬性
title: SystemParameters. CacheSize 屬性
TOCTitle: 'CacheSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesize(v=EXCHG.10)
ms:contentKeyID: 55104109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0981f02df3b807ab56fa20922d1e245f00c2df34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194993"
---
# <a name="systemparameterscachesize-property"></a><span data-ttu-id="addff-103">SystemParameters. CacheSize 屬性</span><span class="sxs-lookup"><span data-stu-id="addff-103">SystemParameters.CacheSize property</span></span>

<span data-ttu-id="addff-104">取得或設定頁面中資料庫快取的大小。</span><span class="sxs-lookup"><span data-stu-id="addff-104">Gets or sets the size of the database cache in pages.</span></span> <span data-ttu-id="addff-105">根據預設，資料庫快取會自動調整其大小，將此屬性設定為非零值會導致快取將本身調整為目標大小。</span><span class="sxs-lookup"><span data-stu-id="addff-105">By default the database cache will automatically tune its size, setting this property to a non-zero value will cause the cache to adjust itself to the target size.</span></span>

<span data-ttu-id="addff-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="addff-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="addff-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="addff-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="addff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="addff-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSize As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSize

SystemParameters.CacheSize = value
```

``` csharp
public static int CacheSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="addff-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="addff-109">Property value</span></span>

<span data-ttu-id="addff-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="addff-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="addff-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="addff-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="addff-112">參考</span><span class="sxs-lookup"><span data-stu-id="addff-112">Reference</span></span>

[<span data-ttu-id="addff-113">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="addff-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="addff-114">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="addff-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="addff-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="addff-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
