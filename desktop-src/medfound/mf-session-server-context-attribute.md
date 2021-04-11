---
description: 可讓兩個媒體會話實例共用相同的受保護媒體路徑 (PMP) 進程。
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: 'MF_SESSION_SERVER_CONTEXT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115841"
---
# <a name="mf_session_server_context-attribute"></a><span data-ttu-id="399ac-103">MF \_ 會話 \_ 伺服器 \_ 內容屬性</span><span class="sxs-lookup"><span data-stu-id="399ac-103">MF\_SESSION\_SERVER\_CONTEXT attribute</span></span>

<span data-ttu-id="399ac-104">可讓兩個媒體會話實例共用相同的受保護媒體路徑 (PMP) 進程。</span><span class="sxs-lookup"><span data-stu-id="399ac-104">Enables two instances of the Media Session to share the same Protected Media Path (PMP) process.</span></span>

## <a name="data-type"></a><span data-ttu-id="399ac-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="399ac-105">Data type</span></span>

<span data-ttu-id="399ac-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="399ac-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="399ac-107">備註</span><span class="sxs-lookup"><span data-stu-id="399ac-107">Remarks</span></span>

<span data-ttu-id="399ac-108">如果您想要在現有的 PMP 流程中建立 PMP 媒體會話，請使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="399ac-108">Use this attribute if you want to create the PMP Media Session in an existing PMP process.</span></span> <span data-ttu-id="399ac-109">屬性的值是 [_ *IMFPMPServer* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="399ac-109">The value of the attribute is a pointer to the [_ *IMFPMPServer*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) interface.</span></span>

<span data-ttu-id="399ac-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="399ac-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="399ac-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="399ac-111">Requirements</span></span>



| <span data-ttu-id="399ac-112">需求</span><span class="sxs-lookup"><span data-stu-id="399ac-112">Requirement</span></span> | <span data-ttu-id="399ac-113">值</span><span class="sxs-lookup"><span data-stu-id="399ac-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="399ac-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="399ac-114">Minimum supported client</span></span><br/> | <span data-ttu-id="399ac-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="399ac-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="399ac-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="399ac-116">Minimum supported server</span></span><br/> | <span data-ttu-id="399ac-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="399ac-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="399ac-118">標頭</span><span class="sxs-lookup"><span data-stu-id="399ac-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="399ac-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="399ac-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="399ac-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="399ac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="399ac-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="399ac-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="399ac-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="399ac-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="399ac-123">**IMFAttributes：： SetUnknown**</span><span class="sxs-lookup"><span data-stu-id="399ac-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="399ac-124">媒體會話屬性</span><span class="sxs-lookup"><span data-stu-id="399ac-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




