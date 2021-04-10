---
description: 深入瞭解： CompareOptionsFromLCMapFlags 方法
title: CompareOptionsFromLCMapFlags 方法
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191664"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a><span data-ttu-id="7c863-103">CompareOptionsFromLCMapFlags 方法</span><span class="sxs-lookup"><span data-stu-id="7c863-103">Conversions.CompareOptionsFromLCMapFlags method</span></span>

<span data-ttu-id="7c863-104">針對 LCMapFlags 指定旗標，將它們轉換成比較選項。</span><span class="sxs-lookup"><span data-stu-id="7c863-104">Given flags for LCMapFlags, turn them into compare options.</span></span> <span data-ttu-id="7c863-105">忽略未知的選項。</span><span class="sxs-lookup"><span data-stu-id="7c863-105">Unknown options are ignored.</span></span>

<span data-ttu-id="7c863-106">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="7c863-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="7c863-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7c863-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7c863-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7c863-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7c863-109">語法</span><span class="sxs-lookup"><span data-stu-id="7c863-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a><span data-ttu-id="7c863-110">參數</span><span class="sxs-lookup"><span data-stu-id="7c863-110">Parameters</span></span>

  - <span data-ttu-id="7c863-111">lcmapFlags</span><span class="sxs-lookup"><span data-stu-id="7c863-111">lcmapFlags</span></span>  
    <span data-ttu-id="7c863-112">類型： [system.object](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="7c863-112">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="7c863-113">LCMapString 旗標。</span><span class="sxs-lookup"><span data-stu-id="7c863-113">LCMapString flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7c863-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c863-114">Return value</span></span>

<span data-ttu-id="7c863-115">類型： [CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="7c863-115">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
<span data-ttu-id="7c863-116">描述 (已知) 旗標的 CompareOptions。</span><span class="sxs-lookup"><span data-stu-id="7c863-116">CompareOptions describing the (known) flags.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c863-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c863-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7c863-118">參考</span><span class="sxs-lookup"><span data-stu-id="7c863-118">Reference</span></span>

[<span data-ttu-id="7c863-119">轉換類別</span><span class="sxs-lookup"><span data-stu-id="7c863-119">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="7c863-120">轉換成員</span><span class="sxs-lookup"><span data-stu-id="7c863-120">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="7c863-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7c863-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
