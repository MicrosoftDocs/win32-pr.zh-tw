---
description: 核心音訊列舉
ms.assetid: 7d25be71-ffbe-4e8c-9a45-cdeb35d10292
title: 核心音訊列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c786e1e18f25374a942a4140b67f0992ca7281
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468545"
---
# <a name="core-audio-enumerations"></a><span data-ttu-id="b65dd-103">核心音訊列舉</span><span class="sxs-lookup"><span data-stu-id="b65dd-103">Core Audio Enumerations</span></span>

<span data-ttu-id="b65dd-104">本節說明 Windows Vista 和更新版本中核心音訊 Api 使用的列舉。</span><span class="sxs-lookup"><span data-stu-id="b65dd-104">This section describes the enumerations that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="b65dd-105">列舉型別</span><span class="sxs-lookup"><span data-stu-id="b65dd-105">Enumeration</span></span>                                                                   | <span data-ttu-id="b65dd-106">描述</span><span class="sxs-lookup"><span data-stu-id="b65dd-106">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b65dd-107">**\_AUDCLNT \_ BUFFERFLAGS**</span><span class="sxs-lookup"><span data-stu-id="b65dd-107">**\_AUDCLNT\_BUFFERFLAGS**</span></span>](/windows/win32/api/audioclient/ne-audioclient-_audclnt_bufferflags)                        | <span data-ttu-id="b65dd-108">音訊端點緩衝區的狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="b65dd-108">Status flags for an audio endpoint buffer.</span></span>                                                         |
| [<span data-ttu-id="b65dd-109">**AUDCLNT \_ SHAREMODE**</span><span class="sxs-lookup"><span data-stu-id="b65dd-109">**AUDCLNT\_SHAREMODE**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audclnt_sharemode)                               | <span data-ttu-id="b65dd-110">資料流程的共用模式。</span><span class="sxs-lookup"><span data-stu-id="b65dd-110">The sharing mode for a stream.</span></span>                                                                     |
| [<span data-ttu-id="b65dd-111">**AUDCLNT \_ STREAMOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="b65dd-111">**AUDCLNT\_STREAMOPTIONS**</span></span>](/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions)                       | <span data-ttu-id="b65dd-112">定義描述音訊資料流程特性的值。</span><span class="sxs-lookup"><span data-stu-id="b65dd-112">Defines values that describe the characteristics of an audio stream.</span></span>                               |
| [<span data-ttu-id="b65dd-113">**音訊 \_ 串流 \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="b65dd-113">**AUDIO\_STREAM\_CATEGORY**</span></span>](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)                      | <span data-ttu-id="b65dd-114">指定音訊資料流程的類別。</span><span class="sxs-lookup"><span data-stu-id="b65dd-114">Specifies the category of an audio stream.</span></span>                                                         |
| [<span data-ttu-id="b65dd-115">**AudioSessionState**</span><span class="sxs-lookup"><span data-stu-id="b65dd-115">**AudioSessionState**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audiosessionstate)                                | <span data-ttu-id="b65dd-116">音訊會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="b65dd-116">The state of an audio session.</span></span>                                                                     |
| [<span data-ttu-id="b65dd-117">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="b65dd-117">**ConnectorType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-connectortype)                                        | <span data-ttu-id="b65dd-118">裝置拓撲中的連接器類型。</span><span class="sxs-lookup"><span data-stu-id="b65dd-118">The type of connector in a device topology.</span></span>                                                        |
| [<span data-ttu-id="b65dd-119">**資料流程**</span><span class="sxs-lookup"><span data-stu-id="b65dd-119">**DataFlow**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-dataflow)                                                  | <span data-ttu-id="b65dd-120">音訊串流的資料流程方向。</span><span class="sxs-lookup"><span data-stu-id="b65dd-120">The data-flow direction of an audio stream.</span></span>                                                        |
| [<span data-ttu-id="b65dd-121">**EDataFlow**</span><span class="sxs-lookup"><span data-stu-id="b65dd-121">**EDataFlow**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)                                                | <span data-ttu-id="b65dd-122">音訊資料在音訊端點裝置與用戶端應用程式之間流動的方向。</span><span class="sxs-lookup"><span data-stu-id="b65dd-122">The direction in which audio data flows between an audio endpoint device and a client application.</span></span> |
| [<span data-ttu-id="b65dd-123">**EndpointFormFactor**</span><span class="sxs-lookup"><span data-stu-id="b65dd-123">**EndpointFormFactor**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor)                              | <span data-ttu-id="b65dd-124">音訊端點裝置的一般實體屬性。</span><span class="sxs-lookup"><span data-stu-id="b65dd-124">The general physical attributes of an audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="b65dd-125">**ERole**</span><span class="sxs-lookup"><span data-stu-id="b65dd-125">**ERole**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)                                                        | <span data-ttu-id="b65dd-126">音訊端點裝置的系統角色。</span><span class="sxs-lookup"><span data-stu-id="b65dd-126">The system role of an audio endpoint device.</span></span>                                                       |
| [<span data-ttu-id="b65dd-127">**KSJACK \_ 接收 \_ CONNECTIONTYPE**</span><span class="sxs-lookup"><span data-stu-id="b65dd-127">**KSJACK\_SINK\_CONNECTIONTYPE**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-ksjack_sink_connectiontype)<br/> | <span data-ttu-id="b65dd-128">連接的類型。</span><span class="sxs-lookup"><span data-stu-id="b65dd-128">The type of connection.</span></span><br/>                                                                 |
| [<span data-ttu-id="b65dd-129">**PartType**</span><span class="sxs-lookup"><span data-stu-id="b65dd-129">**PartType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-parttype)                                                  | <span data-ttu-id="b65dd-130">元件的元件類型 (連接器，或是裝置拓撲中的子單位) 。</span><span class="sxs-lookup"><span data-stu-id="b65dd-130">The part type of a part (connector or subunit) in a device topology.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="b65dd-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="b65dd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b65dd-132">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="b65dd-132">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




