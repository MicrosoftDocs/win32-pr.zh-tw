---
description: 深入瞭解： InstanceParameters. MaxTemporaryTables 屬性
title: InstanceParameters. MaxTemporaryTables 屬性
TOCTitle: 'MaxTemporaryTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtemporarytables(v=EXCHG.10)
ms:contentKeyID: 55103560
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTemporaryTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5802e512a4ea6a4916ae54c24357dbdad057540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983785"
---
# <a name="instanceparametersmaxtemporarytables-property"></a><span data-ttu-id="05ed2-103">InstanceParameters. MaxTemporaryTables 屬性</span><span class="sxs-lookup"><span data-stu-id="05ed2-103">InstanceParameters.MaxTemporaryTables property</span></span>

<span data-ttu-id="05ed2-104">取得或設定實例所使用之臨時表資源的數目。</span><span class="sxs-lookup"><span data-stu-id="05ed2-104">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="05ed2-105">此設定會影響可同時使用的臨時表數目。</span><span class="sxs-lookup"><span data-stu-id="05ed2-105">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="05ed2-106">如果這個系統參數設定為零，則不會建立暫存資料庫，而且任何需要使用暫存資料庫的活動都將會失敗。</span><span class="sxs-lookup"><span data-stu-id="05ed2-106">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="05ed2-107">這項設定有助於避免建立暫存資料庫所需的 i/o （如果已知不會使用）。</span><span class="sxs-lookup"><span data-stu-id="05ed2-107">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="05ed2-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="05ed2-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="05ed2-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="05ed2-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="05ed2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="05ed2-110">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTemporaryTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTemporaryTables

instance.MaxTemporaryTables = value
```

``` csharp
public int MaxTemporaryTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="05ed2-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="05ed2-111">Property value</span></span>

<span data-ttu-id="05ed2-112">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="05ed2-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="remarks"></a><span data-ttu-id="05ed2-113">備註</span><span class="sxs-lookup"><span data-stu-id="05ed2-113">Remarks</span></span>

<span data-ttu-id="05ed2-114">使用臨時表也需要資料指標資源。</span><span class="sxs-lookup"><span data-stu-id="05ed2-114">The use of a temporary table also requires a cursor resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="05ed2-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05ed2-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="05ed2-116">參考</span><span class="sxs-lookup"><span data-stu-id="05ed2-116">Reference</span></span>

[<span data-ttu-id="05ed2-117">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="05ed2-117">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="05ed2-118">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="05ed2-118">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="05ed2-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="05ed2-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
