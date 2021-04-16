---
description: 指定預設 proxy 定位器是否應該強制 proxy 自動偵測。
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: 'MFNETSOURCE_PROXYRERUNAUTODETECTION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512812"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a><span data-ttu-id="145d5-103">MFNETSOURCE \_ PROXYRERUNAUTODETECTION 屬性</span><span class="sxs-lookup"><span data-stu-id="145d5-103">MFNETSOURCE\_PROXYRERUNAUTODETECTION property</span></span>

<span data-ttu-id="145d5-104">指定預設 proxy 定位器是否應該強制 proxy 自動偵測。</span><span class="sxs-lookup"><span data-stu-id="145d5-104">Specifies whether the default proxy locator should force proxy auto-detection.</span></span>



<span data-ttu-id="145d5-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="145d5-105">Data type</span></span>

<span data-ttu-id="145d5-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="145d5-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="145d5-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="145d5-107">PROPVARIANT member</span></span>

<span data-ttu-id="145d5-108">布林 (**LONG**) </span><span class="sxs-lookup"><span data-stu-id="145d5-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="145d5-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="145d5-109">VT\_I4</span></span>

<span data-ttu-id="145d5-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="145d5-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="145d5-111">備註</span><span class="sxs-lookup"><span data-stu-id="145d5-111">Remarks</span></span>

<span data-ttu-id="145d5-112">常數 **MFNETSOURCE \_ PROXYSETTINGS** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="145d5-112">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="145d5-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="145d5-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="145d5-114">應用程式可以在建立 proxy 定位器物件時使用這個屬性來設定 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="145d5-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="145d5-115">若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。</span><span class="sxs-lookup"><span data-stu-id="145d5-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="145d5-116">在自動偵測模式中，proxy 定位器會使用 WinInet proxy 偵測機制。</span><span class="sxs-lookup"><span data-stu-id="145d5-116">In auto-detect mode, the proxy locator uses the WinInet proxy detection mechanism.</span></span> <span data-ttu-id="145d5-117">若要強制自動偵測，請將值設定為0。</span><span class="sxs-lookup"><span data-stu-id="145d5-117">To force auto-detection, set the value to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="145d5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="145d5-118">Requirements</span></span>



| <span data-ttu-id="145d5-119">需求</span><span class="sxs-lookup"><span data-stu-id="145d5-119">Requirement</span></span> | <span data-ttu-id="145d5-120">值</span><span class="sxs-lookup"><span data-stu-id="145d5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="145d5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="145d5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="145d5-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="145d5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="145d5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="145d5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="145d5-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="145d5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="145d5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="145d5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="145d5-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="145d5-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="145d5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="145d5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="145d5-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="145d5-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="145d5-129">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="145d5-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="145d5-130">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="145d5-130">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




