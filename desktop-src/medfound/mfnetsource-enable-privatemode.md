---
description: 在網路來源中啟用私用下載模式。
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: 'MFNETSOURCE_ENABLE_PRI加值稅EMODE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971453"
---
# <a name="mfnetsource_enable_privatemode-property"></a><span data-ttu-id="694b5-103">MFNETSOURCE \_ ENABLE \_ PRI加值稅EMODE 屬性</span><span class="sxs-lookup"><span data-stu-id="694b5-103">MFNETSOURCE\_ENABLE\_PRIVATEMODE property</span></span>

<span data-ttu-id="694b5-104">在網路來源中啟用私用下載模式。</span><span class="sxs-lookup"><span data-stu-id="694b5-104">Enables private download mode in the network source.</span></span>



<span data-ttu-id="694b5-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="694b5-105">Data type</span></span>

<span data-ttu-id="694b5-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="694b5-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="694b5-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="694b5-107">PROPVARIANT member</span></span>

<span data-ttu-id="694b5-108">**Bool**</span><span class="sxs-lookup"><span data-stu-id="694b5-108">**BOOL**</span></span>

<span data-ttu-id="694b5-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="694b5-109">VT\_I4</span></span>

<span data-ttu-id="694b5-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="694b5-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="694b5-111">備註</span><span class="sxs-lookup"><span data-stu-id="694b5-111">Remarks</span></span>

<span data-ttu-id="694b5-112">如果這個屬性為 **TRUE**，則會在會話結束時清除快取。</span><span class="sxs-lookup"><span data-stu-id="694b5-112">If this property is **TRUE**, the cache is cleared when the session ends.</span></span>

<span data-ttu-id="694b5-113">**MFNETSOURCE \_ CLIENTGUID** 常數會定義屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="694b5-113">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="694b5-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="694b5-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="694b5-115">若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="694b5-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="694b5-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="694b5-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="694b5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="694b5-117">Requirements</span></span>



| <span data-ttu-id="694b5-118">需求</span><span class="sxs-lookup"><span data-stu-id="694b5-118">Requirement</span></span> | <span data-ttu-id="694b5-119">值</span><span class="sxs-lookup"><span data-stu-id="694b5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="694b5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="694b5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="694b5-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="694b5-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="694b5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="694b5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="694b5-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="694b5-123">None supported</span></span><br/>                                                          |
| <span data-ttu-id="694b5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="694b5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="694b5-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="694b5-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="694b5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="694b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="694b5-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="694b5-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="694b5-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="694b5-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




