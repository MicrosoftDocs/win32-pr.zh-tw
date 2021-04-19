---
description: 深入瞭解： InstanceParameters. PageTempDBMin 屬性
title: InstanceParameters. PageTempDBMin 屬性
TOCTitle: 'PageTempDBMin property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.pagetempdbmin(v=EXCHG.10)
ms:contentKeyID: 55103558
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06825762485ad52743d585ce0fed86bd1739cd21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974727"
---
# <a name="instanceparameterspagetempdbmin-property"></a><span data-ttu-id="726af-103">InstanceParameters. PageTempDBMin 屬性</span><span class="sxs-lookup"><span data-stu-id="726af-103">InstanceParameters.PageTempDBMin property</span></span>

<span data-ttu-id="726af-104">取得或設定暫存資料庫的初始大小。</span><span class="sxs-lookup"><span data-stu-id="726af-104">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="726af-105">大小是在資料庫頁面中。</span><span class="sxs-lookup"><span data-stu-id="726af-105">The size is in database pages.</span></span> <span data-ttu-id="726af-106">大小為零表示應該使用一般資料庫的預設大小。</span><span class="sxs-lookup"><span data-stu-id="726af-106">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="726af-107">小型應用程式通常需要將暫存資料庫設定為盡可能小。</span><span class="sxs-lookup"><span data-stu-id="726af-107">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="726af-108">將此參數設定為 [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) ，可以達到最小的暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="726af-108">Setting this parameter to [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) will achieve the smallest temporary database possible.</span></span>

<span data-ttu-id="726af-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="726af-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="726af-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="726af-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="726af-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="726af-111">Syntax</span></span>

``` vb
'Declaration
Public Property PageTempDBMin As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PageTempDBMin

instance.PageTempDBMin = value
```

``` csharp
public int PageTempDBMin { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="726af-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="726af-112">Property value</span></span>

<span data-ttu-id="726af-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="726af-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="726af-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="726af-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="726af-115">參考</span><span class="sxs-lookup"><span data-stu-id="726af-115">Reference</span></span>

[<span data-ttu-id="726af-116">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="726af-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="726af-117">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="726af-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="726af-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="726af-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
