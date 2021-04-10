---
description: 指定預設 proxy 定位器的設定。
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: 'MFNETSOURCE_PROXYSETTINGS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114593"
---
# <a name="mfnetsource_proxysettings-property"></a><span data-ttu-id="f5543-103">MFNETSOURCE \_ PROXYSETTINGS 屬性</span><span class="sxs-lookup"><span data-stu-id="f5543-103">MFNETSOURCE\_PROXYSETTINGS property</span></span>

<span data-ttu-id="f5543-104">指定預設 proxy 定位器的設定。</span><span class="sxs-lookup"><span data-stu-id="f5543-104">Specifies the configuration setting for the default proxy locator.</span></span> <span data-ttu-id="f5543-105">這個屬性的值是 [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="f5543-105">The value of this property is a member of the [**MFNET\_PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) enumeration.</span></span>



<span data-ttu-id="f5543-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="f5543-106">Data type</span></span>

<span data-ttu-id="f5543-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="f5543-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f5543-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="f5543-108">PROPVARIANT member</span></span>

<span data-ttu-id="f5543-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="f5543-109">**LONG**</span></span>

<span data-ttu-id="f5543-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f5543-110">VT\_I4</span></span>

<span data-ttu-id="f5543-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="f5543-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f5543-112">備註</span><span class="sxs-lookup"><span data-stu-id="f5543-112">Remarks</span></span>

<span data-ttu-id="f5543-113">常數 **MFNETSOURCE \_ PROXYSETTINGS** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f5543-113">The constant **MFNETSOURCE\_PROXYSETTINGS** defines the GUID for this property key.</span></span> <span data-ttu-id="f5543-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="f5543-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="f5543-115">在建立預設 proxy 定位器物件時，應用程式可以使用這個屬性來設定 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="f5543-115">Applications can use this property to configure the proxy locator when creating the default proxy locator object.</span></span> <span data-ttu-id="f5543-116">若要設定屬性，請在 [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)函數的 *pProxyConfig* 參數中傳遞 **IPropertyStore** 指標。</span><span class="sxs-lookup"><span data-stu-id="f5543-116">To set the property, pass an **IPropertyStore** pointer in the *pProxyConfig* parameter of the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5543-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5543-117">Requirements</span></span>



| <span data-ttu-id="f5543-118">需求</span><span class="sxs-lookup"><span data-stu-id="f5543-118">Requirement</span></span> | <span data-ttu-id="f5543-119">值</span><span class="sxs-lookup"><span data-stu-id="f5543-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5543-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5543-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f5543-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5543-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f5543-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5543-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f5543-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5543-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f5543-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f5543-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5543-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5543-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5543-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5543-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5543-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="f5543-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f5543-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="f5543-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="f5543-129">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="f5543-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




