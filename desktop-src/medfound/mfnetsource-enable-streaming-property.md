---
description: 指定是否啟用所有串流通訊協定。
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: 'MFNETSOURCE_ENABLE_STREAMING 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc8ae10dedd5cb904e43ee79ff64e8f451e37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512245"
---
# <a name="mfnetsource_enable_streaming-property"></a><span data-ttu-id="940a0-103">MFNETSOURCE \_ 啟用 \_ 串流屬性</span><span class="sxs-lookup"><span data-stu-id="940a0-103">MFNETSOURCE\_ENABLE\_STREAMING property</span></span>

<span data-ttu-id="940a0-104">指定是否啟用所有串流通訊協定。</span><span class="sxs-lookup"><span data-stu-id="940a0-104">Specifies whether all streaming protocols are enabled.</span></span>



<span data-ttu-id="940a0-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="940a0-105">Data type</span></span>

<span data-ttu-id="940a0-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="940a0-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="940a0-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="940a0-107">PROPVARIANT member</span></span>

<span data-ttu-id="940a0-108">布林 (**LONG**) </span><span class="sxs-lookup"><span data-stu-id="940a0-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="940a0-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="940a0-109">VT\_I4</span></span>

<span data-ttu-id="940a0-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="940a0-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="940a0-111">備註</span><span class="sxs-lookup"><span data-stu-id="940a0-111">Remarks</span></span>

<span data-ttu-id="940a0-112">常數 **MFNETSOURCE \_ 啟用 \_ 串流** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="940a0-112">The constant **MFNETSOURCE\_ENABLE\_STREAMING** defines the GUID for this property key.</span></span> <span data-ttu-id="940a0-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="940a0-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="940a0-114">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="940a0-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="940a0-115">若要設定屬性，請將 **IPropertyStore** 指標傳遞至設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="940a0-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="940a0-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="940a0-116">Requirements</span></span>



| <span data-ttu-id="940a0-117">需求</span><span class="sxs-lookup"><span data-stu-id="940a0-117">Requirement</span></span> | <span data-ttu-id="940a0-118">值</span><span class="sxs-lookup"><span data-stu-id="940a0-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="940a0-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="940a0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="940a0-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="940a0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="940a0-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="940a0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="940a0-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="940a0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="940a0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="940a0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="940a0-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="940a0-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="940a0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="940a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940a0-126">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="940a0-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="940a0-127">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="940a0-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="940a0-128">支援的通訊協定</span><span class="sxs-lookup"><span data-stu-id="940a0-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




