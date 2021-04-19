---
description: 提供回呼介面，讓應用程式從受保護的媒體路徑接收內容啟用程式物件 (PMP) 會話。
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: 'MF_SESSION_CONTENT_PROTECTION_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981186"
---
# <a name="mf_session_content_protection_manager-attribute"></a><span data-ttu-id="68c55-103">MF \_ 會話 \_ 內容 \_ 保護 \_ 管理員屬性</span><span class="sxs-lookup"><span data-stu-id="68c55-103">MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="68c55-104">提供回呼介面，讓應用程式從受保護的媒體路徑接收內容啟用程式物件 (PMP) 會話。</span><span class="sxs-lookup"><span data-stu-id="68c55-104">Provides a callback interface for the application to receive a content enabler object from the protected media path (PMP) session.</span></span>

## <a name="data-type"></a><span data-ttu-id="68c55-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="68c55-105">Data type</span></span>

<span data-ttu-id="68c55-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="68c55-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="68c55-107">備註</span><span class="sxs-lookup"><span data-stu-id="68c55-107">Remarks</span></span>

<span data-ttu-id="68c55-108">這個屬性的值是應用程式 [_ *IMFContentProtectionManager* \*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="68c55-108">The value of this attribute is a pointer to the application's [_ *IMFContentProtectionManager*\*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="68c55-109">使用 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數，在 PMP 會話上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="68c55-109">Set this attribute on the PMP session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="68c55-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="68c55-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68c55-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="68c55-111">Requirements</span></span>



| <span data-ttu-id="68c55-112">需求</span><span class="sxs-lookup"><span data-stu-id="68c55-112">Requirement</span></span> | <span data-ttu-id="68c55-113">值</span><span class="sxs-lookup"><span data-stu-id="68c55-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68c55-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68c55-114">Minimum supported client</span></span><br/> | <span data-ttu-id="68c55-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68c55-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68c55-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68c55-116">Minimum supported server</span></span><br/> | <span data-ttu-id="68c55-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68c55-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68c55-118">標頭</span><span class="sxs-lookup"><span data-stu-id="68c55-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="68c55-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="68c55-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68c55-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68c55-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c55-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="68c55-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68c55-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="68c55-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="68c55-123">**IMFAttributes：： SetUnknown**</span><span class="sxs-lookup"><span data-stu-id="68c55-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="68c55-124">媒體會話屬性</span><span class="sxs-lookup"><span data-stu-id="68c55-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="68c55-125">如何播放受保護的媒體檔案</span><span class="sxs-lookup"><span data-stu-id="68c55-125">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




