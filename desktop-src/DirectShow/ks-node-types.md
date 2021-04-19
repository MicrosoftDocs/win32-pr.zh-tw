---
description: 下列全域唯一識別碼 (Guid) 定義核心模式篩選的節點類型。 若要尋找節點類型，請查詢 IKsTopologyInfo 介面的篩選準則。
ms.assetid: 0e133ce3-8815-47d1-a5c3-577a98963912
title: 'KS 節點類型 (Ksmedia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSNODETYPE_DEV_SPECIFIC
- KSNODETYPE_VIDEO_CAMERA_TERMINAL
- KSNODETYPE_VIDEO_INPUT_MTT
- KSNODETYPE_VIDEO_INPUT_TERMINAL
- KSNODETYPE_VIDEO_OUTPUT_MTT
- KSNODETYPE_VIDEO_OUTPUT_TERMINAL
- KSNODETYPE_VIDEO_PROCESSING
- KSNODETYPE_VIDEO_SELECTOR
- KSNODETYPE_VIDEO_STREAMING
api_type:
- HeaderDef
api_location:
- Ksmedia.h
ms.openlocfilehash: eadae4fdd70fd80115ea4e8902ba1bb2aa7bf53b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977649"
---
# <a name="ks-node-types"></a><span data-ttu-id="9be9d-104">KS 節點類型</span><span class="sxs-lookup"><span data-stu-id="9be9d-104">KS Node Types</span></span>

<span data-ttu-id="9be9d-105">下列全域唯一識別碼 (Guid) 定義核心模式篩選的節點類型。</span><span class="sxs-lookup"><span data-stu-id="9be9d-105">The following globally unique identifiers (GUIDs) define node types for kernel-mode filters.</span></span> <span data-ttu-id="9be9d-106">若要尋找節點類型，請查詢 [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) 介面的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="9be9d-106">To find the node type, query the filter for the [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) interface.</span></span>



