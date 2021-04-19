---
description: 深入瞭解： InstanceParameters. PreferredVerPages 屬性
title: InstanceParameters. PreferredVerPages 屬性
TOCTitle: 'PreferredVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.preferredverpages(v=EXCHG.10)
ms:contentKeyID: 55103322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PreferredVerPages
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 067d41cd3fb945b2f18d3cd6154b1eef6793b1e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991875"
---
# <a name="instanceparameterspreferredverpages-property"></a><span data-ttu-id="44870-103">InstanceParameters. PreferredVerPages 屬性</span><span class="sxs-lookup"><span data-stu-id="44870-103">InstanceParameters.PreferredVerPages property</span></span>

<span data-ttu-id="44870-104">取得或設定保留給此實例之版本存放區頁面的慣用數目。</span><span class="sxs-lookup"><span data-stu-id="44870-104">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="44870-105">如果版本存放區的大小超過此臨界值，則只會針對選擇性的背景工作（例如回收資料庫中已刪除的空間）使用任何資訊，而不會犧牲保存交易資訊的空間。</span><span class="sxs-lookup"><span data-stu-id="44870-105">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="44870-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44870-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44870-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="44870-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44870-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="44870-108">Syntax</span></span>

``` vb
'Declaration
Public Property PreferredVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PreferredVerPages

instance.PreferredVerPages = value
```

``` csharp
public int PreferredVerPages { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="44870-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="44870-109">Property value</span></span>

<span data-ttu-id="44870-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="44870-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="44870-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44870-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44870-112">參考</span><span class="sxs-lookup"><span data-stu-id="44870-112">Reference</span></span>

[<span data-ttu-id="44870-113">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="44870-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="44870-114">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="44870-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="44870-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="44870-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
