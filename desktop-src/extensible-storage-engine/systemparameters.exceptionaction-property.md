---
description: 深入瞭解： SystemParameters. ExceptionAction 屬性
title: SystemParameters. ExceptionAction 屬性
TOCTitle: 'ExceptionAction property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.ExceptionAction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.exceptionaction(v=EXCHG.10)
ms:contentKeyID: 55104042
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.ExceptionAction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.ExceptionAction
- Microsoft.Isam.Esent.Interop.SystemParameters.get_ExceptionAction
- Microsoft.Isam.Esent.Interop.SystemParameters.set_ExceptionAction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 900a29f9304f869712cd72fd51926fd15a030dca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981888"
---
# <a name="systemparametersexceptionaction-property"></a><span data-ttu-id="bbd39-103">SystemParameters. ExceptionAction 屬性</span><span class="sxs-lookup"><span data-stu-id="bbd39-103">SystemParameters.ExceptionAction property</span></span>

<span data-ttu-id="bbd39-104">取得或設定在 JET 內產生之例外狀況的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="bbd39-104">Gets or sets the value encoding what to do with exceptions generated within JET.</span></span>

<span data-ttu-id="bbd39-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bbd39-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bbd39-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bbd39-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd39-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbd39-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Property ExceptionAction As JET_ExceptionAction
    Get
    Set
'Usage
Dim value As JET_ExceptionAction

value = SystemParameters.ExceptionAction

SystemParameters.ExceptionAction = value
```

``` csharp
public static JET_ExceptionAction ExceptionAction { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="bbd39-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="bbd39-108">Property value</span></span>

<span data-ttu-id="bbd39-109">類型： [Microsoft.Isam.Esent.Interop.JET_ExceptionAction](./jet-exceptionaction-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bbd39-109">Type: [Microsoft.Isam.Esent.Interop.JET_ExceptionAction](./jet-exceptionaction-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="bbd39-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbd39-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bbd39-111">參考</span><span class="sxs-lookup"><span data-stu-id="bbd39-111">Reference</span></span>

[<span data-ttu-id="bbd39-112">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="bbd39-112">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="bbd39-113">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="bbd39-113">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="bbd39-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bbd39-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
