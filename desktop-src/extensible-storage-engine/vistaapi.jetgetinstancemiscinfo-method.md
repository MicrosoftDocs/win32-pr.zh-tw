---
description: 深入瞭解： VistaApi. JetGetInstanceMiscInfo 方法
title: 'VistaApi. JetGetInstanceMiscInfo 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetGetInstanceMiscInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE@,Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetinstancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 55104187
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 204beee343a717d5b45d8003e123bbbe186437d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848578"
---
# <a name="vistaapijetgetinstancemiscinfo-method"></a><span data-ttu-id="5efad-103">VistaApi. JetGetInstanceMiscInfo 方法</span><span class="sxs-lookup"><span data-stu-id="5efad-103">VistaApi.JetGetInstanceMiscInfo method</span></span>

<span data-ttu-id="5efad-104">抓取實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5efad-104">Retrieves information about an instance.</span></span>

<span data-ttu-id="5efad-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="5efad-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="5efad-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5efad-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5efad-107">語法</span><span class="sxs-lookup"><span data-stu-id="5efad-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceMiscInfo ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef signature As JET_SIGNATURE, _
    infoLevel As JET_InstanceMiscInfo _
)
'Usage
Dim instance As JET_INSTANCE
Dim signature As JET_SIGNATURE
Dim infoLevel As JET_InstanceMiscInfoVistaApi.JetGetInstanceMiscInfo(instance, _
    signature, infoLevel)
```

``` csharp
public static void JetGetInstanceMiscInfo(
    JET_INSTANCE instance,
    out JET_SIGNATURE signature,
    JET_InstanceMiscInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="5efad-108">參數</span><span class="sxs-lookup"><span data-stu-id="5efad-108">Parameters</span></span>

  - <span data-ttu-id="5efad-109">instance</span><span class="sxs-lookup"><span data-stu-id="5efad-109">instance</span></span>  
    <span data-ttu-id="5efad-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5efad-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="5efad-111">要取得相關資訊的實例。</span><span class="sxs-lookup"><span data-stu-id="5efad-111">The instance to get information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="5efad-112">簽章</span><span class="sxs-lookup"><span data-stu-id="5efad-112">signature</span></span>  
    <span data-ttu-id="5efad-113">類型： [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="5efad-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="5efad-114">取出的資訊。</span><span class="sxs-lookup"><span data-stu-id="5efad-114">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="5efad-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="5efad-115">infoLevel</span></span>  
    <span data-ttu-id="5efad-116">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5efad-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="5efad-117">要取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="5efad-117">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="5efad-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5efad-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5efad-119">參考</span><span class="sxs-lookup"><span data-stu-id="5efad-119">Reference</span></span>

[<span data-ttu-id="5efad-120">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="5efad-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="5efad-121">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="5efad-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="5efad-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="5efad-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
