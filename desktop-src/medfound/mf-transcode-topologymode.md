---
description: 針對拓撲載入器是否會載入以硬體為基礎的轉換，指定轉碼拓撲。
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: 'MF_TRANSCODE_TOPOLOGYMODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848317"
---
# <a name="mf_transcode_topologymode-attribute"></a><span data-ttu-id="83864-103">MF \_ 轉碼 \_ TOPOLOGYMODE 屬性</span><span class="sxs-lookup"><span data-stu-id="83864-103">MF\_TRANSCODE\_TOPOLOGYMODE attribute</span></span>

<span data-ttu-id="83864-104">針對拓撲載入器是否會載入以硬體為基礎的轉換，指定轉碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="83864-104">Specifies for a transcode topology whether the topology loader will load hardware-based transforms.</span></span>

<span data-ttu-id="83864-105">拓撲模式會指定硬體轉換 (例如硬體編解碼器) 是否可用於轉碼拓撲中。</span><span class="sxs-lookup"><span data-stu-id="83864-105">The topology mode specifies whether hardware transforms (such as hardware codecs) may be used in the transcode topology.</span></span> <span data-ttu-id="83864-106">應用程式可以藉由呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)，將此屬性儲存在轉碼設定檔中。</span><span class="sxs-lookup"><span data-stu-id="83864-106">The application can store this attribute in a transcode profile by calling [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span>

## <a name="data-type"></a><span data-ttu-id="83864-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="83864-107">Data type</span></span>

<span data-ttu-id="83864-108">**[**MF \_以 UINT32 形式儲存的轉碼 \_ TOPOLOGYMODE \_ 旗標**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** </span><span class="sxs-lookup"><span data-stu-id="83864-108">**[**MF\_TRANSCODE\_TOPOLOGYMODE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="83864-109">取得/設定</span><span class="sxs-lookup"><span data-stu-id="83864-109">Get/set</span></span>

<span data-ttu-id="83864-110">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="83864-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="83864-111">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="83864-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="83864-112">備註</span><span class="sxs-lookup"><span data-stu-id="83864-112">Remarks</span></span>

<span data-ttu-id="83864-113">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="83864-113">This attribute is optional.</span></span> <span data-ttu-id="83864-114">它必須有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="83864-114">It must have one of the following values.</span></span>



| <span data-ttu-id="83864-115">值</span><span class="sxs-lookup"><span data-stu-id="83864-115">Value</span></span>                                              | <span data-ttu-id="83864-116">描述</span><span class="sxs-lookup"><span data-stu-id="83864-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83864-117">**允許的 MF \_ 轉碼 \_ TOPOLOGYMODE \_ 硬體 \_**</span><span class="sxs-lookup"><span data-stu-id="83864-117">**MF\_TRANSCODE\_TOPOLOGYMODE\_HARDWARE\_ALLOWED**</span></span> | <span data-ttu-id="83864-118">拓撲載入器會載入以硬體為基礎的 MFTs，例如硬體解碼器（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="83864-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="83864-119">如果找不到硬體解碼器，或硬體解碼器因為某些原因而無法連線，拓撲載入器會自動切換回軟體解碼。</span><span class="sxs-lookup"><span data-stu-id="83864-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="83864-120">**\_僅限 MF 轉碼 \_ TOPOLOGYMODE \_ 軟體 \_**</span><span class="sxs-lookup"><span data-stu-id="83864-120">**MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**</span></span>    | <span data-ttu-id="83864-121">拓撲載入器只會載入軟體 MFTs，包括軟體解碼器。</span><span class="sxs-lookup"><span data-stu-id="83864-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="83864-122">預設值為 **\_ \_ \_ \_ 僅限 MF 轉碼 TOPOLOGYMODE SOFTWARE**。</span><span class="sxs-lookup"><span data-stu-id="83864-122">The default value is **MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**.</span></span>

<span data-ttu-id="83864-123">如果拓撲載入器將硬體 MFT 插入拓撲中，它會在 [拓撲] 節點上設定 [ [mft \_ 列舉 \_ 硬體 \_ URL] \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="83864-123">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="83864-124">若要檢查硬體 MFT 是否存在，請列舉已解析拓撲中的節點，並檢查此屬性是否存在。</span><span class="sxs-lookup"><span data-stu-id="83864-124">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="83864-125">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="83864-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="83864-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="83864-126">Requirements</span></span>



| <span data-ttu-id="83864-127">需求</span><span class="sxs-lookup"><span data-stu-id="83864-127">Requirement</span></span> | <span data-ttu-id="83864-128">值</span><span class="sxs-lookup"><span data-stu-id="83864-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83864-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83864-129">Minimum supported client</span></span><br/> | <span data-ttu-id="83864-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83864-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="83864-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83864-131">Minimum supported server</span></span><br/> | <span data-ttu-id="83864-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83864-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="83864-133">標頭</span><span class="sxs-lookup"><span data-stu-id="83864-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="83864-134"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="83864-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83864-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83864-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83864-136">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="83864-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="83864-137">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="83864-137">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="83864-138">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="83864-138">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="83864-139">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="83864-139">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




