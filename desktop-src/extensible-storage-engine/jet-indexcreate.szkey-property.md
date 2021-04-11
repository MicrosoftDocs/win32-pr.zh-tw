---
description: 深入瞭解： JET_INDEXCREATE szKey 屬性
title: JET_INDEXCREATE szKey 屬性
TOCTitle: 'szKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.szkey(v=EXCHG.10)
ms:contentKeyID: 55103656
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86ade65ee28eef6314d31653772b0c22657476d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320496"
---
# <a name="jet_indexcreateszkey-property"></a><span data-ttu-id="c2ed7-103">JET_INDEXCREATE szKey 屬性</span><span class="sxs-lookup"><span data-stu-id="c2ed7-103">JET_INDEXCREATE.szKey property</span></span>

<span data-ttu-id="c2ed7-104">取得或設定索引鍵的描述。</span><span class="sxs-lookup"><span data-stu-id="c2ed7-104">Gets or sets the description of the index key.</span></span> <span data-ttu-id="c2ed7-105">這是以 null 分隔之標記的雙 null 結束字串。</span><span class="sxs-lookup"><span data-stu-id="c2ed7-105">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="c2ed7-106">每個標記都屬於表單 \[ 方向規範的資料 \] \[ 行名稱 \] ，其中的方向規格為 "+" 或 "-"。</span><span class="sxs-lookup"><span data-stu-id="c2ed7-106">Each token is of the form \[direction-specifier\]\[column-name\], where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="c2ed7-107">例如，"+ abc \\ 0-def \\ 0 + ghi 0" 的 szKey \\ 會以遞增順序來編制三個數據行 "abc" (的索引) 、"def" (以遞減順序) 和 "ghi" (遞增順序) 。</span><span class="sxs-lookup"><span data-stu-id="c2ed7-107">for example, a szKey of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span>

<span data-ttu-id="c2ed7-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c2ed7-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c2ed7-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c2ed7-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ed7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2ed7-110">Syntax</span></span>

``` vb
'Declaration
Public Property szKey As String
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As String

value = instance.szKey

instance.szKey = value
```

``` csharp
public string szKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c2ed7-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="c2ed7-111">Property value</span></span>

<span data-ttu-id="c2ed7-112">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c2ed7-112">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c2ed7-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2ed7-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c2ed7-114">參考</span><span class="sxs-lookup"><span data-stu-id="c2ed7-114">Reference</span></span>

[<span data-ttu-id="c2ed7-115">JET_INDEXCREATE 類別</span><span class="sxs-lookup"><span data-stu-id="c2ed7-115">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="c2ed7-116">JET_INDEXCREATE 成員</span><span class="sxs-lookup"><span data-stu-id="c2ed7-116">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="c2ed7-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c2ed7-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
