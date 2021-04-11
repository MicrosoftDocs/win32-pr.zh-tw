---
description: 深入瞭解： JetInit 方法
title: JetInit 方法
TOCTitle: 'JetInit method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit(Microsoft.Isam.Esent.Interop.JET_INSTANCE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit(v=EXCHG.10)
ms:contentKeyID: 55100760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27b0ad5fa640b853b46cd39ae595a1f486812adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852623"
---
# <a name="apijetinit-method"></a><span data-ttu-id="5ebda-103">JetInit 方法</span><span class="sxs-lookup"><span data-stu-id="5ebda-103">Api.JetInit method</span></span>

<span data-ttu-id="5ebda-104">初始化 ESENT 資料庫引擎。</span><span class="sxs-lookup"><span data-stu-id="5ebda-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="5ebda-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5ebda-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5ebda-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5ebda-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebda-107">語法</span><span class="sxs-lookup"><span data-stu-id="5ebda-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetInit ( _
    ByRef instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetInit(instance)
```

``` csharp
public static void JetInit(
    ref JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="5ebda-108">參數</span><span class="sxs-lookup"><span data-stu-id="5ebda-108">Parameters</span></span>

  - <span data-ttu-id="5ebda-109">instance</span><span class="sxs-lookup"><span data-stu-id="5ebda-109">instance</span></span>  
    <span data-ttu-id="5ebda-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5ebda-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="5ebda-111">要初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="5ebda-111">The instance to initialize.</span></span> <span data-ttu-id="5ebda-112">如果未配置實例，則會建立新的實例，而引擎會在單一實例模式下運作。</span><span class="sxs-lookup"><span data-stu-id="5ebda-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ebda-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ebda-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5ebda-114">參考</span><span class="sxs-lookup"><span data-stu-id="5ebda-114">Reference</span></span>

[<span data-ttu-id="5ebda-115">Api 類別</span><span class="sxs-lookup"><span data-stu-id="5ebda-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5ebda-116">Api 成員</span><span class="sxs-lookup"><span data-stu-id="5ebda-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5ebda-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5ebda-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
