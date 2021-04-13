---
description: 包含應用程式呈現描述項之 proxy 物件的指標。
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: 'MF_PD_PMPHOST_CONTEXT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386247"
---
# <a name="mf_pd_pmphost_context-attribute"></a><span data-ttu-id="7932f-103">MF \_ PD \_ PMPHOST \_ 內容屬性</span><span class="sxs-lookup"><span data-stu-id="7932f-103">MF\_PD\_PMPHOST\_CONTEXT attribute</span></span>

<span data-ttu-id="7932f-104">包含應用程式之展示描述項的 proxy 物件指標。</span><span class="sxs-lookup"><span data-stu-id="7932f-104">Contains a pointer to the proxy object for the application's presentation descriptor.</span></span>

## <a name="data-type"></a><span data-ttu-id="7932f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7932f-105">Data type</span></span>

<span data-ttu-id="7932f-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="7932f-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="7932f-107">備註</span><span class="sxs-lookup"><span data-stu-id="7932f-107">Remarks</span></span>

<span data-ttu-id="7932f-108">受保護的媒體路徑 (PMP) 主機會使用這個屬性，將應用程式的呈現描述項儲存在遠端呈現描述項上。</span><span class="sxs-lookup"><span data-stu-id="7932f-108">The Protected Media Path (PMP) host uses this attribute to store the application's presentation descriptor on the remote presentation descriptor.</span></span> <span data-ttu-id="7932f-109">屬性值是 [_ *IMFRemoteProxy* \*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="7932f-109">The attribute value is a pointer to the [_ *IMFRemoteProxy*\*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) interface.</span></span>

<span data-ttu-id="7932f-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="7932f-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7932f-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7932f-111">Requirements</span></span>



| <span data-ttu-id="7932f-112">需求</span><span class="sxs-lookup"><span data-stu-id="7932f-112">Requirement</span></span> | <span data-ttu-id="7932f-113">值</span><span class="sxs-lookup"><span data-stu-id="7932f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7932f-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7932f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7932f-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7932f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7932f-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7932f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7932f-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7932f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7932f-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7932f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7932f-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7932f-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7932f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7932f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7932f-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7932f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7932f-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="7932f-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="7932f-123">**IMFAttributes：： SetUnknown**</span><span class="sxs-lookup"><span data-stu-id="7932f-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="7932f-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7932f-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="7932f-125">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="7932f-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




