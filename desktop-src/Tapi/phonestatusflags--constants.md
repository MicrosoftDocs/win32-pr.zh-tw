---
description: PHONESTATUSFLAGS \_ 位旗標常數描述各種電話裝置狀態資訊。
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: 'PHONESTATUSFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999331"
---
# <a name="phonestatusflags_-constants"></a><span data-ttu-id="080b1-103">PHONESTATUSFLAGS \_ 常數</span><span class="sxs-lookup"><span data-stu-id="080b1-103">PHONESTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="080b1-104">**PHONESTATUSFLAGS \_** 位旗標常數描述各種電話裝置狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="080b1-104">The **PHONESTATUSFLAGS\_** bit-flag constants describe a variety of phone device status information.</span></span>

<dl> <dt>

<span data-ttu-id="080b1-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ 已連線**</span><span class="sxs-lookup"><span data-stu-id="080b1-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="080b1-106">指定電話目前是否已連接到 TAPI。</span><span class="sxs-lookup"><span data-stu-id="080b1-106">Specifies whether the phone is currently connected to TAPI.</span></span> <span data-ttu-id="080b1-107">如果已連接 **則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="080b1-107">**TRUE** if connected, **FALSE** otherwise.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="080b1-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS 已 \_ 暫止**</span><span class="sxs-lookup"><span data-stu-id="080b1-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="080b1-109">指定是否暫停 TAPI 的電話裝置操作。</span><span class="sxs-lookup"><span data-stu-id="080b1-109">Specifies whether TAPI's manipulation of the phone device is suspended.</span></span> <span data-ttu-id="080b1-110">如果已暫止，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="080b1-110">**TRUE** if suspended, **FALSE** otherwise.</span></span> <span data-ttu-id="080b1-111">當交換器想要以無法容忍應用程式干擾的方式來操作電話時，可以暫時暫停應用程式使用的電話裝置。</span><span class="sxs-lookup"><span data-stu-id="080b1-111">An application's use of a phone device can be temporarily suspended when the switch wants to manipulate the phone in a way that cannot tolerate interference from the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="080b1-112">備註</span><span class="sxs-lookup"><span data-stu-id="080b1-112">Remarks</span></span>

<span data-ttu-id="080b1-113">無延伸。</span><span class="sxs-lookup"><span data-stu-id="080b1-113">No extensibility.</span></span> <span data-ttu-id="080b1-114">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="080b1-114">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="080b1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="080b1-115">Requirements</span></span>



| <span data-ttu-id="080b1-116">需求</span><span class="sxs-lookup"><span data-stu-id="080b1-116">Requirement</span></span> | <span data-ttu-id="080b1-117">值</span><span class="sxs-lookup"><span data-stu-id="080b1-117">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="080b1-118">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="080b1-118">TAPI version</span></span><br/> | <span data-ttu-id="080b1-119">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="080b1-119">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="080b1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="080b1-120">Header</span></span><br/>       | <dl> <span data-ttu-id="080b1-121"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="080b1-121"><dt>Tapi.h</dt></span></span> </dl> |



 

 




