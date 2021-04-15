---
description: 指定網路來源所使用的控制通訊協定。
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: 'MFNETSOURCE_PROTOCOL 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188eeb1f6669544291f4dca95db8a4a45a50d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511313"
---
# <a name="mfnetsource_protocol-property"></a><span data-ttu-id="cefb9-103">MFNETSOURCE \_ 通訊協定屬性</span><span class="sxs-lookup"><span data-stu-id="cefb9-103">MFNETSOURCE\_PROTOCOL property</span></span>

<span data-ttu-id="cefb9-104">指定網路來源所使用的控制通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cefb9-104">Specifies the control protocol used by the network source.</span></span> <span data-ttu-id="cefb9-105">這個屬性的值是 [**MFNETSOURCE \_ 通訊協定 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="cefb9-105">The value of this property is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>



<span data-ttu-id="cefb9-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="cefb9-106">Data type</span></span>

<span data-ttu-id="cefb9-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="cefb9-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="cefb9-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="cefb9-108">PROPVARIANT member</span></span>

<span data-ttu-id="cefb9-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="cefb9-109">**LONG**</span></span>

<span data-ttu-id="cefb9-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cefb9-110">VT\_I4</span></span>

<span data-ttu-id="cefb9-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="cefb9-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="cefb9-112">備註</span><span class="sxs-lookup"><span data-stu-id="cefb9-112">Remarks</span></span>

<span data-ttu-id="cefb9-113">常數 **MFNETSOURCE \_ 通訊協定** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="cefb9-113">The constant **MFNETSOURCE\_PROTOCOL** defines the GUID for this property key.</span></span> <span data-ttu-id="cefb9-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="cefb9-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="cefb9-115">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="cefb9-115">This property is read-only.</span></span> <span data-ttu-id="cefb9-116">若要取得這個屬性，請查詢 **IPropertyStore** 介面的網路來源，然後呼叫 **IPropertyStore：： GetValue**。</span><span class="sxs-lookup"><span data-stu-id="cefb9-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cefb9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="cefb9-117">Requirements</span></span>



| <span data-ttu-id="cefb9-118">需求</span><span class="sxs-lookup"><span data-stu-id="cefb9-118">Requirement</span></span> | <span data-ttu-id="cefb9-119">值</span><span class="sxs-lookup"><span data-stu-id="cefb9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cefb9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cefb9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cefb9-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cefb9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cefb9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cefb9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cefb9-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cefb9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cefb9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="cefb9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cefb9-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cefb9-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cefb9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cefb9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cefb9-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="cefb9-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="cefb9-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="cefb9-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="cefb9-129">支援的通訊協定</span><span class="sxs-lookup"><span data-stu-id="cefb9-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




