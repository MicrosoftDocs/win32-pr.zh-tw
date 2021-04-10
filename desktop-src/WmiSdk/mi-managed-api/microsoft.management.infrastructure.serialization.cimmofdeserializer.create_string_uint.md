---
description: 深入瞭解： CimMofDeserializer (字串，UInt32) 的 Create 方法
title: CimMofDeserializer.Create 方法 (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.Create method (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create(System.String,System.UInt32)
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
- Microsoft::Management::Infrastructure::.Serialization::CimMofDeserializer::Create
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: c8f9b30fb0b9b06c2f1aaeb1fcfcaf65fb3606d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027272"
---
# <a name="cimmofdeserializercreate-method-string-uint32"></a><span data-ttu-id="b97cc-103">CimMofDeserializer： Create 方法 (String，UInt32) </span><span class="sxs-lookup"><span data-stu-id="b97cc-103">CimMofDeserializer.Create method (String, UInt32)</span></span>

<span data-ttu-id="b97cc-104">根據指定的格式和旗標，建立並初始化自訂還原序列化。</span><span class="sxs-lookup"><span data-stu-id="b97cc-104">Creates and initializes a custom deserializer, based on the specified format and flags.</span></span>

<span data-ttu-id="b97cc-105">**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b97cc-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="b97cc-106">**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構</span><span class="sxs-lookup"><span data-stu-id="b97cc-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="b97cc-107">語法</span><span class="sxs-lookup"><span data-stu-id="b97cc-107">Syntax</span></span>

``` csharp
public static CimMofDeserializer Create(
    string format,
    uint flags
)
```

``` c++
public:
static CimMofDeserializer^ Create(
    String^ format,
    unsigned int flags
)
```

``` fsharp
static member Create : 
        format:string *
        flags:uint32 -> CimMofDeserializer
```

``` vb
Public Shared Function Create (
    format As String,
    flags As UInteger
) As CimMofDeserializer
```

#### <a name="parameters"></a><span data-ttu-id="b97cc-108">參數</span><span class="sxs-lookup"><span data-stu-id="b97cc-108">Parameters</span></span>

  - <span data-ttu-id="b97cc-109">format</span><span class="sxs-lookup"><span data-stu-id="b97cc-109">format</span></span>  
    <span data-ttu-id="b97cc-110">類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="b97cc-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="b97cc-111">序列化格式。</span><span class="sxs-lookup"><span data-stu-id="b97cc-111">The serialization format.</span></span> <span data-ttu-id="b97cc-112">僅支援 "MI_XML"。</span><span class="sxs-lookup"><span data-stu-id="b97cc-112">Only "MI_XML" is supported.</span></span>

<!-- end list -->

  - <span data-ttu-id="b97cc-113">flags</span><span class="sxs-lookup"><span data-stu-id="b97cc-113">flags</span></span>  
    <span data-ttu-id="b97cc-114">類型： [system.object](/dotnet/api/system.uint32?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="b97cc-114">Type: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="b97cc-115">序列化旗標。</span><span class="sxs-lookup"><span data-stu-id="b97cc-115">The serialization flags.</span></span> <span data-ttu-id="b97cc-116">必須是 0。</span><span class="sxs-lookup"><span data-stu-id="b97cc-116">Must be 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b97cc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b97cc-117">Return value</span></span>

<span data-ttu-id="b97cc-118">型別： [CimMofDeserializer。](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)</span><span class="sxs-lookup"><span data-stu-id="b97cc-118">Type: [Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)</span></span>

<span data-ttu-id="b97cc-119">新建立的還原序列化物件。</span><span class="sxs-lookup"><span data-stu-id="b97cc-119">The newly created deserializer object.</span></span>

## <a name="see-also"></a><span data-ttu-id="b97cc-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b97cc-120">See also</span></span>

<span data-ttu-id="b97cc-121">[CimMofDeserializer 類別](microsoft.management.infrastructure.serialization.cimmofdeserializer.md) 
。[序列化命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b97cc-121">[CimMofDeserializer class](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)
[Microsoft.Management.Infrastructure.Serialization namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
