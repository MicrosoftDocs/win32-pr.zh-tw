---
description: 深入瞭解： VistaGrbits. IndexCrossProduct 欄位
title: VistaGrbits. IndexCrossProduct 欄位)  (的欄位
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1b16f741c63d455d18a887331505080aef62990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945449"
---
# <a name="vistagrbitsindexcrossproduct-field"></a><span data-ttu-id="1336c-103">VistaGrbits. IndexCrossProduct 欄位</span><span class="sxs-lookup"><span data-stu-id="1336c-103">VistaGrbits.IndexCrossProduct field</span></span>

<span data-ttu-id="1336c-104">針對具有多值資料行之多個索引鍵資料行的索引指定此旗標，會導致針對這些索引鍵資料行中的所有值交叉乘積的每個結果建立索引項目。</span><span class="sxs-lookup"><span data-stu-id="1336c-104">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="1336c-105">否則，索引在最重要的索引鍵資料行中的每個多重值都只會有一個專案，這是多重值資料行，而每個索引項目會使用任何其他索引鍵資料行中的第一個多重值（多重值資料行）。</span><span class="sxs-lookup"><span data-stu-id="1336c-105">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="1336c-106">例如，如果您在資料行 A 上針對具有值 "1" 和 "2" 的資料行 A 指定此旗標，則會建立下列索引項目： "red"、"1"、"red"、"2"、"blue"、"1"、"blue"、"2"。</span><span class="sxs-lookup"><span data-stu-id="1336c-106">For example, if you specified this flag for an index over column A that has the values "red" and "blue" and over column B that has the values "1" and "2" then the following index entries would be created: "red", "1"; "red", "2"; "blue", "1"; "blue", "2".</span></span> <span data-ttu-id="1336c-107">否則，將會建立下列索引項目： "red"、"1"、"blue"、"1"。</span><span class="sxs-lookup"><span data-stu-id="1336c-107">Otherwise, the following index entries would be created: "red", "1"; "blue", "1".</span></span>

<span data-ttu-id="1336c-108">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="1336c-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="1336c-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1336c-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1336c-110">語法</span><span class="sxs-lookup"><span data-stu-id="1336c-110">Syntax</span></span>

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a><span data-ttu-id="1336c-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1336c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1336c-112">參考</span><span class="sxs-lookup"><span data-stu-id="1336c-112">Reference</span></span>

[<span data-ttu-id="1336c-113">VistaGrbits 類別</span><span class="sxs-lookup"><span data-stu-id="1336c-113">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="1336c-114">VistaGrbits 成員</span><span class="sxs-lookup"><span data-stu-id="1336c-114">VistaGrbits members</span></span>](./vistagrbits-members.md)

[<span data-ttu-id="1336c-115">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="1336c-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
