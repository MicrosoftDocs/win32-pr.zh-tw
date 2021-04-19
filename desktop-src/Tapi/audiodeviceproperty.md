---
description: ITAudioDeviceControl：： GetRange、ITAudioDeviceControl：： Get 和 ITAudioDeviceControl：： Set 方法會使用 AudioDeviceProperty 列舉來指出要處理的屬性。
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: 'AudioDeviceProperty 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979437"
---
# <a name="audiodeviceproperty-enumeration"></a><span data-ttu-id="d0f01-103">AudioDeviceProperty 列舉</span><span class="sxs-lookup"><span data-stu-id="d0f01-103">AudioDeviceProperty enumeration</span></span>

<span data-ttu-id="d0f01-104">\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d0f01-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d0f01-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d0f01-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d0f01-106">[**ITAudioDeviceControl：： GetRange**](itaudiodevicecontrol-getrange.md)、 [**ITAudioDeviceControl：： Get**](itaudiodevicecontrol-get.md)和 [**ITAudioDeviceControl：： Set**](itaudiodevicecontrol-set.md)方法會使用 **AudioDeviceProperty** 列舉來指出要處理的屬性。</span><span class="sxs-lookup"><span data-stu-id="d0f01-106">The **AudioDeviceProperty** enum is used by the [**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md), and [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) methods to indicate the property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f01-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0f01-107">Syntax</span></span>


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a><span data-ttu-id="d0f01-108">常數</span><span class="sxs-lookup"><span data-stu-id="d0f01-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d0f01-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ DuplexMode**</span><span class="sxs-lookup"><span data-stu-id="d0f01-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice\_DuplexMode**</span></span>
</dt> <dd>

<span data-ttu-id="d0f01-110">指出正在設定或抓取裝置的雙工模式。</span><span class="sxs-lookup"><span data-stu-id="d0f01-110">Indicates that the duplex mode of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="d0f01-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**</span><span class="sxs-lookup"><span data-stu-id="d0f01-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice\_AutomaticGainControl**</span></span>
</dt> <dd>

<span data-ttu-id="d0f01-112">指出正在設定或抓取裝置的自動增益控制。</span><span class="sxs-lookup"><span data-stu-id="d0f01-112">Indicates that the automatic gain control of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="d0f01-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**</span><span class="sxs-lookup"><span data-stu-id="d0f01-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice\_AcousticEchoCancellation**</span></span>
</dt> <dd>

<span data-ttu-id="d0f01-114">指出正在設定或抓取裝置的聲場回顯取消屬性。</span><span class="sxs-lookup"><span data-stu-id="d0f01-114">Indicates that the acoustic echo cancellation properties of the device are being set or retrieved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0f01-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0f01-115">Requirements</span></span>



| <span data-ttu-id="d0f01-116">需求</span><span class="sxs-lookup"><span data-stu-id="d0f01-116">Requirement</span></span> | <span data-ttu-id="d0f01-117">值</span><span class="sxs-lookup"><span data-stu-id="d0f01-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f01-118">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d0f01-118">TAPI version</span></span><br/> | <span data-ttu-id="d0f01-119">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="d0f01-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="d0f01-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d0f01-120">Header</span></span><br/>       | <dl> <span data-ttu-id="d0f01-121"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0f01-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0f01-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0f01-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f01-123">**ITAudioDeviceControl：： GetRange**</span><span class="sxs-lookup"><span data-stu-id="d0f01-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="d0f01-124">**ITAudioDeviceControl：： Get**</span><span class="sxs-lookup"><span data-stu-id="d0f01-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="d0f01-125">**ITAudioDeviceControl：： Set**</span><span class="sxs-lookup"><span data-stu-id="d0f01-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




