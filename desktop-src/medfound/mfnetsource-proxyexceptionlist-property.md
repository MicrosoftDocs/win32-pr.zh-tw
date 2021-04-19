---
description: 指定可接受來自用戶端應用程式的連線，而不使用 proxy 伺服器的媒體伺服器清單（以分號分隔）。
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: 'MFNETSOURCE_PROXYEXCEPTIONLIST 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591f7036491964928937f2b48b0656e60f9a20f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977899"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a><span data-ttu-id="05726-103">MFNETSOURCE \_ PROXYEXCEPTIONLIST 屬性</span><span class="sxs-lookup"><span data-stu-id="05726-103">MFNETSOURCE\_PROXYEXCEPTIONLIST property</span></span>

<span data-ttu-id="05726-104">指定可接受來自用戶端應用程式的連線，而不使用 proxy 伺服器的媒體伺服器清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="05726-104">Specifies a semicolon-delimited list of media servers that can accept connections from client applications without using a proxy server.</span></span>



<span data-ttu-id="05726-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="05726-105">Data type</span></span>

<span data-ttu-id="05726-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="05726-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="05726-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="05726-107">PROPVARIANT member</span></span>

<span data-ttu-id="05726-108">寬字元字串 (**WCHAR** \*) </span><span class="sxs-lookup"><span data-stu-id="05726-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="05726-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="05726-109">VT\_LPWSTR</span></span>

<span data-ttu-id="05726-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="05726-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="05726-111">備註</span><span class="sxs-lookup"><span data-stu-id="05726-111">Remarks</span></span>

<span data-ttu-id="05726-112">常數 **MFNETSOURCE \_ PROXYEXCEPTIONLIST** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="05726-112">The constant **MFNETSOURCE\_PROXYEXCEPTIONLIST** defines the GUID for this property key.</span></span> <span data-ttu-id="05726-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="05726-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="05726-114">應用程式可以在建立 proxy 定位器物件時使用這個屬性來設定 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="05726-114">Applications can use this property to configure the proxy locator when creating the proxy locator object.</span></span> <span data-ttu-id="05726-115">若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。</span><span class="sxs-lookup"><span data-stu-id="05726-115">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="05726-116">Proxy 定位器不會針對這些位址執行 proxy 偵測。</span><span class="sxs-lookup"><span data-stu-id="05726-116">The proxy locator does not perform proxy detection for these addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="05726-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="05726-117">Requirements</span></span>



| <span data-ttu-id="05726-118">需求</span><span class="sxs-lookup"><span data-stu-id="05726-118">Requirement</span></span> | <span data-ttu-id="05726-119">值</span><span class="sxs-lookup"><span data-stu-id="05726-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05726-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05726-120">Minimum supported client</span></span><br/> | <span data-ttu-id="05726-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05726-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="05726-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05726-122">Minimum supported server</span></span><br/> | <span data-ttu-id="05726-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05726-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="05726-124">標頭</span><span class="sxs-lookup"><span data-stu-id="05726-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="05726-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="05726-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05726-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05726-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05726-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="05726-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="05726-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="05726-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="05726-129">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="05726-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




