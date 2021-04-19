---
description: 網路來源嘗試重新連線到網路的次數。
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: 'MFNETSOURCE_AUTORECONNECTPROGRESS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ade09bd425988cb0a64b258ff0887f8e79d4c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984181"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a><span data-ttu-id="6594c-103">MFNETSOURCE \_ AUTORECONNECTPROGRESS 屬性</span><span class="sxs-lookup"><span data-stu-id="6594c-103">MFNETSOURCE\_AUTORECONNECTPROGRESS property</span></span>

<span data-ttu-id="6594c-104">網路來源嘗試重新連線到網路的次數。</span><span class="sxs-lookup"><span data-stu-id="6594c-104">The number of times the network source has attempted to reconnect to the network.</span></span>



<span data-ttu-id="6594c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6594c-105">Data type</span></span>

<span data-ttu-id="6594c-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="6594c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6594c-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="6594c-107">PROPVARIANT member</span></span>

<span data-ttu-id="6594c-108">**DWORD** (儲存為 **LONG**) </span><span class="sxs-lookup"><span data-stu-id="6594c-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="6594c-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6594c-109">VT\_I4</span></span>

<span data-ttu-id="6594c-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="6594c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6594c-111">備註</span><span class="sxs-lookup"><span data-stu-id="6594c-111">Remarks</span></span>

<span data-ttu-id="6594c-112">常數 **MFNETSOURCE \_ AUTORECONNECTPROGRESS** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="6594c-112">The constant **MFNETSOURCE\_AUTORECONNECTPROGRESS** defines the GUID for this property key.</span></span> <span data-ttu-id="6594c-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="6594c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6594c-114">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="6594c-114">This property is read-only.</span></span> <span data-ttu-id="6594c-115">若要取得這個屬性，請查詢 **IPropertyStore** 介面的網路來源，然後呼叫 **IPropertyStore：： GetValue**。</span><span class="sxs-lookup"><span data-stu-id="6594c-115">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6594c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6594c-116">Requirements</span></span>



| <span data-ttu-id="6594c-117">需求</span><span class="sxs-lookup"><span data-stu-id="6594c-117">Requirement</span></span> | <span data-ttu-id="6594c-118">值</span><span class="sxs-lookup"><span data-stu-id="6594c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6594c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6594c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6594c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6594c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6594c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6594c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6594c-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6594c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6594c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6594c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6594c-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6594c-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6594c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6594c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6594c-126">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="6594c-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6594c-127">網路來源功能</span><span class="sxs-lookup"><span data-stu-id="6594c-127">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="6594c-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="6594c-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




