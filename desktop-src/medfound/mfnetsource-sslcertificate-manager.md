---
description: 儲存實 IMFSSLCertificateManager 介面之類別的 IUnknown 指標。
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: 'MFNETSOURCE_SSLCERTIFICATE_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980932"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a><span data-ttu-id="ed039-103">MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER 屬性</span><span class="sxs-lookup"><span data-stu-id="ed039-103">MFNETSOURCE\_SSLCERTIFICATE\_MANAGER property</span></span>

<span data-ttu-id="ed039-104">儲存實 [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager)介面之類別的 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="ed039-104">Stores the **IUnknown** pointer of the class that implements the [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) interface.</span></span> <span data-ttu-id="ed039-105">用戶端實作此實作會提供在伺服器要求用戶端 SSL 憑證時取得用戶端 SSL 憑證的方法。</span><span class="sxs-lookup"><span data-stu-id="ed039-105">The client implemention provides methods to get the client SSL certificate when it is requested by the server.</span></span>



<span data-ttu-id="ed039-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="ed039-106">Data type</span></span>

<span data-ttu-id="ed039-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="ed039-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ed039-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="ed039-108">PROPVARIANT member</span></span>

<span data-ttu-id="ed039-109">**IUnknown 指標**</span><span class="sxs-lookup"><span data-stu-id="ed039-109">**IUnknown pointer**</span></span>

<span data-ttu-id="ed039-110">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="ed039-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="ed039-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="ed039-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="ed039-112">備註</span><span class="sxs-lookup"><span data-stu-id="ed039-112">Remarks</span></span>

<span data-ttu-id="ed039-113">**MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER** 常數會定義屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ed039-113">The **MFNETSOURCE\_SSLCERTIFICATE\_MANAGER** constant defines the GUID for the property key.</span></span> <span data-ttu-id="ed039-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="ed039-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="ed039-115">若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="ed039-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="ed039-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="ed039-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed039-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed039-117">Requirements</span></span>



| <span data-ttu-id="ed039-118">需求</span><span class="sxs-lookup"><span data-stu-id="ed039-118">Requirement</span></span> | <span data-ttu-id="ed039-119">值</span><span class="sxs-lookup"><span data-stu-id="ed039-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed039-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed039-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed039-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed039-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ed039-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed039-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed039-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed039-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ed039-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ed039-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed039-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed039-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed039-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed039-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed039-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ed039-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ed039-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="ed039-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




