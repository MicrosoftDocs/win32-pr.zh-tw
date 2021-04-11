---
description: 網路來源加速資料流程的持續時間（以毫秒為單位）。
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: 'MFNETSOURCE_ACCELERATEDSTREAMINGDURATION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848315"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a><span data-ttu-id="4b117-103">MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION 屬性</span><span class="sxs-lookup"><span data-stu-id="4b117-103">MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="4b117-104">網路來源加速資料流程的持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4b117-104">Duration of accelerated streaming for the network source, in milliseconds.</span></span>



<span data-ttu-id="4b117-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4b117-105">Data type</span></span>

<span data-ttu-id="4b117-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="4b117-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4b117-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="4b117-107">PROPVARIANT member</span></span>

<span data-ttu-id="4b117-108">**DWORD** (儲存為 **LONG**) </span><span class="sxs-lookup"><span data-stu-id="4b117-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="4b117-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4b117-109">VT\_I4</span></span>

<span data-ttu-id="4b117-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="4b117-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="4b117-111">備註</span><span class="sxs-lookup"><span data-stu-id="4b117-111">Remarks</span></span>

<span data-ttu-id="4b117-112">常數 **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4b117-112">The constant **MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="4b117-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="4b117-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="4b117-114">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="4b117-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="4b117-115">若要設定屬性，請將 **IPropertyStore** 物件傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="4b117-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="4b117-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="4b117-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="4b117-117">此內容適用于 Windows Media Services 的快速啟動功能，可快速地播放內容，而不會等候冗長的初始緩衝。</span><span class="sxs-lookup"><span data-stu-id="4b117-117">This property applies to the Fast Start feature of Windows Media Services, which plays content quickly without waiting for lengthy initial buffering.</span></span> <span data-ttu-id="4b117-118">使用「快速啟動」時，執行 Windows Media Services 的伺服器會以比內容位元速率指定更快的速度，傳送內容開頭的一些資料。</span><span class="sxs-lookup"><span data-stu-id="4b117-118">When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.</span></span>

<span data-ttu-id="4b117-119">這個屬性的預設值為10000毫秒。</span><span class="sxs-lookup"><span data-stu-id="4b117-119">The default value of this property is 10,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b117-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b117-120">Requirements</span></span>



| <span data-ttu-id="4b117-121">需求</span><span class="sxs-lookup"><span data-stu-id="4b117-121">Requirement</span></span> | <span data-ttu-id="4b117-122">值</span><span class="sxs-lookup"><span data-stu-id="4b117-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b117-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b117-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b117-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b117-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4b117-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b117-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b117-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b117-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4b117-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4b117-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b117-128"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4b117-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b117-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b117-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b117-130">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="4b117-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4b117-131">網路來源功能</span><span class="sxs-lookup"><span data-stu-id="4b117-131">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="4b117-132">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="4b117-132">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




