---
description: '\#網路來源用於記錄的 &0034; c-hostexever&\# 0034; 欄位的值。'
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: 'MFNETSOURCE_HOSTVERSION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469188"
---
# <a name="mfnetsource_hostversion-property"></a><span data-ttu-id="4c924-103">MFNETSOURCE \_ HOSTVERSION 屬性</span><span class="sxs-lookup"><span data-stu-id="4c924-103">MFNETSOURCE\_HOSTVERSION property</span></span>

<span data-ttu-id="4c924-104">網路來源用來記錄的 "c-hostexever" 欄位值。</span><span class="sxs-lookup"><span data-stu-id="4c924-104">The value of the "c-hostexever" field that the network source uses for logging.</span></span> <span data-ttu-id="4c924-105">應用程式可以將此屬性設定為主應用程式的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="4c924-105">Applications can set this property to the version number of the host application.</span></span> <span data-ttu-id="4c924-106">主應用程式是由 c-hostexe 欄位所識別的 .exe 檔案。</span><span class="sxs-lookup"><span data-stu-id="4c924-106">The host application is the .exe file identified by the c-hostexe field.</span></span>



<span data-ttu-id="4c924-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="4c924-107">Data type</span></span>

<span data-ttu-id="4c924-108">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="4c924-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4c924-109">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="4c924-109">PROPVARIANT member</span></span>

<span data-ttu-id="4c924-110">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="4c924-110">**LONGLONG**</span></span>

<span data-ttu-id="4c924-111">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="4c924-111">VT\_I8</span></span>

<span data-ttu-id="4c924-112">**hVal**</span><span class="sxs-lookup"><span data-stu-id="4c924-112">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="4c924-113">備註</span><span class="sxs-lookup"><span data-stu-id="4c924-113">Remarks</span></span>

<span data-ttu-id="4c924-114">常數 **MFNETSOURCE \_ HOSTVERSION** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4c924-114">The constant **MFNETSOURCE\_HOSTVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="4c924-115"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="4c924-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="4c924-116">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="4c924-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="4c924-117">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="4c924-117">To set the property, pass an **IPropertyStore** pointer to the Source resolver.</span></span> <span data-ttu-id="4c924-118">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="4c924-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c924-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c924-119">Requirements</span></span>



| <span data-ttu-id="4c924-120">需求</span><span class="sxs-lookup"><span data-stu-id="4c924-120">Requirement</span></span> | <span data-ttu-id="4c924-121">值</span><span class="sxs-lookup"><span data-stu-id="4c924-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c924-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c924-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4c924-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c924-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4c924-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c924-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4c924-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c924-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4c924-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4c924-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c924-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c924-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c924-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c924-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c924-129">用戶端記錄</span><span class="sxs-lookup"><span data-stu-id="4c924-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="4c924-130">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="4c924-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4c924-131">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="4c924-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




