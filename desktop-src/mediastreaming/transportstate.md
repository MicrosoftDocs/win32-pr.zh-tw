---
title: TransportState 列舉
description: 定義 UPnP 指導方針所定義的可用傳輸狀態。
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- TransportState 列舉媒體串流 API
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984437"
---
# <a name="transportstate-enumeration"></a><span data-ttu-id="a0299-104">TransportState 列舉</span><span class="sxs-lookup"><span data-stu-id="a0299-104">TransportState enumeration</span></span>

<span data-ttu-id="a0299-105">定義 UPnP 指導方針所定義的可用傳輸狀態。</span><span class="sxs-lookup"><span data-stu-id="a0299-105">Defines the available transport states as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0299-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0299-106">Syntax</span></span>


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a><span data-ttu-id="a0299-107">常數</span><span class="sxs-lookup"><span data-stu-id="a0299-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a0299-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知**</span><span class="sxs-lookup"><span data-stu-id="a0299-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="a0299-109">錯誤的裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="a0299-109">Erroneous device state.</span></span>

</dd> <dt>

<span data-ttu-id="a0299-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**停止**</span><span class="sxs-lookup"><span data-stu-id="a0299-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped**</span></span>
</dt> <dd>

<span data-ttu-id="a0299-111">裝置 s 傳輸處於停止狀態。</span><span class="sxs-lookup"><span data-stu-id="a0299-111">The device s transport is in a stopped state.</span></span>

</dd> <dt>

<span data-ttu-id="a0299-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**玩**</span><span class="sxs-lookup"><span data-stu-id="a0299-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Playing**</span></span>
</dt> <dd>

<span data-ttu-id="a0299-113">裝置的傳輸狀態為「現正播放」。</span><span class="sxs-lookup"><span data-stu-id="a0299-113">The device s transport is in a playing state.</span></span>

</dd> <dt>

<span data-ttu-id="a0299-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**過渡**</span><span class="sxs-lookup"><span data-stu-id="a0299-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning**</span></span>
</dt> <dd>

<span data-ttu-id="a0299-115">裝置的傳輸處於轉換狀態，這會產生另一個狀態值。</span><span class="sxs-lookup"><span data-stu-id="a0299-115">The device s transport is in a transitioning state which will result in another state value.</span></span>

</dd> <dt>

<span data-ttu-id="a0299-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**暫停**</span><span class="sxs-lookup"><span data-stu-id="a0299-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused**</span></span>
</dt> <dd>

<span data-ttu-id="a0299-117">裝置 s 傳輸處於暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="a0299-117">The device s transport is in a paused state.</span></span>

</dd> <dt>

<span data-ttu-id="a0299-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**記錄**</span><span class="sxs-lookup"><span data-stu-id="a0299-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Recording**</span></span>
</dt> <dd>

<span data-ttu-id="a0299-119">裝置 s 傳輸處於錄製狀態。</span><span class="sxs-lookup"><span data-stu-id="a0299-119">The device s transport is in a recording state.</span></span>

</dd> <dt>

<span data-ttu-id="a0299-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span><span class="sxs-lookup"><span data-stu-id="a0299-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span></span>
</dt> <dd>

<span data-ttu-id="a0299-121">裝置的傳輸沒有針對播放設定的 URI。</span><span class="sxs-lookup"><span data-stu-id="a0299-121">The device s transport does not have an URI set for playback.</span></span>

</dd> <dt>

<span data-ttu-id="a0299-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**最後**</span><span class="sxs-lookup"><span data-stu-id="a0299-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="a0299-123">裝置的先前狀態設為目前的傳輸狀態。</span><span class="sxs-lookup"><span data-stu-id="a0299-123">The device s previous state to the current transport state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0299-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0299-124">Requirements</span></span>



| <span data-ttu-id="a0299-125">需求</span><span class="sxs-lookup"><span data-stu-id="a0299-125">Requirement</span></span> | <span data-ttu-id="a0299-126">值</span><span class="sxs-lookup"><span data-stu-id="a0299-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0299-127">Idl</span><span class="sxs-lookup"><span data-stu-id="a0299-127">IDL</span></span><br/> | <dl> <span data-ttu-id="a0299-128"><dt> (參考) 的 windows...。 </dt></span><span class="sxs-lookup"><span data-stu-id="a0299-128"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





