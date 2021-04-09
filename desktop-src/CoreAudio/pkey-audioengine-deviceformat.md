---
description: PKEY \_ AudioEngine \_ DeviceFormat 屬性會指定裝置格式，也就是使用者針對串流在音訊引擎和音訊端點裝置之間流動的格式（當裝置以共用模式運作時）。
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: 'PKEY_AudioEngine_DeviceFormat (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689128"
---
# <a name="pkey_audioengine_deviceformat"></a><span data-ttu-id="ba82d-103">PKEY \_ AudioEngine \_ DeviceFormat</span><span class="sxs-lookup"><span data-stu-id="ba82d-103">PKEY\_AudioEngine\_DeviceFormat</span></span>

<span data-ttu-id="ba82d-104">**PKEY \_ AudioEngine \_ DeviceFormat** 屬性會指定裝置格式，也就是使用者針對串流在音訊引擎和音訊端點裝置之間流動的格式（當裝置以共用模式運作時）。</span><span class="sxs-lookup"><span data-stu-id="ba82d-104">The **PKEY\_AudioEngine\_DeviceFormat** property specifies the device format, which is the format that the user has selected for the stream that flows between the audio engine and the audio endpoint device when the device operates in shared mode.</span></span> <span data-ttu-id="ba82d-105">此格式可能不是獨佔模式應用程式所要使用的最佳預設格式。</span><span class="sxs-lookup"><span data-stu-id="ba82d-105">This format might not be the best default format for an exclusive-mode application to use.</span></span> <span data-ttu-id="ba82d-106">一般而言，獨佔模式應用程式會對 [**IAudioClient：： IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) 方法進行一些呼叫，以尋找適合的裝置格式。</span><span class="sxs-lookup"><span data-stu-id="ba82d-106">Typically, an exclusive-mode application finds a suitable device format by making some number of calls to the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method.</span></span> <span data-ttu-id="ba82d-107">如需詳細資訊，請參閱 [裝置格式](device-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="ba82d-107">For more information, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="ba82d-108">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ BLOB。</span><span class="sxs-lookup"><span data-stu-id="ba82d-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="ba82d-109">**PROPVARIANT** 結構的 **Blob** 成員是 **blob** 類型的結構，其中包含兩個成員。</span><span class="sxs-lookup"><span data-stu-id="ba82d-109">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="ba82d-110">成員 **blob。 cbSize** 是一個 **DWORD** ，可指定格式描述中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ba82d-110">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="ba82d-111">成員 **blob. pBlobData** 指向包含格式描述的 **WAVEFORMATEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="ba82d-111">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="ba82d-112">如需 **BLOB** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="ba82d-112">For more information about **BLOB**, see the Windows SDK documentation.</span></span> <span data-ttu-id="ba82d-113">如需 **WAVEFORMATEX** 的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="ba82d-113">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba82d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba82d-114">Requirements</span></span>



| <span data-ttu-id="ba82d-115">需求</span><span class="sxs-lookup"><span data-stu-id="ba82d-115">Requirement</span></span> | <span data-ttu-id="ba82d-116">值</span><span class="sxs-lookup"><span data-stu-id="ba82d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba82d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba82d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ba82d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba82d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ba82d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba82d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ba82d-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba82d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ba82d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ba82d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba82d-122"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba82d-122"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba82d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba82d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba82d-124">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="ba82d-124">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="ba82d-125">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="ba82d-125">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




