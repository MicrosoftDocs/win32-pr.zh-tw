---
title: WMDM 結構
description: 結構
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Windows Media 裝置管理員，結構
- 裝置管理員，結構
- 程式設計參考，結構
- Windows Media 裝置管理員、結構的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903aa07bbe3d01029eb2020b521523b545843f2a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104373967"
---
# <a name="wmdm-structures"></a><span data-ttu-id="e169b-107">WMDM 結構</span><span class="sxs-lookup"><span data-stu-id="e169b-107">WMDM structures</span></span>

<span data-ttu-id="e169b-108">Windows Media 裝置管理員定義下列結構。</span><span class="sxs-lookup"><span data-stu-id="e169b-108">Windows Media Device Manager defines the following structures.</span></span>



| <span data-ttu-id="e169b-109">結構</span><span class="sxs-lookup"><span data-stu-id="e169b-109">Structure</span></span>                                                   | <span data-ttu-id="e169b-110">Description</span><span class="sxs-lookup"><span data-stu-id="e169b-110">Description</span></span>                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e169b-111">**\_BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="e169b-111">**\_BITMAPINFOHEADER**</span></span>](-bitmapinfoheader.md)             | <span data-ttu-id="e169b-112">定義影片框架的格式。</span><span class="sxs-lookup"><span data-stu-id="e169b-112">Defines the format of video frame.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="e169b-113">**\_ \_ 中的 MTP 命令資料 \_**</span><span class="sxs-lookup"><span data-stu-id="e169b-113">**MTP\_COMMAND\_DATA\_IN**</span></span>](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | <span data-ttu-id="e169b-114">包含媒體傳輸通訊協定 (MTP) 使用 [**IWMDMDevice3：:D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) 方法傳送至裝置的自訂命令。</span><span class="sxs-lookup"><span data-stu-id="e169b-114">Contains Media Transport Protocol (MTP) custom commands that are sent to the device by using the [**IWMDMDevice3::DeviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) method.</span></span>                                                                           |
| [<span data-ttu-id="e169b-115">**MTP \_ 命令 \_ 資料 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="e169b-115">**MTP\_COMMAND\_DATA\_OUT**</span></span>](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | <span data-ttu-id="e169b-116">包含媒體傳輸通訊協定 (設備磁碟機所填滿的 MTP) 回應。</span><span class="sxs-lookup"><span data-stu-id="e169b-116">Contains Media Transport Protocol (MTP) responses that are filled by the device driver.</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="e169b-117">**OPAQUECOMMAND**</span><span class="sxs-lookup"><span data-stu-id="e169b-117">**OPAQUECOMMAND**</span></span>](opaquecommand.md)                      | <span data-ttu-id="e169b-118">包含命令的資料，這些命令是透過 Windows Media 裝置管理員傳遞至裝置，但不適合 Windows Media 裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="e169b-118">Contains data for commands that are passed through Windows Media Device Manager to a device but are not intended to be acted upon by Windows Media Device Manager.</span></span>                                                                                       |
| [<span data-ttu-id="e169b-119">**\_VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="e169b-119">**\_VIDEOINFOHEADER**</span></span>](-videoinfoheader.md)               | <span data-ttu-id="e169b-120">定義影片資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="e169b-120">Defines the format of a video stream.</span></span>                                                                                                                                                                                                                    |
| [<span data-ttu-id="e169b-121">**\_WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="e169b-121">**\_WAVEFORMATEX**</span></span>](-waveformatex.md)                     | <span data-ttu-id="e169b-122">定義波形音訊資料的格式。</span><span class="sxs-lookup"><span data-stu-id="e169b-122">Defines the format of waveform-audio data.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="e169b-123">**WMDM \_ 格式 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="e169b-123">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)  | <span data-ttu-id="e169b-124">描述特定格式之裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="e169b-124">Describes the capabilities of a device for a particular format.</span></span> <span data-ttu-id="e169b-125">此結構在 [**WMDM \_ \_ 配置**](wmdm-prop-config.md) 結構的陣列中包含一組屬性設定。</span><span class="sxs-lookup"><span data-stu-id="e169b-125">This structure contains a set of property configurations in an array of [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures.</span></span>                                                       |
| [<span data-ttu-id="e169b-126">**WMDM \_ \_ 配置設定**</span><span class="sxs-lookup"><span data-stu-id="e169b-126">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)              | <span data-ttu-id="e169b-127">針對特定格式，在裝置支援的所有屬性上描述一組相容的屬性值。</span><span class="sxs-lookup"><span data-stu-id="e169b-127">Describes a set of compatible property values across all the properties supported by the device for a particular format.</span></span> <span data-ttu-id="e169b-128">此結構在 [**WMDM 屬性 \_ \_ DESC**](wmdm-prop-desc.md) 結構的陣列中包含許多屬性描述。</span><span class="sxs-lookup"><span data-stu-id="e169b-128">This structure contains a number of property descriptions in an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures.</span></span> |
| [<span data-ttu-id="e169b-129">**WMDM 的一種 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e169b-129">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)                  | <span data-ttu-id="e169b-130">描述特定屬性設定中的有效屬性值。</span><span class="sxs-lookup"><span data-stu-id="e169b-130">Describes valid values of a property in a particular property configuration.</span></span>                                                                                                                                                                             |
| [<span data-ttu-id="e169b-131">**WMDM 的 \_ 主張 \_ 值 \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="e169b-131">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)   | <span data-ttu-id="e169b-132">針對特定屬性設定中的特定屬性，包含有效值的列舉集合。</span><span class="sxs-lookup"><span data-stu-id="e169b-132">Contains an enumerated set of valid values for a particular property in a particular property configuration.</span></span>                                                                                                                                             |
| [<span data-ttu-id="e169b-133">**WMDM \_ 的 \_ 值 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="e169b-133">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md) | <span data-ttu-id="e169b-134">描述特定屬性設定中特定屬性的有效值範圍。</span><span class="sxs-lookup"><span data-stu-id="e169b-134">Describes range of valid values for a particular property in a particular property configuration.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="e169b-135">**WMDMDATETIME**</span><span class="sxs-lookup"><span data-stu-id="e169b-135">**WMDMDATETIME**</span></span>](wmdmdatetime.md)                        | <span data-ttu-id="e169b-136">包含日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e169b-136">Contains a date and time.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="e169b-137">**WMDMID**</span><span class="sxs-lookup"><span data-stu-id="e169b-137">**WMDMID**</span></span>](wmdmid.md)                                    | <span data-ttu-id="e169b-138">描述序號和群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e169b-138">Describes serial numbers and group IDs.</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="e169b-139">**WMDMMetadataView**</span><span class="sxs-lookup"><span data-stu-id="e169b-139">**WMDMMetadataView**</span></span>](wmdmmetadataview.md)                | <span data-ttu-id="e169b-140">定義元資料檢視。</span><span class="sxs-lookup"><span data-stu-id="e169b-140">Defines the metadata view.</span></span>                                                                                                                                                                                                                               |
| [<span data-ttu-id="e169b-141">**WMDMRIGHTS**</span><span class="sxs-lookup"><span data-stu-id="e169b-141">**WMDMRIGHTS**</span></span>](wmdmrights.md)                            | <span data-ttu-id="e169b-142">描述內容使用權利。</span><span class="sxs-lookup"><span data-stu-id="e169b-142">Describes content-use rights.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="e169b-143">**WMFILECAPABILITIES**</span><span class="sxs-lookup"><span data-stu-id="e169b-143">**WMFILECAPABILITIES**</span></span>](wmfilecapabilities.md)            | <span data-ttu-id="e169b-144">描述 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="e169b-144">Describes a MIME type.</span></span>                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="e169b-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="e169b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e169b-146">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="e169b-146">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




