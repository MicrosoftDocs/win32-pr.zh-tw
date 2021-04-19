---
description: 指定是否在網路來源中啟用 Real-Time 串流通訊協定 (RTSP) 傳輸。
ms.assetid: 299393d2-7949-48ef-a36d-19bb8760fc4e
title: 'MFNETSOURCE_ENABLE_RTSP 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac191e6e244a8e341fef0dccd274293f09846aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974092"
---
# <a name="mfnetsource_enable_rtsp-property"></a><span data-ttu-id="54461-103">MFNETSOURCE \_ ENABLE \_ RTSP 屬性</span><span class="sxs-lookup"><span data-stu-id="54461-103">MFNETSOURCE\_ENABLE\_RTSP property</span></span>

<span data-ttu-id="54461-104">指定是否在網路來源中啟用 Real-Time 串流通訊協定 (RTSP) 傳輸。</span><span class="sxs-lookup"><span data-stu-id="54461-104">Specifies whether Real-Time Streaming Protocol (RTSP) transport is enabled in the network source.</span></span>



<span data-ttu-id="54461-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="54461-105">Data type</span></span>

<span data-ttu-id="54461-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="54461-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="54461-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="54461-107">PROPVARIANT member</span></span>

<span data-ttu-id="54461-108">布林 (**LONG**) </span><span class="sxs-lookup"><span data-stu-id="54461-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="54461-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="54461-109">VT\_I4</span></span>

<span data-ttu-id="54461-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="54461-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="54461-111">備註</span><span class="sxs-lookup"><span data-stu-id="54461-111">Remarks</span></span>

<span data-ttu-id="54461-112">常數 **MFNETSOURCE \_ ENABLE \_ RTSP** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="54461-112">The constant **MFNETSOURCE\_ENABLE\_RTSP** defines the GUID for this property key.</span></span> <span data-ttu-id="54461-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="54461-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="54461-114">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="54461-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="54461-115">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="54461-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="54461-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="54461-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54461-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="54461-117">Requirements</span></span>



| <span data-ttu-id="54461-118">需求</span><span class="sxs-lookup"><span data-stu-id="54461-118">Requirement</span></span> | <span data-ttu-id="54461-119">值</span><span class="sxs-lookup"><span data-stu-id="54461-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54461-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54461-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54461-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54461-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="54461-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54461-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54461-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54461-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="54461-124">標頭</span><span class="sxs-lookup"><span data-stu-id="54461-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="54461-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="54461-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54461-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54461-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54461-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="54461-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="54461-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="54461-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="54461-129">支援的通訊協定</span><span class="sxs-lookup"><span data-stu-id="54461-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




