---
description: '深入瞭解： CimMofDeserializer. DeserializeInstances 方法 (Byte []，UInt32) '
title: 'CimMofDeserializer. DeserializeInstances 方法 (Byte []、UInt32)  (。序列化) '
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 90cc4f9d88afa9f4ec566ff4733995bce8160eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510866"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32"></a><span data-ttu-id="a8af4-103">CimMofDeserializer. DeserializeInstances 方法 (Byte \[ \] ，UInt32) </span><span class="sxs-lookup"><span data-stu-id="a8af4-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32)</span></span>

<span data-ttu-id="a8af4-104">根據序列化資料將 CIM 實例還原序列化。</span><span class="sxs-lookup"><span data-stu-id="a8af4-104">Deserializes CIM instances based on serialized data.</span></span>

<span data-ttu-id="a8af4-105">**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a8af4-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="a8af4-106">**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構</span><span class="sxs-lookup"><span data-stu-id="a8af4-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="a8af4-107">語法</span><span class="sxs-lookup"><span data-stu-id="a8af4-107">Syntax</span></span>

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a><span data-ttu-id="a8af4-108">參數</span><span class="sxs-lookup"><span data-stu-id="a8af4-108">Parameters</span></span>

  - <span data-ttu-id="a8af4-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="a8af4-109">serializedData</span></span>  
    <span data-ttu-id="a8af4-110">類型： [system.string](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="a8af4-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="a8af4-111">包含序列化資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a8af4-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="a8af4-112">Offset</span><span class="sxs-lookup"><span data-stu-id="a8af4-112">offset</span></span>  
    <span data-ttu-id="a8af4-113">類型： [system.object](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="a8af4-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="a8af4-114">開始讀取資料之位置的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="a8af4-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="a8af4-115">當方法傳回時，位移將指向已還原序列化之實例之後的下一個位元組。</span><span class="sxs-lookup"><span data-stu-id="a8af4-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a8af4-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8af4-116">Return value</span></span>

<span data-ttu-id="a8af4-117">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) 。\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="a8af4-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="a8af4-118">可以用來列舉 CIM 類別的[IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)介面。</span><span class="sxs-lookup"><span data-stu-id="a8af4-118">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8af4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8af4-119">See also</span></span>

<span data-ttu-id="a8af4-120">[CimInstance 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a8af4-120">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="a8af4-121">[。序列化命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a8af4-121">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
