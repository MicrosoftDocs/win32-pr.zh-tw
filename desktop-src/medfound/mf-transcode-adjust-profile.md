---
description: 定義轉碼拓撲之資料流程設定的設定檔旗標。 這些旗標定義于 MF \_ 轉碼 \_ 調整 \_ 設定檔 \_ 旗標列舉中。
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: 'MF_TRANSCODE_ADJUST_PROFILE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974540"
---
# <a name="mf_transcode_adjust_profile-attribute"></a><span data-ttu-id="c7649-104">MF \_ 轉碼 \_ 調整 \_ 配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="c7649-104">MF\_TRANSCODE\_ADJUST\_PROFILE attribute</span></span>

<span data-ttu-id="c7649-105">定義轉碼拓撲之資料流程設定的設定檔旗標。</span><span class="sxs-lookup"><span data-stu-id="c7649-105">Profile flags that define the stream settings for the transcode topology.</span></span> <span data-ttu-id="c7649-106">這些旗標定義于 [**MF \_ 轉碼 \_ 調整 \_ 設定檔 \_ 旗標**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="c7649-106">The flags are defined in the [**MF\_TRANSCODE\_ADJUST\_PROFILE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="c7649-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="c7649-107">Data type</span></span>

<span data-ttu-id="c7649-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c7649-108">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c7649-109">取得/設定</span><span class="sxs-lookup"><span data-stu-id="c7649-109">Get/set</span></span>

<span data-ttu-id="c7649-110">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="c7649-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c7649-111">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="c7649-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7649-112">備註</span><span class="sxs-lookup"><span data-stu-id="c7649-112">Remarks</span></span>

<span data-ttu-id="c7649-113">應用程式可以在轉碼設定檔上的容器層級設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c7649-113">An application can set this attribute at the container level on the transcode profile.</span></span> <span data-ttu-id="c7649-114">如果設定此屬性， [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) 函式會在拓撲建立期間變更資料流程屬性，視指定的旗標而定。</span><span class="sxs-lookup"><span data-stu-id="c7649-114">If this attribute is set, the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function changes the stream attributes during topology building, depending on the specified flag.</span></span> <span data-ttu-id="c7649-115">例如，如果應用程式指定 [ **MF \_ 轉碼 \_ 調整 \_ 設定檔] \_ 預設** 旗標，則會使用應用程式指定的資料流程設定來建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="c7649-115">For example, if the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_DEFAULT** flag, the application-specified stream settings are used to create the profile.</span></span>

<span data-ttu-id="c7649-116">針對影片串流，畫面速率會根據媒體來源進行更新。</span><span class="sxs-lookup"><span data-stu-id="c7649-116">For the video stream, the frame rate is updated based on the media source.</span></span> <span data-ttu-id="c7649-117">如果應用程式未指定交錯模式，預設會將設定檔更新為使用漸進式框架。</span><span class="sxs-lookup"><span data-stu-id="c7649-117">If the application does not specify the interlaced mode, the profile is updated to use progressive frames by default.</span></span>

<span data-ttu-id="c7649-118">如果應用程式指定「 **MF \_ 轉碼 \_ 調整 \_ 設定檔 \_ 使用 \_ 來源 \_ 屬性** 」旗標，則會將遺失的資料流程屬性從輸入媒體來源複製到轉碼設定檔中的串流設定。</span><span class="sxs-lookup"><span data-stu-id="c7649-118">If the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_USE\_SOURCE\_ATTRIBUTES** flag, then missing stream attributes are copied from the input media source to the stream settings in the transcode profile.</span></span>

<span data-ttu-id="c7649-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="c7649-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7649-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7649-120">Requirements</span></span>



| <span data-ttu-id="c7649-121">需求</span><span class="sxs-lookup"><span data-stu-id="c7649-121">Requirement</span></span> | <span data-ttu-id="c7649-122">值</span><span class="sxs-lookup"><span data-stu-id="c7649-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7649-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7649-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7649-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7649-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c7649-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7649-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7649-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7649-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c7649-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c7649-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7649-128"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7649-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7649-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7649-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7649-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c7649-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7649-131">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="c7649-131">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="c7649-132">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="c7649-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




