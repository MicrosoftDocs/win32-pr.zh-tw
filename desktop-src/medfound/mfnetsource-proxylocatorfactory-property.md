---
description: 包含 IMFNetProxyLocatorFactory 介面的指標。
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: 'MFNETSOURCE_PROXYLOCATORFACTORY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114596"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a><span data-ttu-id="bdf44-103">MFNETSOURCE \_ PROXYLOCATORFACTORY 屬性</span><span class="sxs-lookup"><span data-stu-id="bdf44-103">MFNETSOURCE\_PROXYLOCATORFACTORY property</span></span>

<span data-ttu-id="bdf44-104">包含 [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bdf44-104">Contains a pointer to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>



<span data-ttu-id="bdf44-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="bdf44-105">Data type</span></span>

<span data-ttu-id="bdf44-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="bdf44-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bdf44-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="bdf44-107">PROPVARIANT member</span></span>

<span data-ttu-id="bdf44-108">**IUnknown** 指標</span><span class="sxs-lookup"><span data-stu-id="bdf44-108">**IUnknown** pointer</span></span>

<span data-ttu-id="bdf44-109">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="bdf44-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="bdf44-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="bdf44-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="bdf44-111">備註</span><span class="sxs-lookup"><span data-stu-id="bdf44-111">Remarks</span></span>

<span data-ttu-id="bdf44-112">常數 **MFNETSOURCE \_ PROXYLOCATORFACTORY** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="bdf44-112">The constant **MFNETSOURCE\_PROXYLOCATORFACTORY** defines the GUID for this property key.</span></span> <span data-ttu-id="bdf44-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="bdf44-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="bdf44-114">應用程式可以使用這個屬性來提供網路來源的自訂 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="bdf44-114">Applications can use this property to provide a custom proxy locator for the network source.</span></span> <span data-ttu-id="bdf44-115">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="bdf44-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="bdf44-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="bdf44-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf44-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdf44-117">Requirements</span></span>



| <span data-ttu-id="bdf44-118">需求</span><span class="sxs-lookup"><span data-stu-id="bdf44-118">Requirement</span></span> | <span data-ttu-id="bdf44-119">值</span><span class="sxs-lookup"><span data-stu-id="bdf44-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf44-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bdf44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf44-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdf44-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bdf44-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bdf44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf44-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdf44-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bdf44-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bdf44-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf44-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf44-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdf44-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdf44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf44-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="bdf44-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="bdf44-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="bdf44-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="bdf44-129">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="bdf44-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




