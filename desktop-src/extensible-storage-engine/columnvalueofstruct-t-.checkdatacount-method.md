---
description: 深入瞭解： ColumnValueOfStruct <T> 。CheckDataCount 方法
title: ColumnValueOfStruct (T) 。CheckDataCount 方法
TOCTitle: 'CheckDataCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.CheckDataCount(System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334178(v=EXCHG.10)
ms:contentKeyID: 55100977
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.CheckDataCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.CheckDataCount
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fda3fcabe1bb8ff462c37f823d6441720e02c414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193437"
---
# <a name="columnvalueofstructtcheckdatacount-method"></a><span data-ttu-id="845ae-103">ColumnValueOfStruct \<T\> 。CheckDataCount 方法</span><span class="sxs-lookup"><span data-stu-id="845ae-103">ColumnValueOfStruct\<T\>.CheckDataCount method</span></span>

<span data-ttu-id="845ae-104">請確定已抓取的資料完全是結構所需的大小。</span><span class="sxs-lookup"><span data-stu-id="845ae-104">Make sure the retrieved data is exactly the size needed for the structure.</span></span> <span data-ttu-id="845ae-105">如果有不相符的，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="845ae-105">An exception is thrown if there is a mismatch.</span></span>

<span data-ttu-id="845ae-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="845ae-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="845ae-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="845ae-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="845ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="845ae-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub CheckDataCount ( _
    count As Integer _
)
'Usage
Dim count As Integer

Me.CheckDataCount(count)
```

``` csharp
protected void CheckDataCount(
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="845ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="845ae-109">Parameters</span></span>

  - <span data-ttu-id="845ae-110">count</span><span class="sxs-lookup"><span data-stu-id="845ae-110">count</span></span>  
    <span data-ttu-id="845ae-111">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="845ae-111">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="845ae-112">抓取之資料的大小。</span><span class="sxs-lookup"><span data-stu-id="845ae-112">The size of the retrieved data.</span></span>

## <a name="see-also"></a><span data-ttu-id="845ae-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="845ae-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="845ae-114">參考</span><span class="sxs-lookup"><span data-stu-id="845ae-114">Reference</span></span>

[<span data-ttu-id="845ae-115">ColumnValueOfStruct \<T\> 類別</span><span class="sxs-lookup"><span data-stu-id="845ae-115">ColumnValueOfStruct\<T\> class</span></span>](./columnvalueofstruct-t-class.md)

[<span data-ttu-id="845ae-116">ColumnValueOfStruct \<T\> 成員</span><span class="sxs-lookup"><span data-stu-id="845ae-116">ColumnValueOfStruct\<T\> members</span></span>](./columnvalueofstruct-t-members.md)

[<span data-ttu-id="845ae-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="845ae-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