| <span data-ttu-id="9be9d-107">GUID</span><span class="sxs-lookup"><span data-stu-id="9be9d-107">GUID</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="9be9d-108">Description</span><span class="sxs-lookup"><span data-stu-id="9be9d-108">Description</span></span>                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KSNODETYPE_DEV_SPECIFIC"></span><span id="ksnodetype_dev_specific"></span><dl> <span data-ttu-id="9be9d-109"><dt>**KSNODETYPE \_ 開發人員 \_ 專用**</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-109"><dt>**KSNODETYPE\_DEV\_SPECIFIC**</dt></span></span> </dl>                             | <span data-ttu-id="9be9d-110">代表一或多個裝置特定的處理函式。</span><span class="sxs-lookup"><span data-stu-id="9be9d-110">Represents one or more device-specific processing functions.</span></span> <span data-ttu-id="9be9d-111">節點有一個輸入連接和一個輸出連接。</span><span class="sxs-lookup"><span data-stu-id="9be9d-111">The node has one input connection and one output connection.</span></span><br/> <span data-ttu-id="9be9d-112">節點可能會透過 KsProxy 外掛程式公開自訂 COM 介面（如果裝置製造商有提供的話）。</span><span class="sxs-lookup"><span data-stu-id="9be9d-112">The node may expose a custom COM interface through a KsProxy plug-in, if provided by the device manufacturer.</span></span><br/>                                            |
| <span id="KSNODETYPE_VIDEO_CAMERA_TERMINAL"></span><span id="ksnodetype_video_camera_terminal"></span><dl> <span data-ttu-id="9be9d-113"><dt>**KSNODETYPE \_ 攝影機 \_ \_ 終端機**</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-113"><dt>**KSNODETYPE\_VIDEO\_CAMERA\_TERMINAL**</dt></span></span> </dl> | <span data-ttu-id="9be9d-114">代表從相機感應器移入裝置的資料，與 USB 匯流排無關。</span><span class="sxs-lookup"><span data-stu-id="9be9d-114">Represents data moving into the device from a camera sensor, independent of the USB bus.</span></span> <span data-ttu-id="9be9d-115">節點有一個輸出連接。</span><span class="sxs-lookup"><span data-stu-id="9be9d-115">The node has one output connection.</span></span><br/> <span data-ttu-id="9be9d-116">此節點會公開用於控制攝影機的 [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) 和 [**ICameraControl**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-icameracontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="9be9d-116">The node exposes the [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) and [**ICameraControl**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-icameracontrol) interfaces for controlling the camera.</span></span><br/> |
| <span id="KSNODETYPE_VIDEO_INPUT_MTT"></span><span id="ksnodetype_video_input_mtt"></span><dl> <span data-ttu-id="9be9d-117"><dt>**KSNODETYPE \_ 影片 \_ 輸入 \_ MTT**</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-117"><dt>**KSNODETYPE\_VIDEO\_INPUT\_MTT**</dt></span></span> </dl>                   | <span data-ttu-id="9be9d-118">代表從連續媒體傳輸（例如 VTR 磁帶）移入裝置的資料，與 USB 匯流排無關。</span><span class="sxs-lookup"><span data-stu-id="9be9d-118">Represents data moving into the device from a sequential media transport, such as a VTR tape, independent of the USB bus.</span></span> <span data-ttu-id="9be9d-119">節點有一個輸出連接。</span><span class="sxs-lookup"><span data-stu-id="9be9d-119">The node has one output connection.</span></span><br/> <span data-ttu-id="9be9d-120">此節點會公開 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) 介面來控制傳輸機制。</span><span class="sxs-lookup"><span data-stu-id="9be9d-120">The node exposes the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface for controlling the transport mechanism.</span></span><br/>   |
| <span id="KSNODETYPE_VIDEO_INPUT_TERMINAL"></span><span id="ksnodetype_video_input_terminal"></span><dl> <span data-ttu-id="9be9d-121"><dt>**KSNODETYPE \_ 影片 \_ 輸入 \_ 終端機**</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-121"><dt>**KSNODETYPE\_VIDEO\_INPUT\_TERMINAL**</dt></span></span> </dl>    | <span data-ttu-id="9be9d-122">代表移入裝置的資料，與 USB 匯流排無關。</span><span class="sxs-lookup"><span data-stu-id="9be9d-122">Represents data moving into the device, independent of the USB bus.</span></span> <span data-ttu-id="9be9d-123">例如，此節點可能代表類比音訊插孔或 S/PDIF 插口。</span><span class="sxs-lookup"><span data-stu-id="9be9d-123">For example, this node may represent an analog audio jack or S/PDIF jack.</span></span> <span data-ttu-id="9be9d-124">節點有一個輸出連接。</span><span class="sxs-lookup"><span data-stu-id="9be9d-124">The node has one output connection.</span></span><br/>                                                                                                             |
| <span id="KSNODETYPE_VIDEO_OUTPUT_MTT"></span><span id="ksnodetype_video_output_mtt"></span><dl> <span data-ttu-id="9be9d-125"><dt>**KSNODETYPE \_ 影片 \_ 輸出 \_ MTT**</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-125"><dt>**KSNODETYPE\_VIDEO\_OUTPUT\_MTT**</dt></span></span> </dl>                | <span data-ttu-id="9be9d-126">代表從裝置移至連續媒體傳輸（例如 VTR 磁帶）的資料，與 USB 匯流排無關。</span><span class="sxs-lookup"><span data-stu-id="9be9d-126">Represents data moving from the device to a sequential media transport, such as a VTR tape, independent of the USB bus.</span></span> <span data-ttu-id="9be9d-127">節點有一個輸入連接。</span><span class="sxs-lookup"><span data-stu-id="9be9d-127">The node has one input connection.</span></span><br/> <span data-ttu-id="9be9d-128">此節點會公開 [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) 介面來控制傳輸機制。</span><span class="sxs-lookup"><span data-stu-id="9be9d-128">The node exposes the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface for controlling the transport mechanism.</span></span><br/>      |
| <span id="KSNODETYPE_VIDEO_OUTPUT_TERMINAL"></span><span id="ksnodetype_video_output_terminal"></span><dl> <span data-ttu-id="9be9d-129"><dt>**KSNODETYPE \_ 影片 \_ 輸出 \_ 終端機**</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-129"><dt>**KSNODETYPE\_VIDEO\_OUTPUT\_TERMINAL**</dt></span></span> </dl> | <span data-ttu-id="9be9d-130">代表移動自裝置的資料，與 USB 匯流排無關。</span><span class="sxs-lookup"><span data-stu-id="9be9d-130">Represents data moving from the device, independent of the USB bus.</span></span> <span data-ttu-id="9be9d-131">例如，此節點可能代表類比音訊插孔或 S/PDIF 插口。</span><span class="sxs-lookup"><span data-stu-id="9be9d-131">For example, this node may represent an analog audio jack or S/PDIF jack.</span></span> <span data-ttu-id="9be9d-132">節點有一個輸入連接。</span><span class="sxs-lookup"><span data-stu-id="9be9d-132">The node has one input connection.</span></span><br/>                                                                                                              |
| <span id="KSNODETYPE_VIDEO_PROCESSING"></span><span id="ksnodetype_video_processing"></span><dl> <span data-ttu-id="9be9d-133"><dt>**KSNODETYPE \_ 影片 \_ 處理**</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-133"><dt>**KSNODETYPE\_VIDEO\_PROCESSING**</dt></span></span> </dl>                 | <span data-ttu-id="9be9d-134">代表一或多個影片處理函數。</span><span class="sxs-lookup"><span data-stu-id="9be9d-134">Represents one or more video processing functions.</span></span> <span data-ttu-id="9be9d-135">節點有一個輸入連接和一個輸出連接。</span><span class="sxs-lookup"><span data-stu-id="9be9d-135">The node has one input connection and one output connection.</span></span><br/> <span data-ttu-id="9be9d-136">此節點會公開 [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) 和 [**IVideoProcAmp**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ivideoprocamp) 介面，以調整視訊訊號的品質。</span><span class="sxs-lookup"><span data-stu-id="9be9d-136">The node exposes the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) and [**IVideoProcAmp**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ivideoprocamp) interfaces to adjust the qualities of the video signal.</span></span><br/> |
| <span id="KSNODETYPE_VIDEO_SELECTOR"></span><span id="ksnodetype_video_selector"></span><dl> <span data-ttu-id="9be9d-137"><dt>**KSNODETYPE \_ 影片 \_ 選取器**</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-137"><dt>**KSNODETYPE\_VIDEO\_SELECTOR**</dt></span></span> </dl>                       | <span data-ttu-id="9be9d-138">表示從兩個或多個可能來源選取輸入路徑的機制。</span><span class="sxs-lookup"><span data-stu-id="9be9d-138">Represents a mechanism to select the input path from two or more possible sources.</span></span> <span data-ttu-id="9be9d-139">節點有兩個或多個輸入連接和一個輸出連接。</span><span class="sxs-lookup"><span data-stu-id="9be9d-139">The node has two or more input connections and one output connection.</span></span><br/> <span data-ttu-id="9be9d-140">節點會公開 [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) 介面，以便在輸入之間進行選取。</span><span class="sxs-lookup"><span data-stu-id="9be9d-140">The node exposes the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface for selecting between inputs.</span></span><br/>                               |
| <span id="KSNODETYPE_VIDEO_STREAMING"></span><span id="ksnodetype_video_streaming"></span><dl> <span data-ttu-id="9be9d-141"><dt>**KSNODETYPE \_ 影片 \_ 串流**</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-141"><dt>**KSNODETYPE\_VIDEO\_STREAMING**</dt></span></span> </dl>                    | <span data-ttu-id="9be9d-142">代表在主機與裝置之間移動的資料。</span><span class="sxs-lookup"><span data-stu-id="9be9d-142">Represents data moving between the host and the device.</span></span> <span data-ttu-id="9be9d-143">針對 UVC 裝置，此節點代表 USB 端點。</span><span class="sxs-lookup"><span data-stu-id="9be9d-143">For UVC devices, this node represents a USB endpoint.</span></span> <span data-ttu-id="9be9d-144">輸入端點有一個輸入連接;輸出端點有一個輸出連接。</span><span class="sxs-lookup"><span data-stu-id="9be9d-144">Input endpoints have one input connection; output endpoints have one output connection.</span></span><br/>                                                                                         |



## <a name="requirements"></a><span data-ttu-id="9be9d-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="9be9d-145">Requirements</span></span>



| <span data-ttu-id="9be9d-146">需求</span><span class="sxs-lookup"><span data-stu-id="9be9d-146">Requirement</span></span> | <span data-ttu-id="9be9d-147">值</span><span class="sxs-lookup"><span data-stu-id="9be9d-147">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9be9d-148">標頭</span><span class="sxs-lookup"><span data-stu-id="9be9d-148">Header</span></span><br/> | <dl> <span data-ttu-id="9be9d-149"><dt>Ksmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="9be9d-149"><dt>Ksmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9be9d-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9be9d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be9d-151">常數和 Guid</span><span class="sxs-lookup"><span data-stu-id="9be9d-151">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> </dl>

 

 




