---
description: 指定將在遠端進程中建立媒體來源。
ms.assetid: 3a2f9ff5-1780-40f3-b36b-3a7cccb47d05
title: 'MF_SESSION_REMOTE_SOURCE_MODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27b26a71e8bea53ab687eaf6126a1803e71ba16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193769"
---
# <a name="mf_session_remote_source_mode-attribute"></a><span data-ttu-id="9a802-103">MF \_ 會話 \_ 遠端 \_ 來源 \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="9a802-103">MF\_SESSION\_REMOTE\_SOURCE\_MODE attribute</span></span>

<span data-ttu-id="9a802-104">指定將在遠端進程中建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="9a802-104">Specifies that the media source will be created in a remote process.</span></span>

## <a name="data-type"></a><span data-ttu-id="9a802-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9a802-105">Data type</span></span>

<span data-ttu-id="9a802-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9a802-106">**UINT32**</span></span>

<span data-ttu-id="9a802-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="9a802-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a802-108">備註</span><span class="sxs-lookup"><span data-stu-id="9a802-108">Remarks</span></span>

<span data-ttu-id="9a802-109">您可以使用 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數，在受保護的媒體路徑上設定此屬性 (PMP) 會話。</span><span class="sxs-lookup"><span data-stu-id="9a802-109">You can set this attribute on the protected media path (PMP) session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="9a802-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9a802-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a802-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a802-111">Requirements</span></span>



| <span data-ttu-id="9a802-112">需求</span><span class="sxs-lookup"><span data-stu-id="9a802-112">Requirement</span></span> | <span data-ttu-id="9a802-113">值</span><span class="sxs-lookup"><span data-stu-id="9a802-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a802-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a802-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9a802-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a802-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9a802-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a802-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9a802-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a802-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9a802-118">標頭</span><span class="sxs-lookup"><span data-stu-id="9a802-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a802-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a802-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a802-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a802-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a802-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9a802-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a802-122">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9a802-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9a802-123">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9a802-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9a802-124">媒體會話屬性</span><span class="sxs-lookup"><span data-stu-id="9a802-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a802-125">PMP 媒體會話</span><span class="sxs-lookup"><span data-stu-id="9a802-125">PMP Media Session</span></span>](pmp-media-session.md)
</dt> </dl>

 

 




