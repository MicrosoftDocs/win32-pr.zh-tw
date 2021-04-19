---
description: 核心音訊結構
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: 核心音訊結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973149"
---
# <a name="core-audio-structures"></a><span data-ttu-id="9b24b-103">核心音訊結構</span><span class="sxs-lookup"><span data-stu-id="9b24b-103">Core Audio Structures</span></span>

<span data-ttu-id="9b24b-104">本節說明 Windows Vista 和更新版本中核心音訊 Api 所使用的結構。</span><span class="sxs-lookup"><span data-stu-id="9b24b-104">This section describes the structures that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="9b24b-105">結構</span><span class="sxs-lookup"><span data-stu-id="9b24b-105">Structure</span></span>                                                                     | <span data-ttu-id="9b24b-106">Description</span><span class="sxs-lookup"><span data-stu-id="9b24b-106">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b24b-107">**音訊 \_ 大量 \_ 通知 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="9b24b-107">**AUDIO\_VOLUME\_NOTIFICATION\_DATA**</span></span>](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | <span data-ttu-id="9b24b-108">描述音訊端點裝置的音量層級或靜音狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9b24b-108">Describes a change in the volume level or muting state of an audio endpoint device.</span></span>                                                                                 |
| [<span data-ttu-id="9b24b-109">**DIRECTX \_ 音訊 \_ 啟動 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="9b24b-109">**DIRECTX\_AUDIO\_ACTIVATION\_PARAMS**</span></span>](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | <span data-ttu-id="9b24b-110">指定 DirectSound 資料流程的初始化參數。</span><span class="sxs-lookup"><span data-stu-id="9b24b-110">Specifies the initialization parameters for a DirectSound stream.</span></span>                                                                                                   |
| [<span data-ttu-id="9b24b-111">**KSJACK \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="9b24b-111">**KSJACK\_DESCRIPTION**</span></span>](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | <span data-ttu-id="9b24b-112">透過 [**IKsJackDescription：： GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); 抓取描述音訊插孔。</span><span class="sxs-lookup"><span data-stu-id="9b24b-112">Retrieved through [**IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describes an audio jack.</span></span>                                 |
| [<span data-ttu-id="9b24b-113">**KSJACK \_ DESCRIPTION2**</span><span class="sxs-lookup"><span data-stu-id="9b24b-113">**KSJACK\_DESCRIPTION2**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | <span data-ttu-id="9b24b-114">透過 [**IKsJackDescription2：： GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); 抓取描述音訊插孔。</span><span class="sxs-lookup"><span data-stu-id="9b24b-114">Retrieved through [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describes an audio jack.</span></span> <br/>                 |
| [<span data-ttu-id="9b24b-115">**KSJACK \_ 接收 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="9b24b-115">**KSJACK\_SINK\_INFORMATION**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | <span data-ttu-id="9b24b-116">透過 [**IKsJackSinkInformation：： GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); 抓取描述音訊插孔接收器。</span><span class="sxs-lookup"><span data-stu-id="9b24b-116">Retrieved through [**IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describes an audio jack sink.</span></span><br/> |
| [<span data-ttu-id="9b24b-117">**LUID**</span><span class="sxs-lookup"><span data-stu-id="9b24b-117">**LUID**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | <span data-ttu-id="9b24b-118">儲存影片埠識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b24b-118">Stores the video port identifier.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="9b24b-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b24b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b24b-120">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="9b24b-120">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




