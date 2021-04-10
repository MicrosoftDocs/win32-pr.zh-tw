---
description: 儲存位元組陣列，表示與位元組資料流程相關聯的 DRM 授權。
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: 'MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691240"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a><span data-ttu-id="b78d7-103">MFNETSOURCE \_ DRMNET \_ 授權 \_ 表示屬性</span><span class="sxs-lookup"><span data-stu-id="b78d7-103">MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION property</span></span>

<span data-ttu-id="b78d7-104">儲存位元組陣列，表示與位元組資料流程相關聯的 DRM 授權。</span><span class="sxs-lookup"><span data-stu-id="b78d7-104">Stores an array of bytes that represents the DRM license associated with the byte stream.</span></span>



<span data-ttu-id="b78d7-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b78d7-105">Data type</span></span>

<span data-ttu-id="b78d7-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="b78d7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b78d7-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="b78d7-107">PROPVARIANT member</span></span>

<span data-ttu-id="b78d7-108"> (**BLOB** 的位元組陣列) </span><span class="sxs-lookup"><span data-stu-id="b78d7-108">Byte array (**BLOB**)</span></span>

<span data-ttu-id="b78d7-109">VT \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="b78d7-109">VT\_BLOB</span></span>

<span data-ttu-id="b78d7-110">**blob**</span><span class="sxs-lookup"><span data-stu-id="b78d7-110">**blob**</span></span>



## <a name="remarks"></a><span data-ttu-id="b78d7-111">備註</span><span class="sxs-lookup"><span data-stu-id="b78d7-111">Remarks</span></span>

<span data-ttu-id="b78d7-112">常數 **MFNETSOURCE \_ DRMNET \_ 授權 \_ 表示** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b78d7-112">The constant **MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION** defines the GUID for this property key.</span></span> <span data-ttu-id="b78d7-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="b78d7-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="b78d7-114">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="b78d7-114">This property is read-only.</span></span> <span data-ttu-id="b78d7-115">若要從網路位元組資料流程取得屬性值，請呼叫 **IPropertyStore：： GetValue** ，並在 *key* 參數中傳遞 **PROPERTYKEY** 結構。</span><span class="sxs-lookup"><span data-stu-id="b78d7-115">To get the property value from the network byte stream, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="b78d7-116">**PROPERTYKEY** 的 **fmtid** 成員必須設定為屬性 GUID。</span><span class="sxs-lookup"><span data-stu-id="b78d7-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="b78d7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b78d7-117">Requirements</span></span>



| <span data-ttu-id="b78d7-118">需求</span><span class="sxs-lookup"><span data-stu-id="b78d7-118">Requirement</span></span> | <span data-ttu-id="b78d7-119">值</span><span class="sxs-lookup"><span data-stu-id="b78d7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b78d7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b78d7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b78d7-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b78d7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b78d7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b78d7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b78d7-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b78d7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b78d7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b78d7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b78d7-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b78d7-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b78d7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b78d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78d7-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="b78d7-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b78d7-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="b78d7-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




