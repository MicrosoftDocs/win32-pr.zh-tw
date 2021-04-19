---
description: 深入瞭解： JET_INSTANCE_INFO szDatabaseFileName 屬性
title: JET_INSTANCE_INFO szDatabaseFileName 屬性
TOCTitle: 'szDatabaseFileName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szdatabasefilename(v=EXCHG.10)
ms:contentKeyID: 55103711
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szDatabaseFileName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55414184fd25a90f3fbb57be8fb5d84264fde5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983884"
---
# <a name="jet_instance_infoszdatabasefilename-property"></a><span data-ttu-id="f15f7-103">JET_INSTANCE_INFO szDatabaseFileName 屬性</span><span class="sxs-lookup"><span data-stu-id="f15f7-103">JET_INSTANCE_INFO.szDatabaseFileName property</span></span>

<span data-ttu-id="f15f7-104">取得字串的集合，每個字串都包含附加至資料庫實例的資料庫檔案名。</span><span class="sxs-lookup"><span data-stu-id="f15f7-104">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="f15f7-105">陣列具有 cDatabases 元素。</span><span class="sxs-lookup"><span data-stu-id="f15f7-105">The array has cDatabases elements.</span></span>

<span data-ttu-id="f15f7-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f15f7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f15f7-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f15f7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f15f7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f15f7-108">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property szDatabaseFileName As IList(Of String)
    Get
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As IList(Of String)

value = instance.szDatabaseFileName
```

``` csharp
public IList<string> szDatabaseFileName { get; }
```

#### <a name="property-value"></a><span data-ttu-id="f15f7-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="f15f7-109">Property value</span></span>

<span data-ttu-id="f15f7-110">類型： [system.object](/dotnet/api/system.collections.generic.ilist-1) 。\<[String](/dotnet/api/system.string)\></span><span class="sxs-lookup"><span data-stu-id="f15f7-110">Type: [System.Collections.Generic.IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\></span></span>  

## <a name="see-also"></a><span data-ttu-id="f15f7-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f15f7-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f15f7-112">參考</span><span class="sxs-lookup"><span data-stu-id="f15f7-112">Reference</span></span>

[<span data-ttu-id="f15f7-113">JET_INSTANCE_INFO 類別</span><span class="sxs-lookup"><span data-stu-id="f15f7-113">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="f15f7-114">JET_INSTANCE_INFO 成員</span><span class="sxs-lookup"><span data-stu-id="f15f7-114">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="f15f7-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f15f7-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
