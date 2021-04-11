---
description: 深入瞭解： JetIdle 方法
title: JetIdle 方法
TOCTitle: 'JetIdle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIdle(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.IdleGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetidle(v=EXCHG.10)
ms:contentKeyID: 55100757
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e524a23d5e8fb20b1b6db1fb7e82fbb07bf3df0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945288"
---
# <a name="apijetidle-method"></a><span data-ttu-id="94062-103">JetIdle 方法</span><span class="sxs-lookup"><span data-stu-id="94062-103">Api.JetIdle method</span></span>

<span data-ttu-id="94062-104">執行閒置清除工作或檢查 ESE 中的版本存放區狀態。</span><span class="sxs-lookup"><span data-stu-id="94062-104">Performs idle cleanup tasks or checks the version store status in ESE.</span></span>

<span data-ttu-id="94062-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="94062-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="94062-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="94062-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="94062-107">語法</span><span class="sxs-lookup"><span data-stu-id="94062-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetIdle ( _
    sesid As JET_SESID, _
    grbit As IdleGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim grbit As IdleGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetIdle(sesid, _
    grbit)
```

``` csharp
public static JET_wrn JetIdle(
    JET_SESID sesid,
    IdleGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="94062-108">參數</span><span class="sxs-lookup"><span data-stu-id="94062-108">Parameters</span></span>

  - <span data-ttu-id="94062-109">sesid</span><span class="sxs-lookup"><span data-stu-id="94062-109">sesid</span></span>  
    <span data-ttu-id="94062-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="94062-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="94062-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="94062-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="94062-112">grbit</span><span class="sxs-lookup"><span data-stu-id="94062-112">grbit</span></span>  
    <span data-ttu-id="94062-113">型別： [IdleGrbit](./idlegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="94062-113">Type: [Microsoft.Isam.Esent.Interop.IdleGrbit](./idlegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="94062-114">JetIdleGrbit 旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="94062-114">A combination of JetIdleGrbit flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="94062-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="94062-115">Return value</span></span>

<span data-ttu-id="94062-116">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="94062-116">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="94062-117">如果作業失敗，則為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="94062-117">An error code if the operation fails.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94062-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94062-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="94062-119">參考</span><span class="sxs-lookup"><span data-stu-id="94062-119">Reference</span></span>

[<span data-ttu-id="94062-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="94062-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="94062-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="94062-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="94062-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="94062-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
