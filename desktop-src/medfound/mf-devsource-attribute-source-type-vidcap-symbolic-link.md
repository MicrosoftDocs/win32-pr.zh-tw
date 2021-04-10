---
description: 包含影片捕獲驅動程式的符號連結。
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114605"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a><span data-ttu-id="f7f8d-103">MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結屬性</span><span class="sxs-lookup"><span data-stu-id="f7f8d-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute</span></span>

<span data-ttu-id="f7f8d-104">包含影片捕獲驅動程式的符號連結。</span><span class="sxs-lookup"><span data-stu-id="f7f8d-104">Contains the symbolic link for a video capture driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="f7f8d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f7f8d-105">Data type</span></span>

<span data-ttu-id="f7f8d-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="f7f8d-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="f7f8d-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="f7f8d-107">Get/set</span></span>

<span data-ttu-id="f7f8d-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="f7f8d-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="f7f8d-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="f7f8d-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7f8d-110">備註</span><span class="sxs-lookup"><span data-stu-id="f7f8d-110">Remarks</span></span>

<span data-ttu-id="f7f8d-111">使用這個屬性做為 [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) 函數的輸入。</span><span class="sxs-lookup"><span data-stu-id="f7f8d-111">Use this attribute as input to the [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="f7f8d-112">此外，此屬性是在下列函式所傳回的啟用物件上設定：</span><span class="sxs-lookup"><span data-stu-id="f7f8d-112">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="f7f8d-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="f7f8d-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="f7f8d-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="f7f8d-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="f7f8d-115">符號連結應該視為不透明的字串。</span><span class="sxs-lookup"><span data-stu-id="f7f8d-115">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="f7f8d-116">適用于裝置的可讀取顯示名稱會包含在 [ [MF DEVSOURCE 屬性] 的 [ \_ \_ \_ 易記 \_ 名稱](mf-devsource-attribute-friendly-name.md) ] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="f7f8d-116">The human-readable display name for a device is contained in the [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute.</span></span>

<span data-ttu-id="f7f8d-117">您可以將 MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結屬性作為 [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) 函數的 DevicePath 引數值傳入。</span><span class="sxs-lookup"><span data-stu-id="f7f8d-117">The MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute can be passed in as the value of the DevicePath argument of the [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) function.</span></span>

<span data-ttu-id="f7f8d-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="f7f8d-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7f8d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7f8d-119">Requirements</span></span>



| <span data-ttu-id="f7f8d-120">需求</span><span class="sxs-lookup"><span data-stu-id="f7f8d-120">Requirement</span></span> | <span data-ttu-id="f7f8d-121">值</span><span class="sxs-lookup"><span data-stu-id="f7f8d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f8d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7f8d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f7f8d-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7f8d-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f7f8d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7f8d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f7f8d-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7f8d-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f7f8d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f7f8d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7f8d-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7f8d-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7f8d-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7f8d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f8d-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f7f8d-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f7f8d-130">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="f7f8d-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="f7f8d-131">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="f7f8d-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
