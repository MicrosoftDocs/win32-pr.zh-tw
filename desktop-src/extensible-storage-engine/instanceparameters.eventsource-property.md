---
description: 深入瞭解： InstanceParameters EventSource 屬性
title: InstanceParameters EventSource 屬性
TOCTitle: 'EventSource property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsource(v=EXCHG.10)
ms:contentKeyID: 55103563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSource
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSource
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5cba0c6f9aef4b9e6633a5d0073b1fdbc2c3b1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985046"
---
# <a name="instanceparameterseventsource-property"></a><span data-ttu-id="6bf78-103">InstanceParameters EventSource 屬性</span><span class="sxs-lookup"><span data-stu-id="6bf78-103">InstanceParameters.EventSource property</span></span>

<span data-ttu-id="6bf78-104">取得或設定應用程式特定的字串，這個字串將加入 database engine 所發出的任何事件記錄檔訊息中。</span><span class="sxs-lookup"><span data-stu-id="6bf78-104">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="6bf78-105">這可讓事件記錄檔訊息與來源應用程式輕鬆相互關聯。</span><span class="sxs-lookup"><span data-stu-id="6bf78-105">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="6bf78-106">預設會使用主應用程式的可執行檔名稱。</span><span class="sxs-lookup"><span data-stu-id="6bf78-106">By default the host application executable name will be used.</span></span>

<span data-ttu-id="6bf78-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6bf78-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6bf78-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6bf78-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6bf78-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bf78-109">Syntax</span></span>

``` vb
'Declaration
Public Property EventSource As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSource

instance.EventSource = value
```

``` csharp
public string EventSource { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="6bf78-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6bf78-110">Property value</span></span>

<span data-ttu-id="6bf78-111">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6bf78-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6bf78-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bf78-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6bf78-113">參考</span><span class="sxs-lookup"><span data-stu-id="6bf78-113">Reference</span></span>

[<span data-ttu-id="6bf78-114">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="6bf78-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="6bf78-115">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="6bf78-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="6bf78-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6bf78-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
