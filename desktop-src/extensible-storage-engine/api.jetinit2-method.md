---
description: 深入瞭解： JetInit2 方法
title: JetInit2 方法
TOCTitle: 'JetInit2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit2(v=EXCHG.10)
ms:contentKeyID: 55100762
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 138a9830d5a74b887e7e68f3a3833f5f7e7fb8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985063"
---
# <a name="apijetinit2-method"></a><span data-ttu-id="8e226-103">JetInit2 方法</span><span class="sxs-lookup"><span data-stu-id="8e226-103">Api.JetInit2 method</span></span>

<span data-ttu-id="8e226-104">初始化 ESENT 資料庫引擎。</span><span class="sxs-lookup"><span data-stu-id="8e226-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="8e226-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e226-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8e226-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8e226-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e226-107">語法</span><span class="sxs-lookup"><span data-stu-id="8e226-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit2 ( _
    ByRef instance As JET_INSTANCE, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetInit2(instance, _
    grbit)
```

``` csharp
public static JET_wrn JetInit2(
    ref JET_INSTANCE instance,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8e226-108">參數</span><span class="sxs-lookup"><span data-stu-id="8e226-108">Parameters</span></span>

  - <span data-ttu-id="8e226-109">instance</span><span class="sxs-lookup"><span data-stu-id="8e226-109">instance</span></span>  
    <span data-ttu-id="8e226-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8e226-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="8e226-111">要初始化的實例。</span><span class="sxs-lookup"><span data-stu-id="8e226-111">The instance to initialize.</span></span> <span data-ttu-id="8e226-112">如果未配置實例，則會建立新的實例，而引擎會在單一實例模式下運作。</span><span class="sxs-lookup"><span data-stu-id="8e226-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="8e226-113">grbit</span><span class="sxs-lookup"><span data-stu-id="8e226-113">grbit</span></span>  
    <span data-ttu-id="8e226-114">類型： [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8e226-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8e226-115">初始化選項。</span><span class="sxs-lookup"><span data-stu-id="8e226-115">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8e226-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e226-116">Return value</span></span>

<span data-ttu-id="8e226-117">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8e226-117">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="8e226-118">警告碼。</span><span class="sxs-lookup"><span data-stu-id="8e226-118">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8e226-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e226-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e226-120">參考</span><span class="sxs-lookup"><span data-stu-id="8e226-120">Reference</span></span>

[<span data-ttu-id="8e226-121">Api 類別</span><span class="sxs-lookup"><span data-stu-id="8e226-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8e226-122">Api 成員</span><span class="sxs-lookup"><span data-stu-id="8e226-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8e226-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8e226-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
