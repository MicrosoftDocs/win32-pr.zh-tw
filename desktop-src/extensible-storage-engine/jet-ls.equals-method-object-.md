---
description: 深入瞭解： JET_LS。物件)  (Equals 方法
title: JET_LS。物件)  (Equals 方法
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.equals(v=EXCHG.10)
ms:contentKeyID: 39511834
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 033936eb1f8d5176eed1b052ba5ee5332c8c5a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193810"
---
# <a name="jet_lsequals-method-object"></a><span data-ttu-id="50c05-103">JET_LS。物件)  (Equals 方法</span><span class="sxs-lookup"><span data-stu-id="50c05-103">JET_LS.Equals method (Object)</span></span>

<span data-ttu-id="50c05-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="50c05-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="50c05-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50c05-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50c05-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="50c05-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50c05-107">語法</span><span class="sxs-lookup"><span data-stu-id="50c05-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_LS
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a><span data-ttu-id="50c05-108">參數</span><span class="sxs-lookup"><span data-stu-id="50c05-108">Parameters</span></span>

  - <span data-ttu-id="50c05-109">obj</span><span class="sxs-lookup"><span data-stu-id="50c05-109">obj</span></span>  
    <span data-ttu-id="50c05-110">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="50c05-110">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="50c05-111">與這個執行個體相互比較的物件。</span><span class="sxs-lookup"><span data-stu-id="50c05-111">An object to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50c05-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="50c05-112">Return value</span></span>

<span data-ttu-id="50c05-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="50c05-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="50c05-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="50c05-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="50c05-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50c05-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50c05-116">參考</span><span class="sxs-lookup"><span data-stu-id="50c05-116">Reference</span></span>

[<span data-ttu-id="50c05-117">JET_LS 結構</span><span class="sxs-lookup"><span data-stu-id="50c05-117">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="50c05-118">JET_LS 成員</span><span class="sxs-lookup"><span data-stu-id="50c05-118">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="50c05-119">等於多載</span><span class="sxs-lookup"><span data-stu-id="50c05-119">Equals overload</span></span>](./jet-ls.equals-method.md)

[<span data-ttu-id="50c05-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="50c05-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
