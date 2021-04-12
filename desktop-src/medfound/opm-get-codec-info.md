---
description: 取得硬體編解碼器的業績值。
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: 'OPM_GET_CODEC_INFO (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191772"
---
# <a name="opm_get_codec_info"></a><span data-ttu-id="c371a-103">OPM \_ 取得 \_ 編解碼器 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="c371a-103">OPM\_GET\_CODEC\_INFO</span></span>

<span data-ttu-id="c371a-104">取得硬體編解碼器的業績值。</span><span class="sxs-lookup"><span data-stu-id="c371a-104">Gets the merit value of a hardware codec.</span></span>



| <span data-ttu-id="c371a-105">需求</span><span class="sxs-lookup"><span data-stu-id="c371a-105">Requirement</span></span> | <span data-ttu-id="c371a-106">值</span><span class="sxs-lookup"><span data-stu-id="c371a-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c371a-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="c371a-107">Request GUID</span></span> | <span data-ttu-id="c371a-108">**OPM \_ 取得 \_ 編解碼器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="c371a-108">**OPM\_GET\_CODEC\_INFO**</span></span>                                                                 |
| <span data-ttu-id="c371a-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="c371a-109">Input data</span></span>   | <span data-ttu-id="c371a-110">[**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)結構</span><span class="sxs-lookup"><span data-stu-id="c371a-110">An [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure</span></span>   |
| <span data-ttu-id="c371a-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="c371a-111">Return data</span></span>  | <span data-ttu-id="c371a-112">[**OPM \_ 取得 \_ 編解碼器 \_ 資訊 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)結構</span><span class="sxs-lookup"><span data-stu-id="c371a-112">An [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c371a-113">備註</span><span class="sxs-lookup"><span data-stu-id="c371a-113">Remarks</span></span>

<span data-ttu-id="c371a-114">雖然此命令會使用 [輸出保護管理員](output-protection-manager.md) (OPM) 介面，但它只適用于硬體編碼器和解碼器。</span><span class="sxs-lookup"><span data-stu-id="c371a-114">Although this command uses the [Output Protection Manager](output-protection-manager.md) (OPM) interface, it applies only to hardware encoders and decoders.</span></span> <span data-ttu-id="c371a-115">不適用於影片輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="c371a-115">It does not apply to video output devices.</span></span>

<span data-ttu-id="c371a-116">一般而言，您不應該直接使用此命令。</span><span class="sxs-lookup"><span data-stu-id="c371a-116">Generally, you should not use this command directly.</span></span> <span data-ttu-id="c371a-117">若要取得硬體編解碼器的業績值，請呼叫 [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) 函式。</span><span class="sxs-lookup"><span data-stu-id="c371a-117">To get the merit value for a hardware codec, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span> <span data-ttu-id="c371a-118">此函數會執行傳送 **OPM \_ 取得 \_ 編解碼器 \_ 資訊** 命令所需的所有 OPM 呼叫。</span><span class="sxs-lookup"><span data-stu-id="c371a-118">This function performs all of the OPM calls needed to send the **OPM\_GET\_CODEC\_INFO** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="c371a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c371a-119">Requirements</span></span>



| <span data-ttu-id="c371a-120">需求</span><span class="sxs-lookup"><span data-stu-id="c371a-120">Requirement</span></span> | <span data-ttu-id="c371a-121">值</span><span class="sxs-lookup"><span data-stu-id="c371a-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c371a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c371a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c371a-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c371a-123">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c371a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c371a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c371a-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c371a-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c371a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c371a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c371a-127"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c371a-127"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c371a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c371a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c371a-129">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="c371a-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> <dt>

[<span data-ttu-id="c371a-130">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="c371a-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="c371a-131">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="c371a-131">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




