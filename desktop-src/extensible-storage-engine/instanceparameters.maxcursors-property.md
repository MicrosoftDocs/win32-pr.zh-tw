---
description: 深入瞭解： InstanceParameters. MaxCursors 屬性
title: InstanceParameters. MaxCursors 屬性
TOCTitle: 'MaxCursors property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxcursors(v=EXCHG.10)
ms:contentKeyID: 55103565
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxCursors
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 029ff7c41916e668f532be60f018870f30e487ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992105"
---
# <a name="instanceparametersmaxcursors-property"></a><span data-ttu-id="c117a-103">InstanceParameters. MaxCursors 屬性</span><span class="sxs-lookup"><span data-stu-id="c117a-103">InstanceParameters.MaxCursors property</span></span>

<span data-ttu-id="c117a-104">取得或設定保留給這個實例的資料指標資源數目。</span><span class="sxs-lookup"><span data-stu-id="c117a-104">Gets or sets the number of cursor resources reserved for this instance.</span></span> <span data-ttu-id="c117a-105">資料指標資源會直接對應至 JET_TABLEID。</span><span class="sxs-lookup"><span data-stu-id="c117a-105">A cursor resource directly corresponds to a JET_TABLEID.</span></span>

<span data-ttu-id="c117a-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c117a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c117a-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c117a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c117a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c117a-108">Syntax</span></span>

``` vb
'Declaration
Public Property MaxCursors As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxCursors

instance.MaxCursors = value
```

``` csharp
public int MaxCursors { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c117a-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="c117a-109">Property value</span></span>

<span data-ttu-id="c117a-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c117a-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c117a-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c117a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c117a-112">參考</span><span class="sxs-lookup"><span data-stu-id="c117a-112">Reference</span></span>

[<span data-ttu-id="c117a-113">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="c117a-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="c117a-114">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="c117a-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="c117a-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c117a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
