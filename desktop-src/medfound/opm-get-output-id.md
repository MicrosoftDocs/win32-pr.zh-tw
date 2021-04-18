---
description: 傳回與此影片輸出相關聯之監視的唯一識別碼。
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: 'OPM_GET_OUTPUT_ID (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983375"
---
# <a name="opm_get_output_id"></a><span data-ttu-id="60518-103">OPM \_ 取得 \_ 輸出 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="60518-103">OPM\_GET\_OUTPUT\_ID</span></span>

<span data-ttu-id="60518-104">傳回與此影片輸出相關聯之監視的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="60518-104">Returns the unique identifier of the monitor associated with this video output.</span></span>



| <span data-ttu-id="60518-105">需求</span><span class="sxs-lookup"><span data-stu-id="60518-105">Requirement</span></span> | <span data-ttu-id="60518-106">值</span><span class="sxs-lookup"><span data-stu-id="60518-106">Value</span></span> |
|--------------|------------------------------------------------------------------|
| <span data-ttu-id="60518-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="60518-107">Request GUID</span></span> | <span data-ttu-id="60518-108">OPM \_ 取得 \_ 輸出 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="60518-108">OPM\_GET\_OUTPUT\_ID</span></span>                                             |
| <span data-ttu-id="60518-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="60518-109">Input data</span></span>   | <span data-ttu-id="60518-110">無</span><span class="sxs-lookup"><span data-stu-id="60518-110">None</span></span>                                                             |
| <span data-ttu-id="60518-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="60518-111">Return data</span></span>  | <span data-ttu-id="60518-112">[**OPM \_ 輸出 \_ 識別碼 \_ 資料**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)結構</span><span class="sxs-lookup"><span data-stu-id="60518-112">An [**OPM\_OUTPUT\_ID\_DATA**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="60518-113">備註</span><span class="sxs-lookup"><span data-stu-id="60518-113">Remarks</span></span>

<span data-ttu-id="60518-114">影片驅動程式會將唯一識別碼指派給每個監視器。</span><span class="sxs-lookup"><span data-stu-id="60518-114">The video driver assigns a unique identifier to each monitor.</span></span> <span data-ttu-id="60518-115">此查詢會傳回與目前的 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 指標相關聯的監視器識別碼。</span><span class="sxs-lookup"><span data-stu-id="60518-115">This query returns the identifier for the monitor that is associated with the current [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="60518-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="60518-116">Requirements</span></span>



| <span data-ttu-id="60518-117">需求</span><span class="sxs-lookup"><span data-stu-id="60518-117">Requirement</span></span> | <span data-ttu-id="60518-118">值</span><span class="sxs-lookup"><span data-stu-id="60518-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="60518-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60518-119">Minimum supported client</span></span><br/> | <span data-ttu-id="60518-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60518-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="60518-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60518-121">Minimum supported server</span></span><br/> | <span data-ttu-id="60518-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60518-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="60518-123">標頭</span><span class="sxs-lookup"><span data-stu-id="60518-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="60518-124"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="60518-124"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60518-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60518-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60518-126">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="60518-126">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="60518-127">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="60518-127">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




