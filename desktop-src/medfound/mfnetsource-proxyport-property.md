---
description: 指定 proxy 伺服器的埠號碼。
ms.assetid: cd84911b-3658-489f-b454-23eded0cbfa0
title: 'MFNETSOURCE_PROXYPORT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228f7d9390d53f7d8182a198879dcb2d81e3bae7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191878"
---
# <a name="mfnetsource_proxyport-property"></a><span data-ttu-id="70106-103">MFNETSOURCE \_ PROXYPORT 屬性</span><span class="sxs-lookup"><span data-stu-id="70106-103">MFNETSOURCE\_PROXYPORT property</span></span>

<span data-ttu-id="70106-104">指定 proxy 伺服器的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="70106-104">Specifies the port number of the proxy server.</span></span>



<span data-ttu-id="70106-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="70106-105">Data type</span></span>

<span data-ttu-id="70106-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="70106-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="70106-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="70106-107">PROPVARIANT member</span></span>

<span data-ttu-id="70106-108">**DWORD** (儲存為 **LONG**) </span><span class="sxs-lookup"><span data-stu-id="70106-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="70106-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="70106-109">VT\_I4</span></span>

<span data-ttu-id="70106-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="70106-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="70106-111">備註</span><span class="sxs-lookup"><span data-stu-id="70106-111">Remarks</span></span>

<span data-ttu-id="70106-112">常數 **MFNETSOURCE \_ PROXYPORT** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="70106-112">The constant **MFNETSOURCE\_PROXYPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="70106-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="70106-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="70106-114">應用程式可以在建立 proxy 定位器物件時使用這個屬性來設定 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="70106-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="70106-115">若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。</span><span class="sxs-lookup"><span data-stu-id="70106-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="70106-116">如果未針對 HTTP 設定此屬性，則 proxy 定位器預設會使用80的值。</span><span class="sxs-lookup"><span data-stu-id="70106-116">If this property is not set for HTTP, then by default the proxy locator uses a value of 80.</span></span>

## <a name="requirements"></a><span data-ttu-id="70106-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="70106-117">Requirements</span></span>



| <span data-ttu-id="70106-118">需求</span><span class="sxs-lookup"><span data-stu-id="70106-118">Requirement</span></span> | <span data-ttu-id="70106-119">值</span><span class="sxs-lookup"><span data-stu-id="70106-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70106-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70106-120">Minimum supported client</span></span><br/> | <span data-ttu-id="70106-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70106-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="70106-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70106-122">Minimum supported server</span></span><br/> | <span data-ttu-id="70106-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70106-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="70106-124">標頭</span><span class="sxs-lookup"><span data-stu-id="70106-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="70106-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="70106-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70106-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70106-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70106-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="70106-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="70106-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="70106-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="70106-129">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="70106-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




