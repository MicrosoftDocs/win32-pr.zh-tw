---
description: 包含媒體會話之品質管制員的 CLSID。
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: 'MF_SESSION_QUALITY_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319639"
---
# <a name="mf_session_quality_manager-attribute"></a><span data-ttu-id="c97eb-103">MF \_ 會話 \_ 品質 \_ 管理員屬性</span><span class="sxs-lookup"><span data-stu-id="c97eb-103">MF\_SESSION\_QUALITY\_MANAGER attribute</span></span>

<span data-ttu-id="c97eb-104">包含媒體會話之品質管制員的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="c97eb-104">Contains the CLSID of a quality manager for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="c97eb-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c97eb-105">Data type</span></span>

<span data-ttu-id="c97eb-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="c97eb-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="c97eb-107">備註</span><span class="sxs-lookup"><span data-stu-id="c97eb-107">Remarks</span></span>

<span data-ttu-id="c97eb-108">您可以使用這個屬性來提供媒體會話的自訂品質管制員。</span><span class="sxs-lookup"><span data-stu-id="c97eb-108">You can use this attribute to provide a custom quality manager for the Media Session.</span></span>

<span data-ttu-id="c97eb-109">使用 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c97eb-109">Set this attribute by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="c97eb-110">如果設定此屬性，則媒體會話會使用指定的 CLSID 來呼叫 **CoCreateInstance** ，以建立「品質管制員」。</span><span class="sxs-lookup"><span data-stu-id="c97eb-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID to create the quality manager.</span></span> <span data-ttu-id="c97eb-111">此 CLSID 所建立的物件必須公開 [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="c97eb-111">The object created by this CLSID must expose the [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) interface.</span></span>

<span data-ttu-id="c97eb-112">如果未設定此屬性，則媒體會話會建立媒體基礎中提供的預設品質管制員。</span><span class="sxs-lookup"><span data-stu-id="c97eb-112">If this attribute is not set, the Media Session creates the default quality manager provided in Media Foundation.</span></span>

<span data-ttu-id="c97eb-113">如果您想要執行不含品質管制員的媒體會話，請將此屬性設定為 **GUID \_ Null**。</span><span class="sxs-lookup"><span data-stu-id="c97eb-113">If you want to run the Media Session with no quality manager at all, set this attribute to **GUID\_NULL**.</span></span>

<span data-ttu-id="c97eb-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="c97eb-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c97eb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c97eb-115">Requirements</span></span>



| <span data-ttu-id="c97eb-116">需求</span><span class="sxs-lookup"><span data-stu-id="c97eb-116">Requirement</span></span> | <span data-ttu-id="c97eb-117">值</span><span class="sxs-lookup"><span data-stu-id="c97eb-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c97eb-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c97eb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c97eb-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c97eb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c97eb-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c97eb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c97eb-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c97eb-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c97eb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c97eb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c97eb-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c97eb-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97eb-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c97eb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97eb-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c97eb-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c97eb-126">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="c97eb-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="c97eb-127">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="c97eb-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="c97eb-128">媒體會話屬性</span><span class="sxs-lookup"><span data-stu-id="c97eb-128">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




