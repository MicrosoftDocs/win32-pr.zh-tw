---
description: 指定除了保護層級以外的視訊訊號相關資訊。
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: 'OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512577"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a><span data-ttu-id="071e2-103">OPM \_ 設定 \_ ACP \_ 和 \_ CGMSA \_ 信號</span><span class="sxs-lookup"><span data-stu-id="071e2-103">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="071e2-104">指定除了保護層級以外的視訊訊號相關資訊。</span><span class="sxs-lookup"><span data-stu-id="071e2-104">Specifies information about the video signal, other than the protection level.</span></span>



| <span data-ttu-id="071e2-105">需求</span><span class="sxs-lookup"><span data-stu-id="071e2-105">Requirement</span></span> | <span data-ttu-id="071e2-106">值</span><span class="sxs-lookup"><span data-stu-id="071e2-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="071e2-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="071e2-107">Command GUID</span></span> | <span data-ttu-id="071e2-108">OPM \_ 設定 \_ ACP \_ 和 \_ CGMSA \_ 信號</span><span class="sxs-lookup"><span data-stu-id="071e2-108">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                                                |
| <span data-ttu-id="071e2-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="071e2-109">Input data</span></span>   | <span data-ttu-id="071e2-110">[**OPM \_ 設定 \_ ACP \_ 和 \_ CGMSA \_ 信號 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters)結構</span><span class="sxs-lookup"><span data-stu-id="071e2-110">An [**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="071e2-111">備註</span><span class="sxs-lookup"><span data-stu-id="071e2-111">Remarks</span></span>

<span data-ttu-id="071e2-112">此命令相當於 \_ 經認證的輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPSetSignaling 命令。</span><span class="sxs-lookup"><span data-stu-id="071e2-112">This command is equivalent to the DXVA\_COPPSetSignaling command used in Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="071e2-113">針對 CGMS-A，某些保護標準需要電視信號在與 CGMS-A 位相同的 VBI 波形封包中包含資訊。</span><span class="sxs-lookup"><span data-stu-id="071e2-113">For CGMS-A, certain protection standards require that the television signal contain information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="071e2-114">除此之外，這項資訊也包含圖片外觀比例。</span><span class="sxs-lookup"><span data-stu-id="071e2-114">Among other things, this information includes the picture aspect ratio.</span></span> <span data-ttu-id="071e2-115">如果外觀比例資訊與影片串流不一致，則電視可能會顯示不良。</span><span class="sxs-lookup"><span data-stu-id="071e2-115">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="071e2-116">應用程式可以使用此命令來指定外觀比例，讓圖形驅動程式能夠產生正確的 VBI 封包。</span><span class="sxs-lookup"><span data-stu-id="071e2-116">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="071e2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="071e2-117">Requirements</span></span>



| <span data-ttu-id="071e2-118">需求</span><span class="sxs-lookup"><span data-stu-id="071e2-118">Requirement</span></span> | <span data-ttu-id="071e2-119">值</span><span class="sxs-lookup"><span data-stu-id="071e2-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="071e2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="071e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="071e2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="071e2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="071e2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="071e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="071e2-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="071e2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="071e2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="071e2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="071e2-125"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="071e2-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="071e2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="071e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071e2-127">**IOPMVideoOutput：： Configure**</span><span class="sxs-lookup"><span data-stu-id="071e2-127">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="071e2-128">OPM 命令</span><span class="sxs-lookup"><span data-stu-id="071e2-128">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




