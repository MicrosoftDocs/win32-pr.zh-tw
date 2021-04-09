---
description: '\#網路來源用於記錄的 &0034; c-playerversion&\# 0034; 欄位的值。'
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: 'MFNETSOURCE_PLAYERVERSION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695087"
---
# <a name="mfnetsource_playerversion-property"></a><span data-ttu-id="c5e57-103">MFNETSOURCE \_ PLAYERVERSION 屬性</span><span class="sxs-lookup"><span data-stu-id="c5e57-103">MFNETSOURCE\_PLAYERVERSION property</span></span>

<span data-ttu-id="c5e57-104">網路來源用來記錄的 "c-playerversion" 欄位值。</span><span class="sxs-lookup"><span data-stu-id="c5e57-104">The value of the "c-playerversion" field that the network source uses for logging.</span></span> <span data-ttu-id="c5e57-105">應用程式可以將此屬性設定為應用程式的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c5e57-105">Applications can set this property to the version number of the application.</span></span>



<span data-ttu-id="c5e57-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="c5e57-106">Data type</span></span>

<span data-ttu-id="c5e57-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="c5e57-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c5e57-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="c5e57-108">PROPVARIANT member</span></span>

<span data-ttu-id="c5e57-109">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="c5e57-109">**LONGLONG**</span></span>

<span data-ttu-id="c5e57-110">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="c5e57-110">VT\_I8</span></span>

<span data-ttu-id="c5e57-111">**hVal**</span><span class="sxs-lookup"><span data-stu-id="c5e57-111">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c5e57-112">備註</span><span class="sxs-lookup"><span data-stu-id="c5e57-112">Remarks</span></span>

<span data-ttu-id="c5e57-113">常數 **MFNETSOURCE \_ PLAYERVERSION** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="c5e57-113">The constant **MFNETSOURCE\_PLAYERVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="c5e57-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="c5e57-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="c5e57-115">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="c5e57-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="c5e57-116">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="c5e57-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="c5e57-117">如需詳細資訊，請參閱 [來源解析程式](source-resolver.md)。</span><span class="sxs-lookup"><span data-stu-id="c5e57-117">For more information, see [Source Resolver](source-resolver.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e57-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5e57-118">Requirements</span></span>



| <span data-ttu-id="c5e57-119">需求</span><span class="sxs-lookup"><span data-stu-id="c5e57-119">Requirement</span></span> | <span data-ttu-id="c5e57-120">值</span><span class="sxs-lookup"><span data-stu-id="c5e57-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e57-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5e57-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e57-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5e57-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c5e57-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5e57-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e57-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5e57-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c5e57-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c5e57-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5e57-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5e57-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5e57-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5e57-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e57-128">用戶端記錄</span><span class="sxs-lookup"><span data-stu-id="c5e57-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="c5e57-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="c5e57-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c5e57-130">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="c5e57-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




