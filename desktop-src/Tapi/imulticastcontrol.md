---
description: IMulticastControl 介面是由 IPConf MSP 所執行，而且僅適用于多播呼叫物件。
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: 'IMulticastControl 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993222"
---
# <a name="imulticastcontrol-interface"></a><span data-ttu-id="aae6f-103">IMulticastControl 介面</span><span class="sxs-lookup"><span data-stu-id="aae6f-103">IMulticastControl interface</span></span>

<span data-ttu-id="aae6f-104">\[**IMulticastControl** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="aae6f-104">\[**IMulticastControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aae6f-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="aae6f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="aae6f-106">**IMulticastControl** 介面是由 IPConf MSP 所執行，而且僅適用于多播呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="aae6f-106">The **IMulticastControl** interface is implemented by the IPConf MSP and available only on multicast call objects.</span></span> <span data-ttu-id="aae6f-107">此介面會公開方法，以啟用 H323 和 SDP 用戶端間通訊的終端機建立和操作。</span><span class="sxs-lookup"><span data-stu-id="aae6f-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="aae6f-108">**IMulticastControl** 介面控制多播回送模式。</span><span class="sxs-lookup"><span data-stu-id="aae6f-108">The **IMulticastControl** interface controls the multicast loopback mode.</span></span>

<span data-ttu-id="aae6f-109">在 MM \_ NO \_ 回送模式中，多播回送已停用，這表示同一部電腦上同時加入相同多播群組的兩個應用程式將會取得彼此的封包。</span><span class="sxs-lookup"><span data-stu-id="aae6f-109">In the MM\_NO\_LOOPBACK mode, multicast loopback is disabled, which means two applications on the same machine who join the same multicast group will get each other's packets.</span></span> <span data-ttu-id="aae6f-110">如果一律只有一個應用程式在電腦上加入多播群組，則此模式的效能最佳。</span><span class="sxs-lookup"><span data-stu-id="aae6f-110">This mode has the best performance if there is always only one application joining the multicast group on the machine.</span></span> <span data-ttu-id="aae6f-111">MM \_ 沒有 \_ 預設模式的回送模式。</span><span class="sxs-lookup"><span data-stu-id="aae6f-111">MM\_NO\_LOOPBACK mode is the default mode.</span></span>

<span data-ttu-id="aae6f-112">MM \_ 完整 \_ 回送模式只適用于測試。</span><span class="sxs-lookup"><span data-stu-id="aae6f-112">The MM\_FULL\_LOOPBACK mode is good only for testing.</span></span> <span data-ttu-id="aae6f-113">送出的所有封包也會回復。</span><span class="sxs-lookup"><span data-stu-id="aae6f-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="aae6f-114">這可以用來測試裝置是否正常運作。</span><span class="sxs-lookup"><span data-stu-id="aae6f-114">This can be used to test if the devices are working.</span></span>

<span data-ttu-id="aae6f-115">MM \_ 選擇性 \_ 回送模式可用來讓一部電腦上的多個應用程式加入相同的多播群組。</span><span class="sxs-lookup"><span data-stu-id="aae6f-115">The MM\_SELECTIVE\_LOOPBACK mode is used to enable multiple applications on one machine to join the same multicast group.</span></span> <span data-ttu-id="aae6f-116">封包會從堆疊環回，且每個 RTP 會話都會負責篩選掉不需要的封包。</span><span class="sxs-lookup"><span data-stu-id="aae6f-116">The packets are looped back from the stack, and each RTP session is responsible for filtering out unwanted packets.</span></span>

## <a name="members"></a><span data-ttu-id="aae6f-117">成員</span><span class="sxs-lookup"><span data-stu-id="aae6f-117">Members</span></span>

<span data-ttu-id="aae6f-118">**IMulticastControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="aae6f-118">The **IMulticastControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aae6f-119">**IMulticastControl** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aae6f-119">**IMulticastControl** also has these types of members:</span></span>

-   [<span data-ttu-id="aae6f-120">方法</span><span class="sxs-lookup"><span data-stu-id="aae6f-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aae6f-121">方法</span><span class="sxs-lookup"><span data-stu-id="aae6f-121">Methods</span></span>

<span data-ttu-id="aae6f-122">**IMulticastControl** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="aae6f-122">The **IMulticastControl** interface has these methods.</span></span>



| <span data-ttu-id="aae6f-123">方法</span><span class="sxs-lookup"><span data-stu-id="aae6f-123">Method</span></span>                                                          | <span data-ttu-id="aae6f-124">描述</span><span class="sxs-lookup"><span data-stu-id="aae6f-124">Description</span></span>                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="aae6f-125">**取得 \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="aae6f-125">**get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md) | <span data-ttu-id="aae6f-126">取得多播回送模式。</span><span class="sxs-lookup"><span data-stu-id="aae6f-126">Gets the multicast loopback mode.</span></span><br/> |
| [<span data-ttu-id="aae6f-127">**put \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="aae6f-127">**put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md) | <span data-ttu-id="aae6f-128">設定多播回送模式。</span><span class="sxs-lookup"><span data-stu-id="aae6f-128">Sets the multicast loopback mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aae6f-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="aae6f-129">Requirements</span></span>



| <span data-ttu-id="aae6f-130">需求</span><span class="sxs-lookup"><span data-stu-id="aae6f-130">Requirement</span></span> | <span data-ttu-id="aae6f-131">值</span><span class="sxs-lookup"><span data-stu-id="aae6f-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aae6f-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="aae6f-132">TAPI version</span></span><br/> | <span data-ttu-id="aae6f-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="aae6f-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="aae6f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="aae6f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="aae6f-135"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-135"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="aae6f-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="aae6f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="aae6f-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="aae6f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="aae6f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="aae6f-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-139"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="aae6f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aae6f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae6f-141">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="aae6f-141">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

