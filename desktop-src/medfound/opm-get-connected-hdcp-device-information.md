---
description: 深入瞭解： OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: 'OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512584"
---
# <a name="opm_get_connected_hdcp_device_information"></a><span data-ttu-id="a2773-103">OPM \_ 取得 \_ 已連線的 \_ HDCP \_ 裝置 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="a2773-103">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>

<span data-ttu-id="a2773-104">取得連接至影片輸出 High-Bandwidth 數位內容保護 (HDCP) 裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a2773-104">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="a2773-105">會傳回下列資訊：</span><span class="sxs-lookup"><span data-stu-id="a2773-105">The following information is returned:</span></span>

-   <span data-ttu-id="a2773-106">裝置的 HDCP 金鑰選取向量 (KSV) 。</span><span class="sxs-lookup"><span data-stu-id="a2773-106">The device's HDCP key selection vector (KSV).</span></span>
-   <span data-ttu-id="a2773-107">裝置是否為 HDCP 中繼器。</span><span class="sxs-lookup"><span data-stu-id="a2773-107">Whether the device is an HDCP repeater.</span></span>



| <span data-ttu-id="a2773-108">需求</span><span class="sxs-lookup"><span data-stu-id="a2773-108">Requirement</span></span> | <span data-ttu-id="a2773-109">值</span><span class="sxs-lookup"><span data-stu-id="a2773-109">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2773-110">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="a2773-110">Request GUID</span></span> | <span data-ttu-id="a2773-111">OPM \_ 取得 \_ 已連線的 \_ HDCP \_ 裝置 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="a2773-111">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>                                                          |
| <span data-ttu-id="a2773-112">輸入資料</span><span class="sxs-lookup"><span data-stu-id="a2773-112">Input data</span></span>   | <span data-ttu-id="a2773-113">無</span><span class="sxs-lookup"><span data-stu-id="a2773-113">None</span></span>                                                                                                    |
| <span data-ttu-id="a2773-114">傳回資料</span><span class="sxs-lookup"><span data-stu-id="a2773-114">Return data</span></span>  | <span data-ttu-id="a2773-115">[**OPM \_ 連線的 \_ HDCP \_ 裝置 \_ 資訊**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)結構</span><span class="sxs-lookup"><span data-stu-id="a2773-115">An [**OPM\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a2773-116">備註</span><span class="sxs-lookup"><span data-stu-id="a2773-116">Remarks</span></span>

<span data-ttu-id="a2773-117">此查詢只能與 *COPP 模擬模式* 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a2773-117">This query can be used only with *COPP emulation mode*.</span></span> <span data-ttu-id="a2773-118">如果 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面使用輸出保護管理員 (OPM) 語義，則不支援此狀態要求。</span><span class="sxs-lookup"><span data-stu-id="a2773-118">If the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface uses Output Protection Manager (OPM) semantics, this status request is not supported.</span></span>

<span data-ttu-id="a2773-119">KSV 是提供給裝置製造商的識別碼，用於 HDCP 驗證和設定程式。</span><span class="sxs-lookup"><span data-stu-id="a2773-119">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="a2773-120">在 COPP 模擬模式中，應用程式會使用 KSV 來判斷是否已撤銷 HDCP 裝置。</span><span class="sxs-lookup"><span data-stu-id="a2773-120">In COPP emulation mode, the application uses the KSV to determine whether the HDCP device is revoked.</span></span> <span data-ttu-id="a2773-121">如果是，應用程式不應該播放受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="a2773-121">If it is, the application should not play protected content.</span></span> <span data-ttu-id="a2773-122">此外，如果裝置為 HDCP 中繼器，應用程式不應該播放受保護的內容，因為 COPP 不支援 HDCP 中繼器。</span><span class="sxs-lookup"><span data-stu-id="a2773-122">Also, the application should not play protected content if the device is an HDCP repeater, because COPP does not support HDCP repeaters.</span></span>

<span data-ttu-id="a2773-123">使用 OPM 語義時不需要此查詢，因為 OPM 支援裝置撤銷和 HDCP 中繼器。</span><span class="sxs-lookup"><span data-stu-id="a2773-123">This query is not needed when OPM semantics are used, because OPM supports device revocation and HDCP repeaters.</span></span>

<span data-ttu-id="a2773-124">此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryHDCPKeyData 查詢。</span><span class="sxs-lookup"><span data-stu-id="a2773-124">This query is equivalent to the DXVA\_COPPQueryHDCPKeyData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2773-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2773-125">Requirements</span></span>



| <span data-ttu-id="a2773-126">需求</span><span class="sxs-lookup"><span data-stu-id="a2773-126">Requirement</span></span> | <span data-ttu-id="a2773-127">值</span><span class="sxs-lookup"><span data-stu-id="a2773-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a2773-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2773-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a2773-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2773-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a2773-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2773-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a2773-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2773-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a2773-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a2773-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2773-133"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2773-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2773-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2773-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2773-135">**IOPMVideoOutput：： COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="a2773-135">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="a2773-136">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="a2773-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




