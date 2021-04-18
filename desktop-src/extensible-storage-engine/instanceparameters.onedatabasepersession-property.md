---
description: 深入瞭解： InstanceParameters. OneDatabasePerSession 屬性
title: InstanceParameters. OneDatabasePerSession 屬性
TOCTitle: 'OneDatabasePerSession property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.onedatabasepersession(v=EXCHG.10)
ms:contentKeyID: 55103319
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.OneDatabasePerSession
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_OneDatabasePerSession
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_OneDatabasePerSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c130a00b8fcbcbcf6a8fc7bbdbbad6a4e36f218e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976365"
---
# <a name="instanceparametersonedatabasepersession-property"></a><span data-ttu-id="1f212-103">InstanceParameters. OneDatabasePerSession 屬性</span><span class="sxs-lookup"><span data-stu-id="1f212-103">InstanceParameters.OneDatabasePerSession property</span></span>

<span data-ttu-id="1f212-104">取得或設定值，這個值表示一次是否允許指定的會話使用 JetOpenDatabase 來開啟單一資料庫。</span><span class="sxs-lookup"><span data-stu-id="1f212-104">Gets or sets a value indicating whether only one database is allowed to be opened using JetOpenDatabase by a given session at one time.</span></span> <span data-ttu-id="1f212-105">這項限制會排除暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="1f212-105">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="1f212-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f212-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1f212-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1f212-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f212-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f212-108">Syntax</span></span>

``` vb
'Declaration
Public Property OneDatabasePerSession As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.OneDatabasePerSession

instance.OneDatabasePerSession = value
```

``` csharp
public bool OneDatabasePerSession { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1f212-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1f212-109">Property value</span></span>

<span data-ttu-id="1f212-110">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="1f212-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1f212-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f212-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f212-112">參考</span><span class="sxs-lookup"><span data-stu-id="1f212-112">Reference</span></span>

[<span data-ttu-id="1f212-113">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="1f212-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="1f212-114">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="1f212-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="1f212-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1f212-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
