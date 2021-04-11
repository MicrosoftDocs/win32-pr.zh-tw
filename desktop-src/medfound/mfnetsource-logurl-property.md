---
description: 網路來源將傳送記錄資訊的 Url 清單。
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: 'MFNETSOURCE_LOGURL 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113665"
---
# <a name="mfnetsource_logurl-property"></a><span data-ttu-id="b4c44-103">MFNETSOURCE \_ LOGURL 屬性</span><span class="sxs-lookup"><span data-stu-id="b4c44-103">MFNETSOURCE\_LOGURL property</span></span>

<span data-ttu-id="b4c44-104">網路來源將傳送記錄資訊的 Url 清單。</span><span class="sxs-lookup"><span data-stu-id="b4c44-104">List of URLs to which the network source will send logging information.</span></span>



<span data-ttu-id="b4c44-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b4c44-105">Data type</span></span>

<span data-ttu-id="b4c44-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="b4c44-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b4c44-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="b4c44-107">PROPVARIANT member</span></span>

<span data-ttu-id="b4c44-108">寬字元字串的陣列 (**CALPWSTR**) </span><span class="sxs-lookup"><span data-stu-id="b4c44-108">Array of wide-character strings (**CALPWSTR**)</span></span>

<span data-ttu-id="b4c44-109">VT \_ 向量 \| VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="b4c44-109">VT\_VECTOR \| VT\_LPWSTR</span></span>

<span data-ttu-id="b4c44-110">**calpwstr**</span><span class="sxs-lookup"><span data-stu-id="b4c44-110">**calpwstr**</span></span>



## <a name="remarks"></a><span data-ttu-id="b4c44-111">備註</span><span class="sxs-lookup"><span data-stu-id="b4c44-111">Remarks</span></span>

<span data-ttu-id="b4c44-112">常數 **MFNETSOURCE \_ LOGURL** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b4c44-112">The constant **MFNETSOURCE\_LOGURL** defines the GUID for this property key.</span></span> <span data-ttu-id="b4c44-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="b4c44-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="b4c44-114">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="b4c44-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="b4c44-115">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="b4c44-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="b4c44-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="b4c44-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c44-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4c44-117">Requirements</span></span>



| <span data-ttu-id="b4c44-118">需求</span><span class="sxs-lookup"><span data-stu-id="b4c44-118">Requirement</span></span> | <span data-ttu-id="b4c44-119">值</span><span class="sxs-lookup"><span data-stu-id="b4c44-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c44-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4c44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b4c44-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4c44-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b4c44-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4c44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b4c44-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4c44-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b4c44-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b4c44-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4c44-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4c44-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4c44-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4c44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c44-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="b4c44-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b4c44-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="b4c44-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




