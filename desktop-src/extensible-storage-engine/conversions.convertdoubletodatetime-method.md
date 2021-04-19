---
description: 深入瞭解： ConvertDoubleToDateTime 方法
title: ConvertDoubleToDateTime 方法
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979954"
---
# <a name="conversionsconvertdoubletodatetime-method"></a><span data-ttu-id="a4dc0-103">ConvertDoubleToDateTime 方法</span><span class="sxs-lookup"><span data-stu-id="a4dc0-103">Conversions.ConvertDoubleToDateTime method</span></span>

<span data-ttu-id="a4dc0-104">將雙 (的 OA 日期時間格式) 轉換為日期時間。</span><span class="sxs-lookup"><span data-stu-id="a4dc0-104">Convert a double (OA date time format) to a DateTime.</span></span> <span data-ttu-id="a4dc0-105">不同于 DateTime. Date.fromoadate，這不會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a4dc0-105">Unlike DateTime.FromOADate this doesn't throw exceptions.</span></span>

<span data-ttu-id="a4dc0-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a4dc0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a4dc0-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a4dc0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a4dc0-108">語法</span><span class="sxs-lookup"><span data-stu-id="a4dc0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a><span data-ttu-id="a4dc0-109">參數</span><span class="sxs-lookup"><span data-stu-id="a4dc0-109">Parameters</span></span>

  - <span data-ttu-id="a4dc0-110">d</span><span class="sxs-lookup"><span data-stu-id="a4dc0-110">d</span></span>  
    <span data-ttu-id="a4dc0-111">類型： [Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="a4dc0-111">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="a4dc0-112">雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="a4dc0-112">The double value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a4dc0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4dc0-113">Return value</span></span>

<span data-ttu-id="a4dc0-114">類型： [system.object](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="a4dc0-114">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
<span data-ttu-id="a4dc0-115">日期時間。</span><span class="sxs-lookup"><span data-stu-id="a4dc0-115">A DateTime.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a4dc0-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4dc0-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a4dc0-117">參考</span><span class="sxs-lookup"><span data-stu-id="a4dc0-117">Reference</span></span>

[<span data-ttu-id="a4dc0-118">轉換類別</span><span class="sxs-lookup"><span data-stu-id="a4dc0-118">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="a4dc0-119">轉換成員</span><span class="sxs-lookup"><span data-stu-id="a4dc0-119">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="a4dc0-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a4dc0-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
