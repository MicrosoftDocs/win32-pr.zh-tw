---
description: 深入瞭解： LCMapFlagsFromCompareOptions 方法
title: LCMapFlagsFromCompareOptions 方法
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976771"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a><span data-ttu-id="0fd35-103">LCMapFlagsFromCompareOptions 方法</span><span class="sxs-lookup"><span data-stu-id="0fd35-103">Conversions.LCMapFlagsFromCompareOptions method</span></span>

<span data-ttu-id="0fd35-104">提供 CompareOptions，並將其轉換成 LCMapString 的旗標。</span><span class="sxs-lookup"><span data-stu-id="0fd35-104">Give CompareOptions, turn them into flags from LCMapString.</span></span> <span data-ttu-id="0fd35-105">忽略未知的選項。</span><span class="sxs-lookup"><span data-stu-id="0fd35-105">Unknown options are ignored.</span></span>

<span data-ttu-id="0fd35-106">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="0fd35-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="0fd35-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0fd35-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0fd35-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0fd35-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd35-109">語法</span><span class="sxs-lookup"><span data-stu-id="0fd35-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a><span data-ttu-id="0fd35-110">參數</span><span class="sxs-lookup"><span data-stu-id="0fd35-110">Parameters</span></span>

  - <span data-ttu-id="0fd35-111">compareOptions</span><span class="sxs-lookup"><span data-stu-id="0fd35-111">compareOptions</span></span>  
    <span data-ttu-id="0fd35-112">類型： [CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="0fd35-112">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
    
    <span data-ttu-id="0fd35-113">要轉換的選項。</span><span class="sxs-lookup"><span data-stu-id="0fd35-113">The options to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0fd35-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fd35-114">Return value</span></span>

<span data-ttu-id="0fd35-115">類型： [system.object](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="0fd35-115">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
<span data-ttu-id="0fd35-116">符合比較選項的 LCMapString 旗標。</span><span class="sxs-lookup"><span data-stu-id="0fd35-116">The LCMapString flags that match the compare options.</span></span> <span data-ttu-id="0fd35-117">系統會忽略不支援的選項。</span><span class="sxs-lookup"><span data-stu-id="0fd35-117">Unsupported options are ignored.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0fd35-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fd35-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0fd35-119">參考</span><span class="sxs-lookup"><span data-stu-id="0fd35-119">Reference</span></span>

[<span data-ttu-id="0fd35-120">轉換類別</span><span class="sxs-lookup"><span data-stu-id="0fd35-120">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="0fd35-121">轉換成員</span><span class="sxs-lookup"><span data-stu-id="0fd35-121">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="0fd35-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0fd35-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
