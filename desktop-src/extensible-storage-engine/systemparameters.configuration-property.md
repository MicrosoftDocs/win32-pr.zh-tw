---
description: 深入瞭解： SystemParameters.Configuration 屬性
title: SystemParameters.Configuration 屬性
TOCTitle: 'Configuration property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.configuration(v=EXCHG.10)
ms:contentKeyID: 55104117
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.set_Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.get_Configuration
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5eaa387f63df1dd91641ff38f2a6f6450629fe99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849533"
---
# <a name="systemparametersconfiguration-property"></a><span data-ttu-id="7ffaa-103">SystemParameters.Configuration 屬性</span><span class="sxs-lookup"><span data-stu-id="7ffaa-103">SystemParameters.Configuration property</span></span>

<span data-ttu-id="7ffaa-104">取得或設定值，這個值會指定整個系統參數集的預設值。</span><span class="sxs-lookup"><span data-stu-id="7ffaa-104">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="7ffaa-105">當此參數設定為特定設定時，所有系統參數值都會重設為該設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="7ffaa-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="7ffaa-106">如果設定特定實例的設定，則全域系統參數將不會重設為其預設值。</span><span class="sxs-lookup"><span data-stu-id="7ffaa-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="7ffaa-107">Small Configuration (0) ：資料庫引擎已針對記憶體使用量優化。</span><span class="sxs-lookup"><span data-stu-id="7ffaa-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="7ffaa-108">舊版設定 (1) ：資料庫引擎有其傳統預設值。</span><span class="sxs-lookup"><span data-stu-id="7ffaa-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="7ffaa-109">Windows Vista 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="7ffaa-109">Supported on Windows Vista and up.</span></span> <span data-ttu-id="7ffaa-110">在 Windows XP 和 Windows Server 2003 上略過。</span><span class="sxs-lookup"><span data-stu-id="7ffaa-110">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="7ffaa-111">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7ffaa-112">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7ffaa-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffaa-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ffaa-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property Configuration As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.Configuration

SystemParameters.Configuration = value
```

``` csharp
public static int Configuration { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="7ffaa-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="7ffaa-114">Property value</span></span>

<span data-ttu-id="7ffaa-115">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7ffaa-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7ffaa-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ffaa-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7ffaa-117">參考</span><span class="sxs-lookup"><span data-stu-id="7ffaa-117">Reference</span></span>

[<span data-ttu-id="7ffaa-118">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="7ffaa-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="7ffaa-119">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="7ffaa-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="7ffaa-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7ffaa-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
