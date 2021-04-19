---
description: 深入瞭解： SystemParameters. EnableAdvanced 屬性
title: SystemParameters. EnableAdvanced 屬性
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e311685bf5ef436be11d4593523aceee73b955b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987767"
---
# <a name="systemparametersenableadvanced-property"></a><span data-ttu-id="b9931-103">SystemParameters. EnableAdvanced 屬性</span><span class="sxs-lookup"><span data-stu-id="b9931-103">SystemParameters.EnableAdvanced property</span></span>

<span data-ttu-id="b9931-104">取得或設定值，這個值表示資料庫引擎是否接受或拒絕系統參數子集的變更。</span><span class="sxs-lookup"><span data-stu-id="b9931-104">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="b9931-105">此參數會搭配 [設定使用，以防止](./systemparameters.configuration-property.md) 某些系統參數從選取的設定的預設值中退出。</span><span class="sxs-lookup"><span data-stu-id="b9931-105">This parameter is used in conjunction with [Configuration](./systemparameters.configuration-property.md) to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="b9931-106">Windows Vista 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="b9931-106">Supported on Windows Vista and up.</span></span> <span data-ttu-id="b9931-107">在 Windows XP 和 Windows Server 2003 上略過。</span><span class="sxs-lookup"><span data-stu-id="b9931-107">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="b9931-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9931-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b9931-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b9931-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9931-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9931-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b9931-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="b9931-111">Property value</span></span>

<span data-ttu-id="b9931-112">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b9931-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9931-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9931-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9931-114">參考</span><span class="sxs-lookup"><span data-stu-id="b9931-114">Reference</span></span>

[<span data-ttu-id="b9931-115">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="b9931-115">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="b9931-116">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="b9931-116">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="b9931-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b9931-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
