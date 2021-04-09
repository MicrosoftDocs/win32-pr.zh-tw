---
description: 指定網路來源是否快取內容。
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: 'MFNETSOURCE_CACHEENABLED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6f38398e44eaa25da7a5b1f88a76edb8e40924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848313"
---
# <a name="mfnetsource_cacheenabled-property"></a><span data-ttu-id="604f4-103">MFNETSOURCE \_ CACHEENABLED 屬性</span><span class="sxs-lookup"><span data-stu-id="604f4-103">MFNETSOURCE\_CACHEENABLED property</span></span>

<span data-ttu-id="604f4-104">指定網路來源是否快取內容。</span><span class="sxs-lookup"><span data-stu-id="604f4-104">Specifies whether the network source caches content.</span></span>



<span data-ttu-id="604f4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="604f4-105">Data type</span></span>

<span data-ttu-id="604f4-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="604f4-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="604f4-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="604f4-107">PROPVARIANT member</span></span>

<span data-ttu-id="604f4-108">布林 (**LONG**) </span><span class="sxs-lookup"><span data-stu-id="604f4-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="604f4-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="604f4-109">VT\_I4</span></span>

<span data-ttu-id="604f4-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="604f4-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="604f4-111">備註</span><span class="sxs-lookup"><span data-stu-id="604f4-111">Remarks</span></span>

<span data-ttu-id="604f4-112">常數 **MFNETSOURCE \_ CACHEENABLED** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="604f4-112">The constant **MFNETSOURCE\_CACHEENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="604f4-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="604f4-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="604f4-114">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="604f4-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="604f4-115">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="604f4-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="604f4-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="604f4-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="604f4-117">這個屬性的預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="604f4-117">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="604f4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="604f4-118">Requirements</span></span>



| <span data-ttu-id="604f4-119">需求</span><span class="sxs-lookup"><span data-stu-id="604f4-119">Requirement</span></span> | <span data-ttu-id="604f4-120">值</span><span class="sxs-lookup"><span data-stu-id="604f4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="604f4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="604f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="604f4-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="604f4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="604f4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="604f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="604f4-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="604f4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="604f4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="604f4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="604f4-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="604f4-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="604f4-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="604f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="604f4-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="604f4-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="604f4-129">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="604f4-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




