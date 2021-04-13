---
description: 深入瞭解： SystemParameters. EventLoggingLevel 屬性
title: SystemParameters. EventLoggingLevel 屬性
TOCTitle: 'EventLoggingLevel property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EventLoggingLevel
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.eventlogginglevel(v=EXCHG.10)
ms:contentKeyID: 55104119
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EventLoggingLevel
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EventLoggingLevel
- Microsoft.Isam.Esent.Interop.SystemParameters.EventLoggingLevel
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EventLoggingLevel
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e70ef2c0adff6982a34c8e11cc2140f51229299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321139"
---
# <a name="systemparameterseventlogginglevel-property"></a><span data-ttu-id="99a3f-103">SystemParameters. EventLoggingLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="99a3f-103">SystemParameters.EventLoggingLevel property</span></span>

<span data-ttu-id="99a3f-104">取得或設定資料庫引擎發出至 eventlog 的 eventlog 訊息詳細層級。</span><span class="sxs-lookup"><span data-stu-id="99a3f-104">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="99a3f-105">較高的數位將會產生更詳細的事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="99a3f-105">Higher numbers will result in more detailed eventlog messages.</span></span>

<span data-ttu-id="99a3f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99a3f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99a3f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="99a3f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99a3f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="99a3f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EventLoggingLevel As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.EventLoggingLevel

SystemParameters.EventLoggingLevel = value
```

``` csharp
public static int EventLoggingLevel { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="99a3f-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="99a3f-109">Property value</span></span>

<span data-ttu-id="99a3f-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="99a3f-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="99a3f-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99a3f-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99a3f-112">參考</span><span class="sxs-lookup"><span data-stu-id="99a3f-112">Reference</span></span>

[<span data-ttu-id="99a3f-113">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="99a3f-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="99a3f-114">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="99a3f-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="99a3f-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="99a3f-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
