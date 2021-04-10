---
description: 包含網路來源的網路統計資料。
ms.assetid: 1948481b-febd-434b-a5dc-faef592ea0ed
title: 'MFNETSOURCE_STATISTICS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a09e6c0fe4697595ff3600135327ba093350e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111753"
---
# <a name="mfnetsource_statistics-property"></a><span data-ttu-id="7a74d-103">MFNETSOURCE \_ 統計資料屬性</span><span class="sxs-lookup"><span data-stu-id="7a74d-103">MFNETSOURCE\_STATISTICS Property</span></span>

<span data-ttu-id="7a74d-104">包含網路來源的網路統計資料。</span><span class="sxs-lookup"><span data-stu-id="7a74d-104">Contains network statistics for the network source.</span></span>

## <a name="data-type"></a><span data-ttu-id="7a74d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7a74d-105">Data Type</span></span>

<span data-ttu-id="7a74d-106">改變請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="7a74d-106">Varies; see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a74d-107">備註</span><span class="sxs-lookup"><span data-stu-id="7a74d-107">Remarks</span></span>

<span data-ttu-id="7a74d-108">常數 MFNETSOURCE \_ 統計資料會定義與 [**MFNETSOURCE \_ 統計資料 \_ 識別碼**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) 列舉搭配使用的 GUID，以定義一組屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7a74d-108">The constant MFNETSOURCE\_STATISTICS defines a GUID that is used in conjunction with the [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enumeration to define a set of property keys.</span></span> <span data-ttu-id="7a74d-109">集合中的每個屬性索引鍵都有 **fmtid** 等於 MFNETSOURCE \_ 統計資料，而 **pid** 等於列舉的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="7a74d-109">Each property key in the set has **fmtid** equal to MFNETSOURCE\_STATISTICS and **pid** equal to one member of the enumeration.</span></span> <span data-ttu-id="7a74d-110">如需詳細資訊，請參閱 [**MFNETSOURCE \_ 統計資料 \_ 識別碼**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)。</span><span class="sxs-lookup"><span data-stu-id="7a74d-110">For more information, see [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a74d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a74d-111">Requirements</span></span>



| <span data-ttu-id="7a74d-112">需求</span><span class="sxs-lookup"><span data-stu-id="7a74d-112">Requirement</span></span> | <span data-ttu-id="7a74d-113">值</span><span class="sxs-lookup"><span data-stu-id="7a74d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a74d-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a74d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7a74d-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a74d-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7a74d-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a74d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7a74d-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a74d-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7a74d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7a74d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a74d-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a74d-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a74d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a74d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a74d-121">用戶端記錄</span><span class="sxs-lookup"><span data-stu-id="7a74d-121">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="7a74d-122">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="7a74d-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="7a74d-123">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="7a74d-123">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




