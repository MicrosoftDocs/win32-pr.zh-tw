---
description: 儲存網路來源所使用之 proxy 伺服器的主機名稱和埠。
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: 'MFNETSOURCE_PROXYINFO 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f73ceedf71e567e026c5e9af67a67c5d84bebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996805"
---
# <a name="mfnetsource_proxyinfo-property"></a><span data-ttu-id="83cc5-103">MFNETSOURCE \_ proxyinfo.conf 屬性</span><span class="sxs-lookup"><span data-stu-id="83cc5-103">MFNETSOURCE\_PROXYINFO property</span></span>

<span data-ttu-id="83cc5-104">儲存網路來源所使用之 proxy 伺服器的主機名稱和埠。</span><span class="sxs-lookup"><span data-stu-id="83cc5-104">Stores the host name and the port of the proxy server used by the network source.</span></span>



<span data-ttu-id="83cc5-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="83cc5-105">Data type</span></span>

<span data-ttu-id="83cc5-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="83cc5-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="83cc5-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="83cc5-107">PROPVARIANT member</span></span>

<span data-ttu-id="83cc5-108">寬字元字串 (**WCHAR** \*) </span><span class="sxs-lookup"><span data-stu-id="83cc5-108">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="83cc5-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="83cc5-109">VT\_LPWSTR</span></span>

<span data-ttu-id="83cc5-110">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="83cc5-110">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="83cc5-111">備註</span><span class="sxs-lookup"><span data-stu-id="83cc5-111">Remarks</span></span>

<span data-ttu-id="83cc5-112">常數 **MFNETSOURCE \_ proxyinfo.conf** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="83cc5-112">The constant **MFNETSOURCE\_PROXYINFO** defines the GUID for this property key.</span></span> <span data-ttu-id="83cc5-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="83cc5-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="83cc5-114">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="83cc5-114">This property is read-only.</span></span> <span data-ttu-id="83cc5-115">若要從網路來源取得屬性值，請呼叫 **IPropertyStore：： GetValue** ，並在 *金鑰* 參數中傳遞 **PROPERTYKEY** 結構。</span><span class="sxs-lookup"><span data-stu-id="83cc5-115">To get the property value from the network source, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="83cc5-116">**PROPERTYKEY** 的 **fmtid** 成員必須設定為屬性 GUID。</span><span class="sxs-lookup"><span data-stu-id="83cc5-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="83cc5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="83cc5-117">Requirements</span></span>



| <span data-ttu-id="83cc5-118">需求</span><span class="sxs-lookup"><span data-stu-id="83cc5-118">Requirement</span></span> | <span data-ttu-id="83cc5-119">值</span><span class="sxs-lookup"><span data-stu-id="83cc5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83cc5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83cc5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83cc5-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83cc5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="83cc5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83cc5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83cc5-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83cc5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="83cc5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="83cc5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="83cc5-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="83cc5-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83cc5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83cc5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83cc5-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="83cc5-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="83cc5-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="83cc5-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="83cc5-129">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="83cc5-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




