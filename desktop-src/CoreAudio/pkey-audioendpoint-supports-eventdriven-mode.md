---
description: PKEY \_ AudioEndpoint \_ 支援 \_ EventDriven \_ 模式屬性，指出端點是否支援事件驅動模式。
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: 'PKEY_AudioEndpoint_Supports_EventDriven_Mode (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936444"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a><span data-ttu-id="f9a6f-103">PKEY \_ AudioEndpoint \_ 支援 \_ EventDriven \_ 模式</span><span class="sxs-lookup"><span data-stu-id="f9a6f-103">PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode</span></span>

<span data-ttu-id="f9a6f-104">**PKEY \_ AudioEndpoint \_ 支援 \_ EventDriven \_ 模式** 屬性，指出端點是否支援事件驅動模式。</span><span class="sxs-lookup"><span data-stu-id="f9a6f-104">The **PKEY\_AudioEndpoint\_Supports\_EventDriven\_Mode** property indicates whether the endpoint supports the event-driven mode.</span></span>

<span data-ttu-id="f9a6f-105">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ UI4。</span><span class="sxs-lookup"><span data-stu-id="f9a6f-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="f9a6f-106">**PROPVARIANT** 結構的 **uintVal** 成員是一個 **DWORD** ，表示端點是否支援事件驅動模式。</span><span class="sxs-lookup"><span data-stu-id="f9a6f-106">The **uintVal** member of the **PROPVARIANT** structure is a **DWORD** that indicates if the endpoint supports the event-driven mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9a6f-107">備註</span><span class="sxs-lookup"><span data-stu-id="f9a6f-107">Remarks</span></span>

<span data-ttu-id="f9a6f-108">這個屬性值是由 .inf 檔案中的音訊 OEM 填入，表示 HDAudio 硬體支援根據 WHQL 需求的事件驅動模式。</span><span class="sxs-lookup"><span data-stu-id="f9a6f-108">This property value is populated by an audio OEM in an .inf file to indicate that the HDAudio hardware supports event driven mode as per the WHQL requirement.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a6f-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9a6f-109">Requirements</span></span>



| <span data-ttu-id="f9a6f-110">需求</span><span class="sxs-lookup"><span data-stu-id="f9a6f-110">Requirement</span></span> | <span data-ttu-id="f9a6f-111">值</span><span class="sxs-lookup"><span data-stu-id="f9a6f-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a6f-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9a6f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f9a6f-113">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9a6f-113">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f9a6f-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9a6f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f9a6f-115">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9a6f-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9a6f-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f9a6f-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9a6f-117"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9a6f-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9a6f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9a6f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a6f-119">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="f9a6f-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="f9a6f-120">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="f9a6f-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




