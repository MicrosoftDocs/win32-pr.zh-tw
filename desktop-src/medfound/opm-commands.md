---
description: OPM 命令
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: OPM 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976789"
---
# <a name="opm-commands"></a><span data-ttu-id="eb483-103">OPM 命令</span><span class="sxs-lookup"><span data-stu-id="eb483-103">OPM Commands</span></span>

<span data-ttu-id="eb483-104">本節列出 [輸出保護管理員](output-protection-manager.md) (OPM) 可用的命令。</span><span class="sxs-lookup"><span data-stu-id="eb483-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="eb483-105">若要傳送 OPM 命令，請呼叫 [**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)。</span><span class="sxs-lookup"><span data-stu-id="eb483-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="eb483-106">針對每個命令，會列出下列資訊。</span><span class="sxs-lookup"><span data-stu-id="eb483-106">For each command, the following information is listed.</span></span>



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb483-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="eb483-107">Command GUID</span></span> | <span data-ttu-id="eb483-108">識別命令。</span><span class="sxs-lookup"><span data-stu-id="eb483-108">Identifies the command.</span></span> <span data-ttu-id="eb483-109">將 [**OPM 設定 \_ \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)結構的 **guidSetting** 成員設定為等於此值。</span><span class="sxs-lookup"><span data-stu-id="eb483-109">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="eb483-110">輸入資料</span><span class="sxs-lookup"><span data-stu-id="eb483-110">Input data</span></span>   | <span data-ttu-id="eb483-111">指定如何在 [**OPM \_ 設定 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)結構中解讀 **abParameters** 陣列。</span><span class="sxs-lookup"><span data-stu-id="eb483-111">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="eb483-112">下列是已定義的命令：</span><span class="sxs-lookup"><span data-stu-id="eb483-112">The following commands are defined:</span></span>



| <span data-ttu-id="eb483-113">命令</span><span class="sxs-lookup"><span data-stu-id="eb483-113">Command</span></span>                                                                                                       | <span data-ttu-id="eb483-114">描述</span><span class="sxs-lookup"><span data-stu-id="eb483-114">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb483-115">**OPM \_ 設定 \_ ACP \_ 和 \_ CGMSA \_ 信號**</span><span class="sxs-lookup"><span data-stu-id="eb483-115">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="eb483-116">指定除了保護層級以外的視訊訊號相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb483-116">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="eb483-117">**OPM \_ 設定 \_ HDCP \_ SRM**</span><span class="sxs-lookup"><span data-stu-id="eb483-117">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="eb483-118">更新 (SRM) 的系統 renewability 訊息，以 High-Bandwidth 數位內容保護 (HDCP) 。</span><span class="sxs-lookup"><span data-stu-id="eb483-118">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="eb483-119">**OPM \_ SET \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="eb483-119">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="eb483-120">設定輸出保護機制的保護層級。</span><span class="sxs-lookup"><span data-stu-id="eb483-120">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="eb483-121">**\_ \_ \_ \_ 根據 \_ \_ CSS \_ DVD OPM 設定保護等級**</span><span class="sxs-lookup"><span data-stu-id="eb483-121">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="eb483-122">設定 DVD 播放的 HDCP 保護層級，並遵循 DVD 內容管理系統 (CSS) 規則。</span><span class="sxs-lookup"><span data-stu-id="eb483-122">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="eb483-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb483-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb483-124">OPM 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="eb483-124">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="eb483-125">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="eb483-125">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



