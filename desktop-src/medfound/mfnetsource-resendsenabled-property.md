---
description: 指定網路來源是否傳送 UDP 重新傳送要求以回應遺失的封包。
ms.assetid: 7956536d-9f3d-4875-8006-17e2cd577b61
title: 'MFNETSOURCE_RESENDSENABLED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2646a9ef3e23fbcc9b3dff205f87d268115177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979757"
---
# <a name="mfnetsource_resendsenabled-property"></a><span data-ttu-id="d10c0-103">MFNETSOURCE \_ RESENDSENABLED 屬性</span><span class="sxs-lookup"><span data-stu-id="d10c0-103">MFNETSOURCE\_RESENDSENABLED property</span></span>

<span data-ttu-id="d10c0-104">指定網路來源是否傳送 UDP 重新傳送要求以回應遺失的封包。</span><span class="sxs-lookup"><span data-stu-id="d10c0-104">Specifies whether the network source sends UDP resend requests in response to lost packets.</span></span>



<span data-ttu-id="d10c0-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d10c0-105">Data type</span></span>

<span data-ttu-id="d10c0-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="d10c0-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d10c0-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="d10c0-107">PROPVARIANT member</span></span>

<span data-ttu-id="d10c0-108">布林 (**LONG**) </span><span class="sxs-lookup"><span data-stu-id="d10c0-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="d10c0-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d10c0-109">VT\_I4</span></span>

<span data-ttu-id="d10c0-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="d10c0-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d10c0-111">備註</span><span class="sxs-lookup"><span data-stu-id="d10c0-111">Remarks</span></span>

<span data-ttu-id="d10c0-112">常數 **MFNETSOURCE \_ RESENDSENABLED** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d10c0-112">The constant **MFNETSOURCE\_RESENDSENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="d10c0-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="d10c0-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d10c0-114">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="d10c0-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="d10c0-115">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="d10c0-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="d10c0-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="d10c0-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="d10c0-117">這個屬性的預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d10c0-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10c0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d10c0-118">Requirements</span></span>



| <span data-ttu-id="d10c0-119">需求</span><span class="sxs-lookup"><span data-stu-id="d10c0-119">Requirement</span></span> | <span data-ttu-id="d10c0-120">值</span><span class="sxs-lookup"><span data-stu-id="d10c0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d10c0-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d10c0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d10c0-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d10c0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d10c0-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d10c0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d10c0-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d10c0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d10c0-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d10c0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d10c0-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d10c0-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d10c0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d10c0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10c0-128">用戶端記錄</span><span class="sxs-lookup"><span data-stu-id="d10c0-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="d10c0-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="d10c0-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d10c0-130">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="d10c0-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




