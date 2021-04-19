---
title: ConnectionStatus 列舉
description: 表示網路中的裝置在上一次看到的狀態。
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- ConnectionStatus 列舉媒體串流 API
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985765"
---
# <a name="connectionstatus-enumeration"></a><span data-ttu-id="99e21-104">ConnectionStatus 列舉</span><span class="sxs-lookup"><span data-stu-id="99e21-104">ConnectionStatus enumeration</span></span>

<span data-ttu-id="99e21-105">表示網路中的裝置在上一次看到的狀態。</span><span class="sxs-lookup"><span data-stu-id="99e21-105">Represents the state of the device in the network as last seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e21-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="99e21-106">Syntax</span></span>


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a><span data-ttu-id="99e21-107">常數</span><span class="sxs-lookup"><span data-stu-id="99e21-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="99e21-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**線上**</span><span class="sxs-lookup"><span data-stu-id="99e21-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**</span></span>
</dt> <dd>

<span data-ttu-id="99e21-109">裝置處於線上狀態且在網路上作用中。</span><span class="sxs-lookup"><span data-stu-id="99e21-109">Device is online and active on the network.</span></span>

</dd> <dt>

<span data-ttu-id="99e21-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線**</span><span class="sxs-lookup"><span data-stu-id="99e21-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**</span></span>
</dt> <dd>

<span data-ttu-id="99e21-111">裝置已離線。</span><span class="sxs-lookup"><span data-stu-id="99e21-111">Device is offline.</span></span>

</dd> <dt>

<span data-ttu-id="99e21-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**睡覺**</span><span class="sxs-lookup"><span data-stu-id="99e21-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Sleeping**</span></span>
</dt> <dd>

<span data-ttu-id="99e21-113">裝置目前為離線狀態，但可能會在嘗試與其進行通訊時自動喚醒。</span><span class="sxs-lookup"><span data-stu-id="99e21-113">Device is currently offline but might automatically wake up when an attempt is made to communicate with it.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99e21-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="99e21-114">Requirements</span></span>



| <span data-ttu-id="99e21-115">需求</span><span class="sxs-lookup"><span data-stu-id="99e21-115">Requirement</span></span> | <span data-ttu-id="99e21-116">值</span><span class="sxs-lookup"><span data-stu-id="99e21-116">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e21-117">Idl</span><span class="sxs-lookup"><span data-stu-id="99e21-117">IDL</span></span><br/> | <dl> <span data-ttu-id="99e21-118"><dt> (參考) 的 windows...。 </dt></span><span class="sxs-lookup"><span data-stu-id="99e21-118"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





