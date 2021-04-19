---
description: '深入瞭解： CimMofDeserializer. OnClassNeeded 委派 (字串、字串、字串) '
title: CimMofDeserializer.OnClassNeeded delegate (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.OnClassNeeded delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::OnClassNeeded
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 50e107c09eccde03446278516a1f125f4ad86022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973904"
---
# <a name="cimmofdeserializeronclassneeded-delegate-string-string-string"></a><span data-ttu-id="e31f3-103">CimMofDeserializer。 OnClassNeeded 委派 (字串、字串、字串) </span><span class="sxs-lookup"><span data-stu-id="e31f3-103">CimMofDeserializer.OnClassNeeded delegate (String, String, String)</span></span>

<span data-ttu-id="e31f3-104">表示用來抓取指定伺服器、命名空間和類別名稱之 CIM 類別的回呼。</span><span class="sxs-lookup"><span data-stu-id="e31f3-104">Represents a callback to retrieve a CIM class for the specified server, namespace, and class name.</span></span>

<span data-ttu-id="e31f3-105">**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e31f3-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="e31f3-106">**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構</span><span class="sxs-lookup"><span data-stu-id="e31f3-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="e31f3-107">語法</span><span class="sxs-lookup"><span data-stu-id="e31f3-107">Syntax</span></span>

``` csharp
public delegate CimClass OnClassNeeded(
    string serverName,
    string namespaceName,
    string className
)
```

``` c++
public delegate CimClass^ OnClassNeeded(
    String^ serverName,
    String^ namespaceName,
    String^ className
)
```

``` fsharp
type OnClassNeeded = 
    delegate of 
        serverName:string *
        namespaceName:string *
        className:string -> CimClass
```

``` vb
Public Delegate Function OnClassNeeded (
    serverName As String,
    namespaceName As String,
    className As String,
) As CimClass
```

#### <a name="parameters"></a><span data-ttu-id="e31f3-108">參數</span><span class="sxs-lookup"><span data-stu-id="e31f3-108">Parameters</span></span>

  - <span data-ttu-id="e31f3-109">serverName</span><span class="sxs-lookup"><span data-stu-id="e31f3-109">serverName</span></span>  
    <span data-ttu-id="e31f3-110">類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="e31f3-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="e31f3-111">CIM 類別的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e31f3-111">The name of the server for the CIM class.</span></span>

<!-- end list -->

  - <span data-ttu-id="e31f3-112">namespaceName</span><span class="sxs-lookup"><span data-stu-id="e31f3-112">namespaceName</span></span>  
    <span data-ttu-id="e31f3-113">類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="e31f3-113">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="e31f3-114">CIM 類別的命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="e31f3-114">The name of the namespace for the CIM class.</span></span>

<!-- end list -->

  - <span data-ttu-id="e31f3-115">className</span><span class="sxs-lookup"><span data-stu-id="e31f3-115">className</span></span>  
    <span data-ttu-id="e31f3-116">類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="e31f3-116">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="e31f3-117">CIM 類別的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="e31f3-117">The name of the class for the CIM class.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e31f3-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e31f3-118">Return Value</span></span>

<span data-ttu-id="e31f3-119">Type： [CimClass 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e31f3-119">Type: [CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>

<span data-ttu-id="e31f3-120">傳回對應至指定引數的 CIM 類別，如果找不到類別，則 **為 null** 。</span><span class="sxs-lookup"><span data-stu-id="e31f3-120">Returns the CIM class corresponding to the specified arguments, or **null** if the class can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="e31f3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e31f3-121">See Also</span></span>

<span data-ttu-id="e31f3-122">[管理基礎結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e31f3-122">[Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
