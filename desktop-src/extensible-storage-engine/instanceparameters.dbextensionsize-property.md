---
description: 深入瞭解： InstanceParameters. DbExtensionSize 屬性
title: InstanceParameters. DbExtensionSize 屬性
TOCTitle: 'DbExtensionSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.dbextensionsize(v=EXCHG.10)
ms:contentKeyID: 55107443
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_DbExtensionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.DbExtensionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_DbExtensionSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 402c37ca649a9e9ff70435c8a8ef58f79376842b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977031"
---
# <a name="instanceparametersdbextensionsize-property"></a><span data-ttu-id="bdfc5-103">InstanceParameters. DbExtensionSize 屬性</span><span class="sxs-lookup"><span data-stu-id="bdfc5-103">InstanceParameters.DbExtensionSize property</span></span>

<span data-ttu-id="bdfc5-104">取得或設定每次需要成長以容納更多資料時，資料庫檔案中加入的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="bdfc5-104">Gets or sets the number of pages that are added to a database file each time it needs to grow to accommodate more data.</span></span>

<span data-ttu-id="bdfc5-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bdfc5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bdfc5-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bdfc5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bdfc5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdfc5-107">Syntax</span></span>

``` vb
'Declaration
Public Property DbExtensionSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.DbExtensionSize

instance.DbExtensionSize = value
```

``` csharp
public int DbExtensionSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="bdfc5-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="bdfc5-108">Property value</span></span>

<span data-ttu-id="bdfc5-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bdfc5-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="bdfc5-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdfc5-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bdfc5-111">參考</span><span class="sxs-lookup"><span data-stu-id="bdfc5-111">Reference</span></span>

[<span data-ttu-id="bdfc5-112">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="bdfc5-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="bdfc5-113">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="bdfc5-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="bdfc5-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bdfc5-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
