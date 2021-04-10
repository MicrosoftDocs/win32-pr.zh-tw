---
description: 支援 MTP 擴充功能
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: 支援 MTP 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6a5a585167984ec944528bb74a6746e42ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851408"
---
# <a name="supporting-mtp-extensions"></a><span data-ttu-id="4b1a8-103">支援 MTP 擴充功能</span><span class="sxs-lookup"><span data-stu-id="4b1a8-103">Supporting MTP Extensions</span></span>

## <a name="media-transfer-protocol"></a><span data-ttu-id="4b1a8-104">媒體傳輸通訊協定</span><span class="sxs-lookup"><span data-stu-id="4b1a8-104">Media Transfer Protocol</span></span>

<span data-ttu-id="4b1a8-105">媒體傳輸通訊協定 (MTP) 是圖片傳輸通訊協定 (PTP) 的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-105">Media Transfer Protocol (MTP) is an extension to the Picture Transfer Protocol (PTP).</span></span> <span data-ttu-id="4b1a8-106">因此，所有的 PTP 通訊協定語法在 MTP 中都有效。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-106">As a result, all PTP protocol semantics are valid in MTP.</span></span>

<span data-ttu-id="4b1a8-107">MTP 會使用兩方、起始端和回應者之間的命令和回應進行通訊。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-107">MTP communicates by using commands and responses between two parties, the initiator and the responder.</span></span> <span data-ttu-id="4b1a8-108">相關裝置的角色很清楚地定義。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-108">The roles of the involved devices are very clearly defined.</span></span> <span data-ttu-id="4b1a8-109">電腦通常是起始端，而裝置一律是回應者。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-109">The PC typically is the initiator, and the device is always the responder.</span></span> <span data-ttu-id="4b1a8-110">非電腦裝置也可以是啟動者 (例如，汽車組或 Microsoft X box) 。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-110">A non-PC device could also be an initiator (for example, a car deck or a Microsoft X-box).</span></span> <span data-ttu-id="4b1a8-111">裝置絕對不能同時採用這兩個角色。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-111">A device can never assume both roles at the same time.</span></span>

<span data-ttu-id="4b1a8-112">啟動器會將命令傳送至回應程式以開始通訊。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-112">The initiator starts communication by sending a command to the responder.</span></span> <span data-ttu-id="4b1a8-113">回應程式會處理此命令並傳回適當的回應。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-113">The responder processes the command and sends back an appropriate response.</span></span> <span data-ttu-id="4b1a8-114">可能會有與命令相關聯的資料階段。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-114">There might be a data phase associated with the command.</span></span> <span data-ttu-id="4b1a8-115">如果是這種情況，則必須事先知道資料流程的方向，並由起始端和回應者接受。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-115">If this is the case, the direction of data flow must be known beforehand and accepted by both the initiator and the responder.</span></span> <span data-ttu-id="4b1a8-116">請注意，沒有指出新命令之資料流程的描述性標頭。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-116">Be aware that there is not a descriptive header that indicates data flows for new commands.</span></span>

<span data-ttu-id="4b1a8-117">回應程式可以啟動與啟動器無關的通訊。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-117">The responder can start communication independent of the initiator.</span></span> <span data-ttu-id="4b1a8-118">例如，回應程式可以將事件傳送給啟動器。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-118">For example, the responder can send events to the initiator.</span></span> <span data-ttu-id="4b1a8-119">但是，不能與事件一起傳送任何資料。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-119">However, no data can be sent together with the event.</span></span> <span data-ttu-id="4b1a8-120">如果有任何需要在事件中讀取的資料，啟動者必須傳送 MTP 命令，然後裝置可以傳送資料以回應命令。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-120">If there is any data that needs to be read as part of the event, the initiator must send an MTP command, and the device can then send data in response to the command.</span></span>

<span data-ttu-id="4b1a8-121">如需 MTP 的完整說明，請參閱 [mtp 規格](https://www.usb.org/sites/default/files/MTPv1_1.zip)。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-121">For a complete description of MTP, refer to the [MTP specification](https://www.usb.org/sites/default/files/MTPv1_1.zip).</span></span>

## <a name="sending-mtp-commands"></a><span data-ttu-id="4b1a8-122">傳送 MTP 命令</span><span class="sxs-lookup"><span data-stu-id="4b1a8-122">Sending MTP Commands</span></span>

<span data-ttu-id="4b1a8-123">應用程式可以藉由叫用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) 方法，將 MTP 命令傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-123">Applications can send MTP commands to a device by invoking the [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) method.</span></span> <span data-ttu-id="4b1a8-124">傳送的命令取決於是否有資料階段，以及是否有任何伴隨的資料讀取或寫入至裝置。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-124">The command that is sent depends on whether there is a data phase, and, on whether any accompanying data is read from or written to the device.</span></span> <span data-ttu-id="4b1a8-125">下表描述三個可能的 MTP 延伸模組命令。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-125">The following table describes the three possible MTP extension commands.</span></span>

