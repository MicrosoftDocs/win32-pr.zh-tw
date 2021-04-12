---
description: 深入瞭解： SystemParameters. EnableFileCache 屬性
title: SystemParameters. EnableFileCache 屬性
TOCTitle: 'EnableFileCache property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableFileCache
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enablefilecache(v=EXCHG.10)
ms:contentKeyID: 55104039
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableFileCache
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableFileCache
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableFileCache
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableFileCache
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a0714931860cf8dcce767995f9766bb5440743e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193023"
---
# <a name="systemparametersenablefilecache-property"></a><span data-ttu-id="9dd87-103">SystemParameters. EnableFileCache 屬性</span><span class="sxs-lookup"><span data-stu-id="9dd87-103">SystemParameters.EnableFileCache property</span></span>

<span data-ttu-id="9dd87-104">取得或設定值，這個值表示資料庫引擎是否應使用所有 managed 檔案的 OS 檔案快取。</span><span class="sxs-lookup"><span data-stu-id="9dd87-104">Gets or sets a value indicating whether the database engine should use the OS file cache for all managed files.</span></span>

<span data-ttu-id="9dd87-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9dd87-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9dd87-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9dd87-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd87-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dd87-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EnableFileCache As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableFileCache

SystemParameters.EnableFileCache = value
```

``` csharp
public static bool EnableFileCache { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="9dd87-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="9dd87-108">Property value</span></span>

<span data-ttu-id="9dd87-109">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="9dd87-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9dd87-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dd87-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9dd87-111">參考</span><span class="sxs-lookup"><span data-stu-id="9dd87-111">Reference</span></span>

[<span data-ttu-id="9dd87-112">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="9dd87-112">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="9dd87-113">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="9dd87-113">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="9dd87-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9dd87-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
