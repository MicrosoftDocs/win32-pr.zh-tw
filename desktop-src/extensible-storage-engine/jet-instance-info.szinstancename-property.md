---
description: 深入瞭解： JET_INSTANCE_INFO szInstanceName 屬性
title: JET_INSTANCE_INFO szInstanceName 屬性
TOCTitle: 'szInstanceName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szInstanceName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szinstancename(v=EXCHG.10)
ms:contentKeyID: 55103713
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szInstanceName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szInstanceName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.set_szInstanceName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szInstanceName
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edaa331fce5564672ac844f6977ea5ae1688a38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193823"
---
# <a name="jet_instance_infoszinstancename-property"></a><span data-ttu-id="d4bf4-103">JET_INSTANCE_INFO szInstanceName 屬性</span><span class="sxs-lookup"><span data-stu-id="d4bf4-103">JET_INSTANCE_INFO.szInstanceName property</span></span>

<span data-ttu-id="d4bf4-104">取得資料庫實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4bf4-104">Gets the name of the database instance.</span></span> <span data-ttu-id="d4bf4-105">如果實例沒有名稱，這個值可以是 null。</span><span class="sxs-lookup"><span data-stu-id="d4bf4-105">This value can be null if the instance does not have a name.</span></span>

<span data-ttu-id="d4bf4-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d4bf4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d4bf4-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d4bf4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d4bf4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4bf4-108">Syntax</span></span>

``` vb
'Declaration
Public Property szInstanceName As String
    Get
    Private Set
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As String

value = instance.szInstanceName
```

``` csharp
public string szInstanceName { get; private set; }
```

#### <a name="property-value"></a><span data-ttu-id="d4bf4-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d4bf4-109">Property value</span></span>

<span data-ttu-id="d4bf4-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d4bf4-110">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d4bf4-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4bf4-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d4bf4-112">參考</span><span class="sxs-lookup"><span data-stu-id="d4bf4-112">Reference</span></span>

[<span data-ttu-id="d4bf4-113">JET_INSTANCE_INFO 類別</span><span class="sxs-lookup"><span data-stu-id="d4bf4-113">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="d4bf4-114">JET_INSTANCE_INFO 成員</span><span class="sxs-lookup"><span data-stu-id="d4bf4-114">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="d4bf4-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d4bf4-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