<span data-ttu-id="4b1a8-126">請注意，這些命令是 MTP 專用的。因此，只由 WPD MTP 類別驅動程式所執行。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-126">Be aware that these commands are specific to MTP; and are therefore, only implemented by the WPD MTP class driver.</span></span>



|                                                                                                                                      |                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b1a8-127">命令</span><span class="sxs-lookup"><span data-stu-id="4b1a8-127">Command</span></span>                                                                                                                              | <span data-ttu-id="4b1a8-128">描述</span><span class="sxs-lookup"><span data-stu-id="4b1a8-128">Description</span></span>                                                                                       |
| [<span data-ttu-id="4b1a8-129">**WPD \_ 命令 \_ MTP \_ EXT \_ END \_ DATA \_ TRANSFER**</span><span class="sxs-lookup"><span data-stu-id="4b1a8-129">**WPD\_COMMAND\_MTP\_EXT\_END\_DATA\_TRANSFER**</span></span>](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | <span data-ttu-id="4b1a8-130">發出 MTP 命令，以對資料讀取或寫入作業的結束髮出信號。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-130">Issues an MTP command that signals the conclusion of a data read or write operation.</span></span>              |
| [<span data-ttu-id="4b1a8-131">**WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令（ \_ 不含 \_ 資料 \_ 階段）**</span><span class="sxs-lookup"><span data-stu-id="4b1a8-131">**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITHOUT\_DATA\_PHASE**</span></span>](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | <span data-ttu-id="4b1a8-132">發出 MTP 命令，而不使用對應的資料階段。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-132">Issues an MTP command without a corresponding data phase.</span></span>                                         |
| [<span data-ttu-id="4b1a8-133">**WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要 \_ 寫入的資料**</span><span class="sxs-lookup"><span data-stu-id="4b1a8-133">**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_WRITE**</span></span>](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | <span data-ttu-id="4b1a8-134">發出 MTP 命令，其後伴隨的資料會寫入至裝置。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-134">Issues an MTP command that is followed by accompanying data, which will be written to the device.</span></span> |
| [<span data-ttu-id="4b1a8-135">**WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要 \_ 讀取的資料**</span><span class="sxs-lookup"><span data-stu-id="4b1a8-135">**WPD\_COMMAND\_MTP\_EXT\_EXECUTE\_COMMAND\_WITH\_DATA\_TO\_READ**</span></span>](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | <span data-ttu-id="4b1a8-136">發出 MTP 命令，後面接著伴隨的資料（從裝置讀取）。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-136">Issues an MTP command that is followed by accompanying data, which is read from the device.</span></span>       |
| [<span data-ttu-id="4b1a8-137">**WPD \_ 命令 \_ MTP \_ EXT \_ 讀取 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="4b1a8-137">**WPD\_COMMAND\_MTP\_EXT\_READ\_DATA**</span></span>](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | <span data-ttu-id="4b1a8-138">發出 MTP 命令，此命令會將資料從裝置傳送到電腦。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-138">Issues an MTP command that sends data from the device to the PC.</span></span>                                  |
| [<span data-ttu-id="4b1a8-139">**WPD \_ 命令 \_ MTP \_ EXT \_ 寫入 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="4b1a8-139">**WPD\_COMMAND\_MTP\_EXT\_WRITE\_DATA**</span></span>](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | <span data-ttu-id="4b1a8-140">發出 MTP 命令，此命令會從電腦將資料傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-140">Issues an MTP command that sends data to the device from the PC.</span></span>                                  |



 

<span data-ttu-id="4b1a8-141">無論該階段為何，都必須指定 **WPD \_ 屬性 \_ mtp \_ ext \_ \_** ext operation 程式碼和 **WPD \_ 屬性 \_ mtp \_ ext ext 作業 \_ \_ 參數** 。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-141">Regardless of the phase, **WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_CODE** and **WPD\_PROPERTY\_MTP\_EXT\_OPERATION\_PARAMS** must be specified.</span></span>

<span data-ttu-id="4b1a8-142">如果 MTP 驅動程式能夠將命令傳送至裝置，則傳回值一律會包含 **WPD \_ 屬性 \_ MTP \_ EXT 的 \_ 回應 \_ 碼**。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-142">If the MTP driver was able to send the command to the device, the return values will always contain **WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_CODE**.</span></span> <span data-ttu-id="4b1a8-143">如果回應碼指出成功，而且命令的語法允許回應參數，則也會提供 **WPD \_ 屬性 \_ MTP \_ EXT \_ 回應 \_** 參數。</span><span class="sxs-lookup"><span data-stu-id="4b1a8-143">If the response code indicates success and if the semantics of the command allow for response parameters, **WPD\_PROPERTY\_MTP\_EXT\_RESPONSE\_PARAMS** will also be available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b1a8-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b1a8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b1a8-145">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="4b1a8-145">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 
