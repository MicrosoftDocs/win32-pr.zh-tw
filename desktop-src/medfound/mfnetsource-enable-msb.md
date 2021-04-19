---
description: 指定是否在網路來源中啟用媒體串流廣播 (MSB) 多播通訊協定。
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: 'MFNETSOURCE_ENABLE_MSB 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b2a49876cf504bfc4e086ab1e064e6835283a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973685"
---
# <a name="mfnetsource_enable_msb-property"></a><span data-ttu-id="114ea-103">MFNETSOURCE \_ ENABLE \_ MSB 屬性</span><span class="sxs-lookup"><span data-stu-id="114ea-103">MFNETSOURCE\_ENABLE\_MSB property</span></span>

<span data-ttu-id="114ea-104">指定是否在網路來源中啟用媒體串流廣播 (MSB) 多播通訊協定。</span><span class="sxs-lookup"><span data-stu-id="114ea-104">Specifies whether the Media Stream Broadcast (MSB) multicast protocol is enabled in the network source.</span></span>



<span data-ttu-id="114ea-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="114ea-105">Data type</span></span>

<span data-ttu-id="114ea-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="114ea-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="114ea-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="114ea-107">PROPVARIANT member</span></span>

<span data-ttu-id="114ea-108">**LONG**</span><span class="sxs-lookup"><span data-stu-id="114ea-108">**LONG**</span></span>

<span data-ttu-id="114ea-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="114ea-109">VT\_I4</span></span>

<span data-ttu-id="114ea-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="114ea-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="114ea-111">備註</span><span class="sxs-lookup"><span data-stu-id="114ea-111">Remarks</span></span>

<span data-ttu-id="114ea-112">常數 **MFNETSOURCE \_ ENABLE \_ MSB** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="114ea-112">The constant **MFNETSOURCE\_ENABLE\_MSB** defines the GUID for this property key.</span></span> <span data-ttu-id="114ea-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="114ea-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="114ea-114">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="114ea-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="114ea-115">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="114ea-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="114ea-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="114ea-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="114ea-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="114ea-117">Requirements</span></span>



| <span data-ttu-id="114ea-118">需求</span><span class="sxs-lookup"><span data-stu-id="114ea-118">Requirement</span></span> | <span data-ttu-id="114ea-119">值</span><span class="sxs-lookup"><span data-stu-id="114ea-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="114ea-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="114ea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="114ea-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="114ea-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="114ea-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="114ea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="114ea-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="114ea-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="114ea-124">標頭</span><span class="sxs-lookup"><span data-stu-id="114ea-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="114ea-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="114ea-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="114ea-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="114ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114ea-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="114ea-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="114ea-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="114ea-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="114ea-129">支援的通訊協定</span><span class="sxs-lookup"><span data-stu-id="114ea-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




