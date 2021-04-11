---
description: 指定是否啟用網路來源的資料流程切換。
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: 'MFNETSOURCE_THINNINGENABLED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d5b1b362f8776e80e3d12b591dbf2116217846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936555"
---
# <a name="mfnetsource_thinningenabled-property"></a><span data-ttu-id="ca626-103">MFNETSOURCE \_ THINNINGENABLED 屬性</span><span class="sxs-lookup"><span data-stu-id="ca626-103">MFNETSOURCE\_THINNINGENABLED property</span></span>

<span data-ttu-id="ca626-104">指定是否啟用網路來源的資料流程切換。</span><span class="sxs-lookup"><span data-stu-id="ca626-104">Specifies whether stream switching is enabled on the network source.</span></span> <span data-ttu-id="ca626-105">串流切換可讓媒體伺服器根據可用的頻寬，以多個位元速率 (MBR) 檔來變更資料流程。</span><span class="sxs-lookup"><span data-stu-id="ca626-105">Stream switching enables the media server to change streams in a multiple bit-rate (MBR) file, based on available bandwidth.</span></span>



<span data-ttu-id="ca626-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="ca626-106">Data type</span></span>

<span data-ttu-id="ca626-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="ca626-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ca626-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="ca626-108">PROPVARIANT member</span></span>

<span data-ttu-id="ca626-109">布林 (**LONG**) </span><span class="sxs-lookup"><span data-stu-id="ca626-109">Boolean (**LONG**)</span></span>

<span data-ttu-id="ca626-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ca626-110">VT\_I4</span></span>

<span data-ttu-id="ca626-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="ca626-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="ca626-112">備註</span><span class="sxs-lookup"><span data-stu-id="ca626-112">Remarks</span></span>

<span data-ttu-id="ca626-113">常數 **MFNETSOURCE \_ THINNINGENABLED** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ca626-113">The constant **MFNETSOURCE\_THINNINGENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="ca626-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="ca626-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="ca626-115">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="ca626-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="ca626-116">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="ca626-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="ca626-117">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="ca626-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="ca626-118">這個屬性的預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ca626-118">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca626-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca626-119">Requirements</span></span>



| <span data-ttu-id="ca626-120">需求</span><span class="sxs-lookup"><span data-stu-id="ca626-120">Requirement</span></span> | <span data-ttu-id="ca626-121">值</span><span class="sxs-lookup"><span data-stu-id="ca626-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca626-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca626-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ca626-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca626-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ca626-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca626-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ca626-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca626-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ca626-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ca626-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca626-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca626-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca626-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca626-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca626-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ca626-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ca626-130">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="ca626-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




