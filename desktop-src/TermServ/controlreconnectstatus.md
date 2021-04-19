---
title: ControlReconnectStatus 列舉
description: 指定 IMsRdpClient8 Reconnect 方法的結果。
ms.assetid: FB0AC4CF-18F5-4CDD-A75C-59A7CF716688
ms.tgt_platform: multiple
keywords:
- ControlReconnectStatus 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- ControlReconnectStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5638cbdda268dd453881ee1d88085728479aada6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966291"
---
# <a name="controlreconnectstatus-enumeration"></a><span data-ttu-id="f2ef5-104">ControlReconnectStatus 列舉</span><span class="sxs-lookup"><span data-stu-id="f2ef5-104">ControlReconnectStatus enumeration</span></span>

<span data-ttu-id="f2ef5-105">指定 [**IMsRdpClient8：： Reconnect**](imsrdpclient8-reconnect.md) 方法的結果。</span><span class="sxs-lookup"><span data-stu-id="f2ef5-105">Specifies the result of the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ef5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2ef5-106">Syntax</span></span>


```C++
typedef enum  { 
  controlReconnectStarted  = 0x0000,
  controlReconnectBlocked  = 0x0001
} ControlReconnectStatus;
```



## <a name="constants"></a><span data-ttu-id="f2ef5-107">常數</span><span class="sxs-lookup"><span data-stu-id="f2ef5-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f2ef5-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span><span class="sxs-lookup"><span data-stu-id="f2ef5-108"><span id="controlReconnectStarted"></span><span id="controlreconnectstarted"></span><span id="CONTROLRECONNECTSTARTED"></span>**controlReconnectStarted**</span></span>
</dt> <dd>

<span data-ttu-id="f2ef5-109">重新連接作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="f2ef5-109">The reconnect operation was started.</span></span>

</dd> <dt>

<span data-ttu-id="f2ef5-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span><span class="sxs-lookup"><span data-stu-id="f2ef5-110"><span id="controlReconnectBlocked"></span><span id="controlreconnectblocked"></span><span id="CONTROLRECONNECTBLOCKED"></span>**controlReconnectBlocked**</span></span>
</dt> <dd>

<span data-ttu-id="f2ef5-111">無法啟動重新連接操作。</span><span class="sxs-lookup"><span data-stu-id="f2ef5-111">The reconnect operation could not be started.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2ef5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2ef5-112">Requirements</span></span>



| <span data-ttu-id="f2ef5-113">需求</span><span class="sxs-lookup"><span data-stu-id="f2ef5-113">Requirement</span></span> | <span data-ttu-id="f2ef5-114">值</span><span class="sxs-lookup"><span data-stu-id="f2ef5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ef5-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2ef5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ef5-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f2ef5-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="f2ef5-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2ef5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ef5-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2ef5-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="f2ef5-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f2ef5-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2ef5-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2ef5-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ef5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2ef5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ef5-122">**IMsRdpClient8：： Reconnect**</span><span class="sxs-lookup"><span data-stu-id="f2ef5-122">**IMsRdpClient8::Reconnect**</span></span>](imsrdpclient8-reconnect.md)
</dt> </dl>

 

 





