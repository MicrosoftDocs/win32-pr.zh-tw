---
description: '深入瞭解： CimMofDeserializer. DeserializeClasses 方法 (Byte []、UInt32、IEnumerable <CimClass> 、string、string、OnClassNeeded、GetIncludedFileContent) '
title: 'CimMofDeserializer. DeserializeClasses 方法 (Byte []、UInt32、IEnumerable (CimClass) 、String、String、OnClassNeeded、GetIncludedFileContent)  (。序列化) '
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},System.String,System.String,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
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
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 5772ca08a94c27e1ae0b110e05192004b9e4df2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510865"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-string-string-onclassneeded-getincludedfilecontent"></a><span data-ttu-id="43ce3-103">CimMofDeserializer. DeserializeClasses 方法 (Byte \[ \] 、UInt32、IEnumerable \<CimClass\> 、string、string、OnClassNeeded、GetIncludedFileContent) </span><span class="sxs-lookup"><span data-stu-id="43ce3-103">CimMofDeserializer.DeserializeClasses method (Byte\[\], UInt32, IEnumerable\<CimClass\>, String, String, OnClassNeeded, GetIncludedFileContent)</span></span>

<span data-ttu-id="43ce3-104">根據序列化資料、父 CIM 類別的集合、電腦和命名空間名稱，以及回呼，將 CIM 類別還原序列化。</span><span class="sxs-lookup"><span data-stu-id="43ce3-104">Deserializes CIM classes based on serialized data, collection of parent CIM classes, computer and namespace names, and callbacks.</span></span>

<span data-ttu-id="43ce3-105">**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43ce3-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="43ce3-106">**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構</span><span class="sxs-lookup"><span data-stu-id="43ce3-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="43ce3-107">語法</span><span class="sxs-lookup"><span data-stu-id="43ce3-107">Syntax</span></span>

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes,
    string computerName,
    string namespaceName,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes,
    String^ computerName,
    String^ namespaceName,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> *
        computerName:string *
        namespaceName:string *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass),
    computerName As String,
    namespaceName As String,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a><span data-ttu-id="43ce3-108">參數</span><span class="sxs-lookup"><span data-stu-id="43ce3-108">Parameters</span></span>

  - <span data-ttu-id="43ce3-109">serializedData</span><span class="sxs-lookup"><span data-stu-id="43ce3-109">serializedData</span></span>  
    <span data-ttu-id="43ce3-110">類型： [system.string](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="43ce3-110">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>
    
    <span data-ttu-id="43ce3-111">包含序列化資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="43ce3-111">A buffer that contains the serialized data.</span></span>

<!-- end list -->

  - <span data-ttu-id="43ce3-112">Offset</span><span class="sxs-lookup"><span data-stu-id="43ce3-112">offset</span></span>  
    <span data-ttu-id="43ce3-113">類型： [system.object](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="43ce3-113">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="43ce3-114">開始讀取資料之位置的位元組位移。</span><span class="sxs-lookup"><span data-stu-id="43ce3-114">The byte offset to the location at which to begin reading the data.</span></span> <span data-ttu-id="43ce3-115">當方法傳回時，位移會指向還原序列化類別之後的下一個位元組。</span><span class="sxs-lookup"><span data-stu-id="43ce3-115">When the method returns, the offset will be pointing to the next byte after the deserialized classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="43ce3-116">類別</span><span class="sxs-lookup"><span data-stu-id="43ce3-116">classes</span></span>  
    <span data-ttu-id="43ce3-117">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) 。\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="43ce3-117">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>
    
    <span data-ttu-id="43ce3-118">父 CIM 類別的選擇性快取。</span><span class="sxs-lookup"><span data-stu-id="43ce3-118">An optional cache of parent CIM classes.</span></span>

<!-- end list -->

  - <span data-ttu-id="43ce3-119">computerName</span><span class="sxs-lookup"><span data-stu-id="43ce3-119">computerName</span></span>  
    [<span data-ttu-id="43ce3-120">System.String</span><span class="sxs-lookup"><span data-stu-id="43ce3-120">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="43ce3-121">電腦名稱。</span><span class="sxs-lookup"><span data-stu-id="43ce3-121">The computer name.</span></span>

<!-- end list -->

  - <span data-ttu-id="43ce3-122">namespaceName</span><span class="sxs-lookup"><span data-stu-id="43ce3-122">namespaceName</span></span>  
    [<span data-ttu-id="43ce3-123">System.String</span><span class="sxs-lookup"><span data-stu-id="43ce3-123">System.String</span></span>](/dotnet/api/system.string?view=netframework-4.8)
    
    <span data-ttu-id="43ce3-124">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="43ce3-124">The namespace name.</span></span>

<!-- end list -->

  - <span data-ttu-id="43ce3-125">onClassNeededCallback</span><span class="sxs-lookup"><span data-stu-id="43ce3-125">onClassNeededCallback</span></span>  
    <span data-ttu-id="43ce3-126">類型： [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span><span class="sxs-lookup"><span data-stu-id="43ce3-126">Type: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)</span></span>
    
    <span data-ttu-id="43ce3-127">回呼函數，用來在還原序列化期間提供要求的類別物件。</span><span class="sxs-lookup"><span data-stu-id="43ce3-127">A callback function used to provide a requested class object during deserialization.</span></span>

<!-- end list -->

  - <span data-ttu-id="43ce3-128">getIncludedFileCallback</span><span class="sxs-lookup"><span data-stu-id="43ce3-128">getIncludedFileCallback</span></span>  
    <span data-ttu-id="43ce3-129">類型： [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span><span class="sxs-lookup"><span data-stu-id="43ce3-129">Type: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)</span></span>
    
    <span data-ttu-id="43ce3-130">回呼函數，用來提供指定檔案的檔案緩衝區內容。</span><span class="sxs-lookup"><span data-stu-id="43ce3-130">A callback function used to provide the file buffer contents of a specified file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="43ce3-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="43ce3-131">Return value</span></span>

<span data-ttu-id="43ce3-132">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) 。\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span><span class="sxs-lookup"><span data-stu-id="43ce3-132">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\></span></span>

<span data-ttu-id="43ce3-133">可以用來列舉 CIM 類別的[IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)介面。</span><span class="sxs-lookup"><span data-stu-id="43ce3-133">An [IEnumerable\<T\>](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) interface that can be used to enumerate the CIM classes.</span></span>

## <a name="see-also"></a><span data-ttu-id="43ce3-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43ce3-134">See also</span></span>

<span data-ttu-id="43ce3-135">[CimClass 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43ce3-135">[CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>  
<span data-ttu-id="43ce3-136">[。序列化命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43ce3-136">[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
