---
description: 網路來源緩衝的最大資料量（以毫秒為單位）。
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: 'MFNETSOURCE_MAXBUFFERTIMEMS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f98cd17f33bb893dacd02b2a00669f3d2355e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972892"
---
# <a name="mfnetsource_maxbuffertimems-property"></a><span data-ttu-id="6f474-103">MFNETSOURCE \_ MAXBUFFERTIMEMS 屬性</span><span class="sxs-lookup"><span data-stu-id="6f474-103">MFNETSOURCE\_MAXBUFFERTIMEMS property</span></span>

<span data-ttu-id="6f474-104">網路來源緩衝的最大資料量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6f474-104">Maximum amount of data the network source buffers, in milliseconds.</span></span>



<span data-ttu-id="6f474-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6f474-105">Data type</span></span>

<span data-ttu-id="6f474-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="6f474-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6f474-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="6f474-107">PROPVARIANT member</span></span>

<span data-ttu-id="6f474-108">**DWORD** (儲存為 **LONG**) </span><span class="sxs-lookup"><span data-stu-id="6f474-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="6f474-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6f474-109">VT\_I4</span></span>

<span data-ttu-id="6f474-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="6f474-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6f474-111">備註</span><span class="sxs-lookup"><span data-stu-id="6f474-111">Remarks</span></span>

<span data-ttu-id="6f474-112">常數 **MFNETSOURCE \_ MAXBUFFERTIMEMS** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="6f474-112">The constant **MFNETSOURCE\_MAXBUFFERTIMEMS** defines the GUID for this property key.</span></span> <span data-ttu-id="6f474-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="6f474-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6f474-114">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="6f474-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="6f474-115">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="6f474-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="6f474-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="6f474-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="6f474-117">這個屬性的預設值為40000毫秒。</span><span class="sxs-lookup"><span data-stu-id="6f474-117">The default value of this property is 40,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f474-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f474-118">Requirements</span></span>



| <span data-ttu-id="6f474-119">需求</span><span class="sxs-lookup"><span data-stu-id="6f474-119">Requirement</span></span> | <span data-ttu-id="6f474-120">值</span><span class="sxs-lookup"><span data-stu-id="6f474-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f474-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f474-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6f474-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f474-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6f474-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f474-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6f474-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f474-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6f474-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6f474-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f474-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6f474-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f474-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f474-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f474-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="6f474-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6f474-129">網路來源功能</span><span class="sxs-lookup"><span data-stu-id="6f474-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="6f474-130">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="6f474-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




