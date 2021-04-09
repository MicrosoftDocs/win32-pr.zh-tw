---
description: 指定 ASF 媒體接收器應該如何套用 Windows Media DRM。
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: 'MFPKEY_ASFMEDIASINK_DRMACTION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696274"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a><span data-ttu-id="3a222-103">MFPKEY \_ ASFMEDIASINK \_ DRMACTION 屬性</span><span class="sxs-lookup"><span data-stu-id="3a222-103">MFPKEY\_ASFMEDIASINK\_DRMACTION property</span></span>

<span data-ttu-id="3a222-104">指定 ASF 媒體接收器應該如何套用 Windows Media DRM。</span><span class="sxs-lookup"><span data-stu-id="3a222-104">Specifies how the ASF media sink should apply Windows Media DRM.</span></span>



<span data-ttu-id="3a222-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3a222-105">Data type</span></span>

<span data-ttu-id="3a222-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="3a222-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3a222-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="3a222-107">PROPVARIANT member</span></span>

<span data-ttu-id="3a222-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="3a222-108">**ULONG**</span></span>

<span data-ttu-id="3a222-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="3a222-109">VT\_UI4</span></span>

<span data-ttu-id="3a222-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="3a222-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="3a222-111">備註</span><span class="sxs-lookup"><span data-stu-id="3a222-111">Remarks</span></span>

<span data-ttu-id="3a222-112">這個屬性的值是 [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="3a222-112">The value of this property is a member of the [**MFSINK\_WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) enumeration.</span></span>

<span data-ttu-id="3a222-113">您可以使用這個屬性來設定 ASF 媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="3a222-113">You can use this attribute to configure the ASF media sink.</span></span> <span data-ttu-id="3a222-114">使用方式取決於您所呼叫用來建立 ASF 媒體接收器的函式：</span><span class="sxs-lookup"><span data-stu-id="3a222-114">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="3a222-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)：查詢 **IPropertyStore** 介面的已取出 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)指標。</span><span class="sxs-lookup"><span data-stu-id="3a222-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="3a222-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)：在 *pContentInfo* 參數中指定的 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標上呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 。</span><span class="sxs-lookup"><span data-stu-id="3a222-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a222-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a222-117">Requirements</span></span>



| <span data-ttu-id="3a222-118">需求</span><span class="sxs-lookup"><span data-stu-id="3a222-118">Requirement</span></span> | <span data-ttu-id="3a222-119">值</span><span class="sxs-lookup"><span data-stu-id="3a222-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a222-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a222-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3a222-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a222-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a222-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a222-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3a222-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a222-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a222-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3a222-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a222-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a222-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a222-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a222-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a222-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="3a222-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
