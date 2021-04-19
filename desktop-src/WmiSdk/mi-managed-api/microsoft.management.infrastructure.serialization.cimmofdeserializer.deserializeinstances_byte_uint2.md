---
description: '深入瞭解： CimMofDeserializer. DeserializeInstances 方法 (Byte []、UInt32、OnClassNeeded、GetIncludedFileContent) '
title: 'CimMofDeserializer. DeserializeInstances 方法 (Byte []、UInt32、OnClassNeeded、GetIncludedFileContent)  (。序列化) '
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
ms.openlocfilehash: 17a8a84f841f07439b716909fbc8d63232032263
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980957"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="73442-103">CimMofDeserializer. DeserializeInstances 方法 (Byte \[ \] 、UInt32、OnClassNeeded、GetIncludedFileContent) </span><span class="sxs-lookup"><span data-stu-id="73442-103">CimMofDeserializer.DeserializeInstances method (Byte\[\], UInt32, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="73442-104">根據序列化資料和回呼將 CIM 實例還原序列化。</span><span class="sxs-lookup"><span data-stu-id="73442-104">Deserializes CIM instances based on serialized data, and callbacks.</span></span>

<span data-ttu-id="73442-105">**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73442-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="73442-106">**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構</span><span class="sxs-lookup"><span data-stu-id="73442-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="73442-107">語法</span><span class="sxs-lookup"><span data-stu-id="73442-107">Syntax</span></span>

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a><span data-ttu-id="73442-108">參數</span><span class="sxs-lookup"><span data-stu-id="73442-108">Parameters</span></span>

  - <span data-ttu-id="73442-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="73442-109">serializedData</span></span>  
    <span data-ttu-id="73442-110">類型： [system.string](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="73442-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="73442-111">包含序列化資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="73442-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="73442-112">Offset</span><span class="sxs-lookup"><span data-stu-id="73442-112">offset</span></span>  
    <span data-ttu-id="73442-113">類型： [system.object](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="73442-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="73442-114">開始讀取資料之位置的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="73442-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="73442-115">當方法傳回時，位移將指向已還原序列化之實例之後的下一個位元組。</span><span class="sxs-lookup"><span data-stu-id="73442-115">When the method returns, the offset will be pointing to the next byte after the deserialized instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="73442-116">onClassNeededCallback</span><span class="sxs-lookup"><span data-stu-id="73442-116">onClassNeededCallback</span></span>  
    <span data-ttu-id="73442-117">類型： [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="73442-117">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="73442-118">回呼函數，用來在還原序列化期間提供要求的類別物件。</span><span class="sxs-lookup"><span data-stu-id="73442-118">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="73442-119">getIncludedFileCallback</span><span class="sxs-lookup"><span data-stu-id="73442-119">getIncludedFileCallback</span></span>  
    <span data-ttu-id="73442-120">類型： [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="73442-120">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="73442-121">回呼函數，用來提供指定檔案的檔案緩衝區內容。</span><span class="sxs-lookup"><span data-stu-id="73442-121">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="73442-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="73442-122">Return value</span></span>

<span data-ttu-id="73442-123">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) 。\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="73442-123">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\></span></span>

<span data-ttu-id="73442-124">可以用來列舉 CIM 類別的[IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)介面。</span><span class="sxs-lookup"><span data-stu-id="73442-124">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="73442-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73442-125">See also</span></span>

<span data-ttu-id="73442-126">[CimInstance 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73442-126">[CimInstance class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))</span></span>  
<span data-ttu-id="73442-127">[。序列化命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73442-127">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
