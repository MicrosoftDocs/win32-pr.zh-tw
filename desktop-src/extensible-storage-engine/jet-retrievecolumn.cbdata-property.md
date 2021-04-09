---
description: 深入瞭解： JET_RETRIEVECOLUMN cbData 屬性
title: JET_RETRIEVECOLUMN cbData 屬性
TOCTitle: 'cbData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.cbData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.cbdata(v=EXCHG.10)
ms:contentKeyID: 55103810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.cbData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_cbData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_cbData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.cbData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b91e78d31e2c82b0825da5e320fef558f790caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690916"
---
# <a name="jet_retrievecolumncbdata-property"></a><span data-ttu-id="16279-103">JET_RETRIEVECOLUMN cbData 屬性</span><span class="sxs-lookup"><span data-stu-id="16279-103">JET_RETRIEVECOLUMN.cbData property</span></span>

<span data-ttu-id="16279-104">取得或設定 [pvData](./jet-retrievecolumn.pvdata-property.md) 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="16279-104">Gets or sets the size of the [pvData](./jet-retrievecolumn.pvdata-property.md) buffer, in bytes.</span></span> <span data-ttu-id="16279-105">抓取資料行作業將不會在 pvData 中儲存比 cbData 更多的資料。</span><span class="sxs-lookup"><span data-stu-id="16279-105">The retrieve column operation will not store more data in pvData than cbData.</span></span>

<span data-ttu-id="16279-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="16279-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="16279-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="16279-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="16279-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="16279-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbData As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.cbData

instance.cbData = value
```

``` csharp
public int cbData { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="16279-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="16279-109">Property value</span></span>

<span data-ttu-id="16279-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="16279-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="16279-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16279-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="16279-112">參考</span><span class="sxs-lookup"><span data-stu-id="16279-112">Reference</span></span>

[<span data-ttu-id="16279-113">JET_RETRIEVECOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="16279-113">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="16279-114">JET_RETRIEVECOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="16279-114">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="16279-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="16279-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
