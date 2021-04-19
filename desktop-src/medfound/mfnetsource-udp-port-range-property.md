---
description: 網路來源可以用來接收串流內容的有效 UDP 埠範圍。
ms.assetid: 97fe2d11-70f7-4baa-b49f-513d90146591
title: 'MFNETSOURCE_UDP_PORT_RANGE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04db8c450bd20adc8c03ec3b964b543f1500aa51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972666"
---
# <a name="mfnetsource_udp_port_range-property"></a><span data-ttu-id="4ceb5-103">MFNETSOURCE \_ UDP \_ 埠 \_ 範圍屬性</span><span class="sxs-lookup"><span data-stu-id="4ceb5-103">MFNETSOURCE\_UDP\_PORT\_RANGE property</span></span>

<span data-ttu-id="4ceb5-104">網路來源可以用來接收串流內容的有效 UDP 埠範圍。</span><span class="sxs-lookup"><span data-stu-id="4ceb5-104">The range of valid UDP ports that the network source can use to receive streaming content.</span></span> <span data-ttu-id="4ceb5-105">這個屬性的值是格式為 " *m*–*n* " 的字串，其中 *m* 和 *n* 是埠號碼。</span><span class="sxs-lookup"><span data-stu-id="4ceb5-105">The value of this property is a string with the form " *m*–*n* " where *m* and *n* are port numbers.</span></span>



<span data-ttu-id="4ceb5-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="4ceb5-106">Data type</span></span>

<span data-ttu-id="4ceb5-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="4ceb5-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4ceb5-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="4ceb5-108">PROPVARIANT member</span></span>

<span data-ttu-id="4ceb5-109">寬字元字串 (**WCHAR** \*) </span><span class="sxs-lookup"><span data-stu-id="4ceb5-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="4ceb5-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="4ceb5-110">VT\_LPWSTR</span></span>

<span data-ttu-id="4ceb5-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="4ceb5-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="4ceb5-112">備註</span><span class="sxs-lookup"><span data-stu-id="4ceb5-112">Remarks</span></span>

<span data-ttu-id="4ceb5-113">常數 **MFNETSOURCE \_ UDP \_ 埠 \_ 範圍** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4ceb5-113">The constant **MFNETSOURCE\_UDP\_PORT\_RANGE** defines the GUID for this property key.</span></span> <span data-ttu-id="4ceb5-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="4ceb5-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="4ceb5-115">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="4ceb5-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="4ceb5-116">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="4ceb5-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="4ceb5-117">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="4ceb5-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ceb5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ceb5-118">Requirements</span></span>



| <span data-ttu-id="4ceb5-119">需求</span><span class="sxs-lookup"><span data-stu-id="4ceb5-119">Requirement</span></span> | <span data-ttu-id="4ceb5-120">值</span><span class="sxs-lookup"><span data-stu-id="4ceb5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4ceb5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ceb5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4ceb5-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ceb5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4ceb5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ceb5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4ceb5-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ceb5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4ceb5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4ceb5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ceb5-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ceb5-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ceb5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ceb5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ceb5-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="4ceb5-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4ceb5-129">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="4ceb5-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




