---
description: 指定裝置的顯示名稱。
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: 'MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab0d2bb3c0e75d547e1249a83261b7c804743ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967164"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a><span data-ttu-id="b187c-103">MF \_ DEVSOURCE \_ 屬性 \_ 易記 \_ 名稱屬性</span><span class="sxs-lookup"><span data-stu-id="b187c-103">MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME attribute</span></span>

<span data-ttu-id="b187c-104">指定裝置的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b187c-104">Specifies the display name for a device.</span></span> <span data-ttu-id="b187c-105">*顯示名稱* 是人們可讀取的字串，適合在使用者介面中顯示。</span><span class="sxs-lookup"><span data-stu-id="b187c-105">The *display name* is a human-readable string, suitable for display in a user interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="b187c-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="b187c-106">Data type</span></span>

<span data-ttu-id="b187c-107">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b187c-107">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="b187c-108">取得/設定</span><span class="sxs-lookup"><span data-stu-id="b187c-108">Get/set</span></span>

<span data-ttu-id="b187c-109">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="b187c-109">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="b187c-110">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="b187c-110">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="b187c-111">備註</span><span class="sxs-lookup"><span data-stu-id="b187c-111">Remarks</span></span>

<span data-ttu-id="b187c-112">這個屬性是在下列函式所傳回的啟用物件上設定：</span><span class="sxs-lookup"><span data-stu-id="b187c-112">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="b187c-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="b187c-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="b187c-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="b187c-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="b187c-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="b187c-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b187c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b187c-116">Requirements</span></span>



| <span data-ttu-id="b187c-117">需求</span><span class="sxs-lookup"><span data-stu-id="b187c-117">Requirement</span></span> | <span data-ttu-id="b187c-118">值</span><span class="sxs-lookup"><span data-stu-id="b187c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b187c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b187c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b187c-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b187c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b187c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b187c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b187c-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b187c-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b187c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b187c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b187c-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b187c-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b187c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b187c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b187c-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b187c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b187c-127">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="b187c-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="b187c-128">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="b187c-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




