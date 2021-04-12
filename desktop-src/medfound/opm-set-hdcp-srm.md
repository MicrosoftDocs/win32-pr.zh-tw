---
description: 更新 (SRM) 的系統 renewability 訊息，以 High-Bandwidth 數位內容保護 (HDCP) 。
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: 'OPM_SET_HDCP_SRM (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191766"
---
# <a name="opm_set_hdcp_srm"></a><span data-ttu-id="b403a-103">OPM \_ 設定 \_ HDCP \_ SRM</span><span class="sxs-lookup"><span data-stu-id="b403a-103">OPM\_SET\_HDCP\_SRM</span></span>

<span data-ttu-id="b403a-104">更新 (SRM) 的系統 renewability 訊息，以 High-Bandwidth 數位內容保護 (HDCP) 。</span><span class="sxs-lookup"><span data-stu-id="b403a-104">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span>



| <span data-ttu-id="b403a-105">需求</span><span class="sxs-lookup"><span data-stu-id="b403a-105">Requirement</span></span> | <span data-ttu-id="b403a-106">值</span><span class="sxs-lookup"><span data-stu-id="b403a-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b403a-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="b403a-107">Command GUID</span></span> | <span data-ttu-id="b403a-108">OPM \_ 設定 \_ HDCP \_ SRM</span><span class="sxs-lookup"><span data-stu-id="b403a-108">OPM\_SET\_HDCP\_SRM</span></span>                                                                 |
| <span data-ttu-id="b403a-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="b403a-109">Input data</span></span>   | <span data-ttu-id="b403a-110">[**OPM \_ 設定 \_ HDCP \_ SRM \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)結構</span><span class="sxs-lookup"><span data-stu-id="b403a-110">An [**OPM\_SET\_HDCP\_SRM\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) structure</span></span> |



 

<span data-ttu-id="b403a-111">[**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)的 *pbAdditionalParameters* 參數必須指向包含 SRM 的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b403a-111">The *pbAdditionalParameters* parameter of [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) must point to a buffer that contains the SRM.</span></span> <span data-ttu-id="b403a-112">HDCP SRM 的格式記載于 HDCP 規格中。</span><span class="sxs-lookup"><span data-stu-id="b403a-112">The format of an HDCP SRM is documented in the HDCP specification.</span></span> <span data-ttu-id="b403a-113">將 *ulAdditionalParametersSize* 參數設定為等於緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b403a-113">Set the *ulAdditionalParametersSize* parameter equal to the size of the buffer, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="b403a-114">備註</span><span class="sxs-lookup"><span data-stu-id="b403a-114">Remarks</span></span>

<span data-ttu-id="b403a-115">SRMs 可用來更新已撤銷的 HDCP 裝置清單。</span><span class="sxs-lookup"><span data-stu-id="b403a-115">SRMs are used to update the list of revoked HDCP devices.</span></span> <span data-ttu-id="b403a-116">SRMs 是以影片內容提供。</span><span class="sxs-lookup"><span data-stu-id="b403a-116">SRMs are delivered with the video content.</span></span>

<span data-ttu-id="b403a-117">此命令會更新影片輸出的目前「SRM」。</span><span class="sxs-lookup"><span data-stu-id="b403a-117">This command updates the video output's current SRM.</span></span> <span data-ttu-id="b403a-118">如果在命令時啟用了 HDCP，則影片輸出會使用新的 SRM 來檢查是否已撤銷任何已連線的 HDCP 裝置。</span><span class="sxs-lookup"><span data-stu-id="b403a-118">If HDCP is enabled at the time of the command, the video output uses the new SRM to check whether any of the connected HDCP devices are revoked.</span></span> <span data-ttu-id="b403a-119">如果影片輸出偵測到已撤銷的裝置，則會停止顯示影片。</span><span class="sxs-lookup"><span data-stu-id="b403a-119">If the video output detects a revoked device, it stops displaying video.</span></span> <span data-ttu-id="b403a-120">如果您在 HDCP 停用時傳送此命令，則影片輸出會驗證 SRM 並加以儲存。</span><span class="sxs-lookup"><span data-stu-id="b403a-120">If you send this command while HDCP is disabled, the video output validates the SRM and stores it.</span></span> <span data-ttu-id="b403a-121">之後，如果應用程式啟用 HDCP，則影片輸出會使用新的 SRM 來檢查裝置的撤銷狀態。</span><span class="sxs-lookup"><span data-stu-id="b403a-121">Later, if the application enables HDCP, the video output uses the new SRM to check the device's revocation status.</span></span>

