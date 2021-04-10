---
description: 深入瞭解： MofDeserializerSchemaValidationOption 列舉
title: MofDeserializerSchemaValidationOption 列舉 (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: MofDeserializerSchemaValidationOption enumeration (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption
ms.date: 11/14/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Default
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Strict
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Loose
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.IgnorePropertyType
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Ignore
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Default
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Strict
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Loose
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::IgnorePropertyType
- Microsoft::Management::Infrastructure::Serialization::MofDeserializerSchemaValidationOption::Ignore
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Default
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Strict
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Loose
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.IgnorePropertyType
- Microsoft.Management.Infrastructure.Serialization.MofDeserializerSchemaValidationOption.Ignore
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: efb6c5a694d09bcb59fedf3f186498c940a95c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114280"
---
# <a name="mofdeserializerschemavalidationoption-enumeration"></a><span data-ttu-id="3aa82-103">MofDeserializerSchemaValidationOption 列舉</span><span class="sxs-lookup"><span data-stu-id="3aa82-103">MofDeserializerSchemaValidationOption enumeration</span></span>

<span data-ttu-id="3aa82-104">定義常數，指定還原序列化的架構驗證選項。</span><span class="sxs-lookup"><span data-stu-id="3aa82-104">Defines constants that specify schema validation options for deserialization.</span></span>

<span data-ttu-id="3aa82-105">**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3aa82-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="3aa82-106">**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構</span><span class="sxs-lookup"><span data-stu-id="3aa82-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="3aa82-107">語法</span><span class="sxs-lookup"><span data-stu-id="3aa82-107">Syntax</span></span>

``` csharp
internal enum MofDeserializerSchemaValidationOption
```

``` c++
private enum class MofDeserializerSchemaValidationOption
```

``` fsharp
type internal MofDeserializerSchemaValidationOption
```

``` vb
Friend Enumeration MofDeserializerSchemaValidationOption
```

## <a name="members"></a><span data-ttu-id="3aa82-108">成員</span><span class="sxs-lookup"><span data-stu-id="3aa82-108">Members</span></span>

||<span data-ttu-id="3aa82-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="3aa82-109">Member name</span></span>|<span data-ttu-id="3aa82-110">描述</span><span class="sxs-lookup"><span data-stu-id="3aa82-110">Description</span></span>|
|-|-|-|
||<span data-ttu-id="3aa82-111">預設</span><span class="sxs-lookup"><span data-stu-id="3aa82-111">Default</span></span>|<span data-ttu-id="3aa82-112">指定預設架構驗證。</span><span class="sxs-lookup"><span data-stu-id="3aa82-112">Specifies default schema validation.</span></span>|
||<span data-ttu-id="3aa82-113">Strict</span><span class="sxs-lookup"><span data-stu-id="3aa82-113">Strict</span></span>|<span data-ttu-id="3aa82-114">指定嚴格的架構驗證。</span><span class="sxs-lookup"><span data-stu-id="3aa82-114">Specifies strict schema validation.</span></span>|
||<span data-ttu-id="3aa82-115">鬆散</span><span class="sxs-lookup"><span data-stu-id="3aa82-115">Loose</span></span>|<span data-ttu-id="3aa82-116">指定鬆散的架構驗證。</span><span class="sxs-lookup"><span data-stu-id="3aa82-116">Specifies loose schema validation.</span></span>|
||<span data-ttu-id="3aa82-117">IgnorePropertyType</span><span class="sxs-lookup"><span data-stu-id="3aa82-117">IgnorePropertyType</span></span>|<span data-ttu-id="3aa82-118">指定架構驗證應該忽略屬性類型。</span><span class="sxs-lookup"><span data-stu-id="3aa82-118">Specifies that schema validation should ignore property types.</span></span>|
||<span data-ttu-id="3aa82-119">忽略</span><span class="sxs-lookup"><span data-stu-id="3aa82-119">Ignore</span></span>|<span data-ttu-id="3aa82-120">指定應忽略架構驗證。</span><span class="sxs-lookup"><span data-stu-id="3aa82-120">Specifies that schema validation should be ignored.</span></span>|

## <a name="see-also"></a><span data-ttu-id="3aa82-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3aa82-121">See Also</span></span>

<span data-ttu-id="3aa82-122">[。序列化命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3aa82-122">[Microsoft.Management.Infrastructure.Serialization Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
