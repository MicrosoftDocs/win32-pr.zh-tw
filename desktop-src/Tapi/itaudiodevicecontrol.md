---
description: ITAudioDeviceControl 介面會公開方法，讓應用程式取得並設定參數來控制音訊裝置。
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: 'ITAudioDeviceControl 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001618"
---
# <a name="itaudiodevicecontrol-interface"></a><span data-ttu-id="b771d-103">ITAudioDeviceControl 介面</span><span class="sxs-lookup"><span data-stu-id="b771d-103">ITAudioDeviceControl interface</span></span>

<span data-ttu-id="b771d-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。</span><span class="sxs-lookup"><span data-stu-id="b771d-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b771d-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b771d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b771d-106">**ITAudioDeviceControl** 介面會公開方法，讓應用程式取得並設定參數來控制音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="b771d-106">The **ITAudioDeviceControl** interface exposes methods that enable an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="b771d-107">此介面是由 [IPCONF msp](ipconf-msp.md) 和 [H323 msp](h323-msp.md)所執行。</span><span class="sxs-lookup"><span data-stu-id="b771d-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="b771d-108">當呼叫使用這些服務提供者或協力廠商服務提供者來執行此介面時，就會公開此服務提供者。</span><span class="sxs-lookup"><span data-stu-id="b771d-108">It is exposed when a call uses these service providers or a third party service provider that implements this interface.</span></span> <span data-ttu-id="b771d-109">若要取得 **ITAudioDeviceControl** 介面的指標，請在 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)介面上呼叫 **QueryInterface** ，以控制對應至資料流程的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="b771d-109">To obtain a pointer to the **ITAudioDeviceControl** interface, call **QueryInterface** on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface that controls the audio device corresponding to the stream.</span></span> <span data-ttu-id="b771d-110">**ITStream** 介面的媒體類型必須是音訊，才能公開 **ITAudioDeviceControl** 介面。</span><span class="sxs-lookup"><span data-stu-id="b771d-110">The media type of the **ITStream** interface must be audio for the **ITAudioDeviceControl** interface to be exposed.</span></span>

## <a name="members"></a><span data-ttu-id="b771d-111">成員</span><span class="sxs-lookup"><span data-stu-id="b771d-111">Members</span></span>

<span data-ttu-id="b771d-112">**ITAudioDeviceControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b771d-112">The **ITAudioDeviceControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b771d-113">**ITAudioDeviceControl** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b771d-113">**ITAudioDeviceControl** also has these types of members:</span></span>

-   [<span data-ttu-id="b771d-114">方法</span><span class="sxs-lookup"><span data-stu-id="b771d-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b771d-115">方法</span><span class="sxs-lookup"><span data-stu-id="b771d-115">Methods</span></span>

<span data-ttu-id="b771d-116">**ITAudioDeviceControl** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b771d-116">The **ITAudioDeviceControl** interface has these methods.</span></span>



| <span data-ttu-id="b771d-117">方法</span><span class="sxs-lookup"><span data-stu-id="b771d-117">Method</span></span>                                              | <span data-ttu-id="b771d-118">描述</span><span class="sxs-lookup"><span data-stu-id="b771d-118">Description</span></span>                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b771d-119">**獲取**</span><span class="sxs-lookup"><span data-stu-id="b771d-119">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="b771d-120">取得指定 [音訊裝置屬性](audiodeviceproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="b771d-120">Gets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="b771d-121">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="b771d-121">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="b771d-122">取得指定 [音訊裝置屬性](audiodeviceproperty.md)的有效值範圍。</span><span class="sxs-lookup"><span data-stu-id="b771d-122">Gets the range of valid values for a given [audio device property](audiodeviceproperty.md).</span></span><br/> |
| [<span data-ttu-id="b771d-123">**設定**</span><span class="sxs-lookup"><span data-stu-id="b771d-123">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="b771d-124">設定指定 [音訊裝置屬性](audiodeviceproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="b771d-124">Sets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="b771d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b771d-125">Requirements</span></span>



| <span data-ttu-id="b771d-126">需求</span><span class="sxs-lookup"><span data-stu-id="b771d-126">Requirement</span></span> | <span data-ttu-id="b771d-127">值</span><span class="sxs-lookup"><span data-stu-id="b771d-127">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b771d-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="b771d-128">TAPI version</span></span><br/> | <span data-ttu-id="b771d-129">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="b771d-129">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="b771d-130">標頭</span><span class="sxs-lookup"><span data-stu-id="b771d-130">Header</span></span><br/>       | <dl> <span data-ttu-id="b771d-131"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b771d-131"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b771d-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="b771d-132">Library</span></span><br/>      | <dl> <span data-ttu-id="b771d-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="b771d-133"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="b771d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b771d-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="b771d-135"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b771d-135"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b771d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b771d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b771d-137">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="b771d-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

