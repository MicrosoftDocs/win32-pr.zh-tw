---
description: 包含媒體會話拓撲載入器的 CLSID。
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: 'MF_SESSION_TOPOLOADER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977101"
---
# <a name="mf_session_topoloader-attribute"></a><span data-ttu-id="abece-103">MF \_ 會話 \_ TOPOLOADER 屬性</span><span class="sxs-lookup"><span data-stu-id="abece-103">MF\_SESSION\_TOPOLOADER attribute</span></span>

<span data-ttu-id="abece-104">包含媒體會話拓撲載入器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="abece-104">Contains the CLSID of a topology loader for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="abece-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="abece-105">Data type</span></span>

<span data-ttu-id="abece-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="abece-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="abece-107">備註</span><span class="sxs-lookup"><span data-stu-id="abece-107">Remarks</span></span>

<span data-ttu-id="abece-108">您可以使用這個屬性來提供媒體會話的自訂拓撲載入器。</span><span class="sxs-lookup"><span data-stu-id="abece-108">You can use this attribute to provide a custom topology loader for the Media Session.</span></span>

<span data-ttu-id="abece-109">使用 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)函數或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="abece-109">Set this attribute using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function or the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="abece-110">如果設定此屬性，媒體會話會在建立拓撲載入器時，使用指定的 CLSID 來呼叫 **CoCreateInstance** 。</span><span class="sxs-lookup"><span data-stu-id="abece-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID when it creates the topology loader.</span></span> <span data-ttu-id="abece-111">此 CLSID 所建立的物件必須公開 [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) 介面。</span><span class="sxs-lookup"><span data-stu-id="abece-111">The object created by this CLSID must expose the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="abece-112">如果未設定此屬性，則媒體會話會建立媒體基礎中提供的預設拓撲載入器。</span><span class="sxs-lookup"><span data-stu-id="abece-112">If this attribute is not set, the Media Session creates the default topology loader provided in Media Foundation.</span></span>

<span data-ttu-id="abece-113">拓撲載入器必須支援多執行緒單元。</span><span class="sxs-lookup"><span data-stu-id="abece-113">A topology loader must support multithreaded apartments.</span></span> <span data-ttu-id="abece-114">您應該將拓撲載入器註冊為 >threadingmodel = "Both"。</span><span class="sxs-lookup"><span data-stu-id="abece-114">You should register the topology loader as ThreadingModel="Both".</span></span> <span data-ttu-id="abece-115">此外，如果您在受保護的媒體路徑中使用拓撲載入器 (PMP) ，拓撲載入器必須是受信任的元件。</span><span class="sxs-lookup"><span data-stu-id="abece-115">Also, if you are using the topology loader inside the protected media path (PMP), the topology loader must be a trusted component.</span></span> <span data-ttu-id="abece-116">如需詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。</span><span class="sxs-lookup"><span data-stu-id="abece-116">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

<span data-ttu-id="abece-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="abece-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="abece-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="abece-118">Requirements</span></span>



| <span data-ttu-id="abece-119">需求</span><span class="sxs-lookup"><span data-stu-id="abece-119">Requirement</span></span> | <span data-ttu-id="abece-120">值</span><span class="sxs-lookup"><span data-stu-id="abece-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="abece-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="abece-121">Minimum supported client</span></span><br/> | <span data-ttu-id="abece-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abece-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="abece-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="abece-123">Minimum supported server</span></span><br/> | <span data-ttu-id="abece-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abece-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="abece-125">標頭</span><span class="sxs-lookup"><span data-stu-id="abece-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="abece-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="abece-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abece-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abece-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abece-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="abece-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="abece-129">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="abece-129">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="abece-130">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="abece-130">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="abece-131">媒體會話屬性</span><span class="sxs-lookup"><span data-stu-id="abece-131">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="abece-132">自訂拓撲載入器</span><span class="sxs-lookup"><span data-stu-id="abece-132">Custom Topology Loaders</span></span>](custom-topology-loaders.md)
</dt> </dl>

 

 




