---
description: '深入瞭解： CimMofDeserializer. DeserializeClasses 方法 (Byte []、UInt32、IEnumerable <CimClass>) '
title: 'CimMofDeserializer. DeserializeClasses 方法 (Byte []、UInt32、IEnumerable (CimClass) )  () '
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass)) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass})
ms.date: 11/13/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: edcdb84e9c3a3fe7a070263385c9ee6551341152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975890"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass"></a><span data-ttu-id="2f59f-103">CimMofDeserializer. DeserializeClasses 方法 (Byte \[ \] ，UInt32，IEnumerable \<CimClass\>) </span><span class="sxs-lookup"><span data-stu-id="2f59f-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>)</span></span>

<span data-ttu-id="2f59f-104">將以序列化資料為基礎的 CIM 類別還原序列化，以及父 CIM 類別的集合。</span><span class="sxs-lookup"><span data-stu-id="2f59f-104">Deserializes CIM classes based on serialized data, and a collection of parent CIM classes.</span></span>

<span data-ttu-id="2f59f-105">**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f59f-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="2f59f-106">**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構</span><span class="sxs-lookup"><span data-stu-id="2f59f-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="2f59f-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f59f-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass)
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="2f59f-108">參數</span><span class="sxs-lookup"><span data-stu-id="2f59f-108">Parameters</span></span>

  - <span data-ttu-id="2f59f-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="2f59f-109">serializedData</span></span>  
    <span data-ttu-id="2f59f-110">類型： [system.string](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="2f59f-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="2f59f-111">包含序列化資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2f59f-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="2f59f-112">Offset</span><span class="sxs-lookup"><span data-stu-id="2f59f-112">offset</span></span>  
    <span data-ttu-id="2f59f-113">類型： [system.object](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="2f59f-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="2f59f-114">開始讀取資料之位置的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="2f59f-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="2f59f-115">當方法傳回時，位移會指向還原序列化類別之後的下一個位元組。</span><span class="sxs-lookup"><span data-stu-id="2f59f-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="2f59f-116">類別</span><span class="sxs-lookup"><span data-stu-id="2f59f-116">classes</span></span>  
    <span data-ttu-id="2f59f-117">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) 。\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="2f59f-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="2f59f-118">父 CIM 類別的選擇性快取。</span><span class="sxs-lookup"><span data-stu-id="2f59f-118">An optional cache of parent CIM classes.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2f59f-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f59f-119">Return value</span></span>

<span data-ttu-id="2f59f-120">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) 。\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="2f59f-120">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="2f59f-121">可以用來列舉 CIM 類別的[IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)介面。</span><span class="sxs-lookup"><span data-stu-id="2f59f-121">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f59f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f59f-122">See also</span></span>

<span data-ttu-id="2f59f-123">[CimClass 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f59f-123">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="2f59f-124">[。序列化命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f59f-124">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