<span data-ttu-id="b403a-122">此命令可能會導致 **Configure** 方法傳回下列任何錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b403a-122">This command can cause the **Configure** method to return any of the following error codes.</span></span>



| <span data-ttu-id="b403a-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b403a-123">Return code</span></span>                                            | <span data-ttu-id="b403a-124">Description</span><span class="sxs-lookup"><span data-stu-id="b403a-124">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="b403a-125">錯誤 \_ 圖形 \_ OPM \_ 不正確 \_ SRM</span><span class="sxs-lookup"><span data-stu-id="b403a-125">ERROR\_GRAPHICS\_OPM\_INVALID\_SRM</span></span>                     | <span data-ttu-id="b403a-126">SRM 無效。</span><span class="sxs-lookup"><span data-stu-id="b403a-126">The SRM is not valid.</span></span>                   |
| <span data-ttu-id="b403a-127">錯誤 \_ 圖形 \_ OPM \_ 輸出 \_ 不 \_ \_ 支援 \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="b403a-127">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="b403a-128">影片輸出不支援 HDCP。</span><span class="sxs-lookup"><span data-stu-id="b403a-128">The video output does not support HDCP.</span></span> |



 

<span data-ttu-id="b403a-129">當 **IOPMVideoOutput** 介面 (COPP) 模擬經認證的輸出保護通訊協定時，不支援這個命令。</span><span class="sxs-lookup"><span data-stu-id="b403a-129">This command is not supported when the **IOPMVideoOutput** interface emulates Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="b403a-130">使用 COPP 的語法時，應用程式會負責剖析 SRMs 和檢查 HDCP 裝置的撤銷狀態。</span><span class="sxs-lookup"><span data-stu-id="b403a-130">When COPP semantics are used, the application is responsible for parsing SRMs and checking the revocation status of the HDCP device.</span></span> <span data-ttu-id="b403a-131">使用 [OPM \_ 取得連線 \_ 的 \_ HDCP \_ 裝置 \_ 資訊](opm-get-connected-hdcp-device-information.md) 狀態要求，取得裝置的金鑰選取向量 (KSV) ，這是檢查撤銷狀態所需的專案。</span><span class="sxs-lookup"><span data-stu-id="b403a-131">Use the [OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION](opm-get-connected-hdcp-device-information.md) status request to get the device's key selection vector (KSV), which is needed to check the revocation status.</span></span> <span data-ttu-id="b403a-132">如需 SRMs 的詳細資訊，請參閱 HDCP 規格。</span><span class="sxs-lookup"><span data-stu-id="b403a-132">For more information about SRMs, refer to the HDCP specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="b403a-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b403a-133">Requirements</span></span>



| <span data-ttu-id="b403a-134">需求</span><span class="sxs-lookup"><span data-stu-id="b403a-134">Requirement</span></span> | <span data-ttu-id="b403a-135">值</span><span class="sxs-lookup"><span data-stu-id="b403a-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b403a-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b403a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b403a-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b403a-137">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b403a-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b403a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b403a-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b403a-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b403a-140">標頭</span><span class="sxs-lookup"><span data-stu-id="b403a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b403a-141"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b403a-141"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b403a-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b403a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b403a-143">**IOPMVideoOutput：： Configure**</span><span class="sxs-lookup"><span data-stu-id="b403a-143">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="b403a-144">OPM 命令</span><span class="sxs-lookup"><span data-stu-id="b403a-144">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




