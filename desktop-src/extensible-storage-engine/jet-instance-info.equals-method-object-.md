---
description: 深入瞭解： JET_INSTANCE_INFO。物件)  (Equals 方法
title: JET_INSTANCE_INFO。物件)  (Equals 方法
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.equals(v=EXCHG.10)
ms:contentKeyID: 55103694
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca19f5886d9950a5d185de8e91687ec984e9db95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980555"
---
# <a name="jet_instance_infoequals-method-object"></a><span data-ttu-id="e1f24-103">JET_INSTANCE_INFO。物件)  (Equals 方法</span><span class="sxs-lookup"><span data-stu-id="e1f24-103">JET_INSTANCE_INFO.Equals method (Object)</span></span>

<span data-ttu-id="e1f24-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="e1f24-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="e1f24-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e1f24-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e1f24-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e1f24-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f24-107">語法</span><span class="sxs-lookup"><span data-stu-id="e1f24-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_INSTANCE_INFO
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a><span data-ttu-id="e1f24-108">參數</span><span class="sxs-lookup"><span data-stu-id="e1f24-108">Parameters</span></span>

  - <span data-ttu-id="e1f24-109">obj</span><span class="sxs-lookup"><span data-stu-id="e1f24-109">obj</span></span>  
    <span data-ttu-id="e1f24-110">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="e1f24-110">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="e1f24-111">與這個執行個體相互比較的物件。</span><span class="sxs-lookup"><span data-stu-id="e1f24-111">An object to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e1f24-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1f24-112">Return value</span></span>

<span data-ttu-id="e1f24-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e1f24-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e1f24-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="e1f24-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e1f24-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1f24-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e1f24-116">參考</span><span class="sxs-lookup"><span data-stu-id="e1f24-116">Reference</span></span>

[<span data-ttu-id="e1f24-117">JET_INSTANCE_INFO 類別</span><span class="sxs-lookup"><span data-stu-id="e1f24-117">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="e1f24-118">JET_INSTANCE_INFO 成員</span><span class="sxs-lookup"><span data-stu-id="e1f24-118">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="e1f24-119">等於多載</span><span class="sxs-lookup"><span data-stu-id="e1f24-119">Equals overload</span></span>](./jet-instance-info.equals-method.md)

[<span data-ttu-id="e1f24-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e1f24-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
