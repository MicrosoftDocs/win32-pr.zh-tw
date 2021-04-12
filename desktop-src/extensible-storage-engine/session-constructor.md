---
description: 深入瞭解：會話的函式
title: 會話的函式
TOCTitle: 'Session constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.session(v=EXCHG.10)
ms:contentKeyID: 55107728
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Session
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73d19d5ae1ba422969cd5b11f5b59ceb2811a89d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193029"
---
# <a name="session-constructor"></a><span data-ttu-id="25786-103">會話的函式</span><span class="sxs-lookup"><span data-stu-id="25786-103">Session constructor</span></span>

<span data-ttu-id="25786-104">初始化 Session 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="25786-104">Initializes a new instance of the Session class.</span></span> <span data-ttu-id="25786-105">從指定的實例配置新的 JET_SESSION。</span><span class="sxs-lookup"><span data-stu-id="25786-105">A new JET_SESSION is allocated from the given instance.</span></span>

<span data-ttu-id="25786-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25786-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25786-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="25786-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25786-108">語法</span><span class="sxs-lookup"><span data-stu-id="25786-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCE

Dim instance As New Session(instance)
```

``` csharp
public Session(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="25786-109">參數</span><span class="sxs-lookup"><span data-stu-id="25786-109">Parameters</span></span>

  - <span data-ttu-id="25786-110">instance</span><span class="sxs-lookup"><span data-stu-id="25786-110">instance</span></span>  
    <span data-ttu-id="25786-111">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25786-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="25786-112">要在其中啟動會話的實例。</span><span class="sxs-lookup"><span data-stu-id="25786-112">The instance to start the session in.</span></span>

## <a name="see-also"></a><span data-ttu-id="25786-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25786-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25786-114">參考</span><span class="sxs-lookup"><span data-stu-id="25786-114">Reference</span></span>

[<span data-ttu-id="25786-115">工作階段類別</span><span class="sxs-lookup"><span data-stu-id="25786-115">Session class</span></span>](./session-class.md)

[<span data-ttu-id="25786-116">會話成員</span><span class="sxs-lookup"><span data-stu-id="25786-116">Session members</span></span>](./session-members.md)

[<span data-ttu-id="25786-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="25786-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
