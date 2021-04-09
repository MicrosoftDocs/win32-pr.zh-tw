---
description: 深入瞭解： VistaParam.Configuration 欄位
title: 'VistaParam.Configuration 欄位 (的 Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689524"
---
# <a name="vistaparamconfiguration-field"></a><span data-ttu-id="1162a-103">VistaParam.Configuration 欄位</span><span class="sxs-lookup"><span data-stu-id="1162a-103">VistaParam.Configuration field</span></span>

<span data-ttu-id="1162a-104">此參數會針對整組系統參數公開多組預設值。</span><span class="sxs-lookup"><span data-stu-id="1162a-104">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="1162a-105">當此參數設定為特定設定時，所有系統參數值都會重設為該設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="1162a-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="1162a-106">如果設定特定實例的設定，則全域系統參數將不會重設為其預設值。</span><span class="sxs-lookup"><span data-stu-id="1162a-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="1162a-107">Small Configuration (0) ：資料庫引擎已針對記憶體使用量優化。</span><span class="sxs-lookup"><span data-stu-id="1162a-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="1162a-108">舊版設定 (1) ：資料庫引擎有其傳統預設值。</span><span class="sxs-lookup"><span data-stu-id="1162a-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="1162a-109">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="1162a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="1162a-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1162a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1162a-111">語法</span><span class="sxs-lookup"><span data-stu-id="1162a-111">Syntax</span></span>

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a><span data-ttu-id="1162a-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1162a-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1162a-113">參考</span><span class="sxs-lookup"><span data-stu-id="1162a-113">Reference</span></span>

[<span data-ttu-id="1162a-114">VistaParam 類別</span><span class="sxs-lookup"><span data-stu-id="1162a-114">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="1162a-115">VistaParam 成員</span><span class="sxs-lookup"><span data-stu-id="1162a-115">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="1162a-116">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="1162a-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
