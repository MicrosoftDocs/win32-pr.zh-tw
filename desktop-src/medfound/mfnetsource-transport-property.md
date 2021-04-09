---
description: 指定網路來源所使用的傳輸通訊協定。
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: 'MFNETSOURCE_TRANSPORT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd41653f2b5ea0686527af4d6ee8c8b9962005aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848310"
---
# <a name="mfnetsource_transport-property"></a><span data-ttu-id="15c7e-103">MFNETSOURCE \_ 傳輸屬性</span><span class="sxs-lookup"><span data-stu-id="15c7e-103">MFNETSOURCE\_TRANSPORT property</span></span>

<span data-ttu-id="15c7e-104">指定網路來源所使用的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="15c7e-104">Specifies the transport protocol used by the network source.</span></span> <span data-ttu-id="15c7e-105">這個屬性的值是 [**MFNETSOURCE \_ 傳輸 \_ 類型**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="15c7e-105">The value of this property is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>



<span data-ttu-id="15c7e-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="15c7e-106">Data type</span></span>

<span data-ttu-id="15c7e-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="15c7e-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="15c7e-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="15c7e-108">PROPVARIANT member</span></span>

<span data-ttu-id="15c7e-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="15c7e-109">**LONG**</span></span>

<span data-ttu-id="15c7e-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="15c7e-110">VT\_I4</span></span>

<span data-ttu-id="15c7e-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="15c7e-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="15c7e-112">備註</span><span class="sxs-lookup"><span data-stu-id="15c7e-112">Remarks</span></span>

<span data-ttu-id="15c7e-113">常數 **MFNETSOURCE \_ 傳輸** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="15c7e-113">The constant **MFNETSOURCE\_TRANSPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="15c7e-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="15c7e-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="15c7e-115">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="15c7e-115">This property is read-only.</span></span> <span data-ttu-id="15c7e-116">若要取得這個屬性，請查詢 **IPropertyStore** 介面的網路來源，然後呼叫 **IPropertyStore：： GetValue**。</span><span class="sxs-lookup"><span data-stu-id="15c7e-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c7e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="15c7e-117">Requirements</span></span>



| <span data-ttu-id="15c7e-118">需求</span><span class="sxs-lookup"><span data-stu-id="15c7e-118">Requirement</span></span> | <span data-ttu-id="15c7e-119">值</span><span class="sxs-lookup"><span data-stu-id="15c7e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15c7e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15c7e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="15c7e-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15c7e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="15c7e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15c7e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="15c7e-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15c7e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="15c7e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="15c7e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="15c7e-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="15c7e-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15c7e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15c7e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c7e-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="15c7e-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="15c7e-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="15c7e-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="15c7e-129">支援的通訊協定</span><span class="sxs-lookup"><span data-stu-id="15c7e-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




