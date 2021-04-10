---
description: 深入瞭解： EsentMustDisableLoggingForDbUpgradeException 類別
title: EsentMustDisableLoggingForDbUpgradeException 類別
TOCTitle: EsentMustDisableLoggingForDbUpgradeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmustdisableloggingfordbupgradeexception(v=EXCHG.10)
ms:contentKeyID: 55102330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c176dfbd9165f28225c4223ea3e47fdc24bb22c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114757"
---
# <a name="esentmustdisableloggingfordbupgradeexception-class"></a><span data-ttu-id="acf21-103">EsentMustDisableLoggingForDbUpgradeException 類別</span><span class="sxs-lookup"><span data-stu-id="acf21-103">EsentMustDisableLoggingForDbUpgradeException class</span></span>

<span data-ttu-id="acf21-104">JET_err 的基類。MustDisableLoggingForDbUpgrade 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="acf21-104">Base class for JET_err.MustDisableLoggingForDbUpgrade exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="acf21-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="acf21-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="acf21-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="acf21-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="acf21-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="acf21-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="acf21-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="acf21-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="acf21-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="acf21-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="acf21-110">EsentApiException （.）</span><span class="sxs-lookup"><span data-stu-id="acf21-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="acf21-111">EsentObsoleteException （.）</span><span class="sxs-lookup"><span data-stu-id="acf21-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="acf21-112">EsentMustDisableLoggingForDbUpgradeException （.）</span><span class="sxs-lookup"><span data-stu-id="acf21-112">Microsoft.Isam.Esent.Interop.EsentMustDisableLoggingForDbUpgradeException</span></span>  

<span data-ttu-id="acf21-113">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="acf21-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="acf21-114">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="acf21-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="acf21-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="acf21-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMustDisableLoggingForDbUpgradeException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentMustDisableLoggingForDbUpgradeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMustDisableLoggingForDbUpgradeException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="acf21-116">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="acf21-116">Thread safety</span></span>

<span data-ttu-id="acf21-117">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="acf21-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="acf21-118">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="acf21-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="acf21-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acf21-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="acf21-120">參考</span><span class="sxs-lookup"><span data-stu-id="acf21-120">Reference</span></span>

[<span data-ttu-id="acf21-121">EsentMustDisableLoggingForDbUpgradeException 成員</span><span class="sxs-lookup"><span data-stu-id="acf21-121">EsentMustDisableLoggingForDbUpgradeException members</span></span>](./esentmustdisableloggingfordbupgradeexception-members.md)

[<span data-ttu-id="acf21-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="acf21-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
