---
description: 深入瞭解： InstanceParameters. EventSourceKey 屬性
title: InstanceParameters. EventSourceKey 屬性
TOCTitle: 'EventSourceKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsourcekey(v=EXCHG.10)
ms:contentKeyID: 55107449
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSourceKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d1dc80943095611737d0c9704bcc0e82ffee506f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943739"
---
# <a name="instanceparameterseventsourcekey-property"></a><span data-ttu-id="e22b2-103">InstanceParameters. EventSourceKey 屬性</span><span class="sxs-lookup"><span data-stu-id="e22b2-103">InstanceParameters.EventSourceKey property</span></span>

<span data-ttu-id="e22b2-104">取得或設定資料庫引擎為其事件記錄檔訊息所使用的事件記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="e22b2-104">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="e22b2-105">依預設，所有事件記錄檔訊息都會移至應用程式事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="e22b2-105">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="e22b2-106">如果已設定另一個事件記錄檔的登錄機碼名稱，則會改為將事件記錄檔訊息移至該處。</span><span class="sxs-lookup"><span data-stu-id="e22b2-106">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<span data-ttu-id="e22b2-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e22b2-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e22b2-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e22b2-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e22b2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e22b2-109">Syntax</span></span>

``` vb
'Declaration
Public Property EventSourceKey As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSourceKey

instance.EventSourceKey = value
```

``` csharp
public string EventSourceKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e22b2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e22b2-110">Property value</span></span>

<span data-ttu-id="e22b2-111">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e22b2-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e22b2-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e22b2-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e22b2-113">參考</span><span class="sxs-lookup"><span data-stu-id="e22b2-113">Reference</span></span>

[<span data-ttu-id="e22b2-114">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="e22b2-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="e22b2-115">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="e22b2-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="e22b2-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e22b2-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
