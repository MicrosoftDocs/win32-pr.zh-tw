---
description: 深入瞭解： VistaApi. JetInit3 方法
title: 'VistaApi. JetInit3 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetInit3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetinit3(v=EXCHG.10)
ms:contentKeyID: 55104198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c5fa7d1450240a8250e66e2bbe6d8ef0b97c136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974067"
---
# <a name="vistaapijetinit3-method"></a><span data-ttu-id="54ce3-103">VistaApi. JetInit3 方法</span><span class="sxs-lookup"><span data-stu-id="54ce3-103">VistaApi.JetInit3 method</span></span>

<span data-ttu-id="54ce3-104">初始化 ESENT 資料庫引擎。</span><span class="sxs-lookup"><span data-stu-id="54ce3-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="54ce3-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="54ce3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="54ce3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="54ce3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="54ce3-107">語法</span><span class="sxs-lookup"><span data-stu-id="54ce3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit3 ( _
    ByRef instance As JET_INSTANCE, _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = VistaApi.JetInit3(instance, _
    recoveryOptions, grbit)
```

``` csharp
public static JET_wrn JetInit3(
    ref JET_INSTANCE instance,
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="54ce3-108">參數</span><span class="sxs-lookup"><span data-stu-id="54ce3-108">Parameters</span></span>

  - <span data-ttu-id="54ce3-109">instance</span><span class="sxs-lookup"><span data-stu-id="54ce3-109">instance</span></span>  
    <span data-ttu-id="54ce3-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54ce3-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="54ce3-111">要初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="54ce3-111">The instance to initialize.</span></span> <span data-ttu-id="54ce3-112">如果未配置實例，則會建立新的實例，而引擎會在單一實例模式下運作。</span><span class="sxs-lookup"><span data-stu-id="54ce3-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="54ce3-113">recoveryOptions</span><span class="sxs-lookup"><span data-stu-id="54ce3-113">recoveryOptions</span></span>  
    <span data-ttu-id="54ce3-114">類型： [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="54ce3-114">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="54ce3-115">在復原期間重新對應資料庫的其他修復參數、放置停止復原的位置，或復原狀態。</span><span class="sxs-lookup"><span data-stu-id="54ce3-115">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="54ce3-116">grbit</span><span class="sxs-lookup"><span data-stu-id="54ce3-116">grbit</span></span>  
    <span data-ttu-id="54ce3-117">類型： [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="54ce3-117">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="54ce3-118">初始化選項。</span><span class="sxs-lookup"><span data-stu-id="54ce3-118">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="54ce3-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="54ce3-119">Return value</span></span>

<span data-ttu-id="54ce3-120">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="54ce3-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="54ce3-121">警告碼。</span><span class="sxs-lookup"><span data-stu-id="54ce3-121">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="54ce3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54ce3-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="54ce3-123">參考</span><span class="sxs-lookup"><span data-stu-id="54ce3-123">Reference</span></span>

[<span data-ttu-id="54ce3-124">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="54ce3-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="54ce3-125">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="54ce3-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="54ce3-126">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="54ce3-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
