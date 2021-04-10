---
description: '\#網路來源用於記錄的 &0034; c-hostexe&\# 0034; 欄位的值。'
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: 'MFNETSOURCE_HOSTEXE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ac786fe08ede556537703d2eb886b30be39207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694691"
---
# <a name="mfnetsource_hostexe-property"></a><span data-ttu-id="d85e5-103">MFNETSOURCE \_ HOSTEXE 屬性</span><span class="sxs-lookup"><span data-stu-id="d85e5-103">MFNETSOURCE\_HOSTEXE property</span></span>

<span data-ttu-id="d85e5-104">網路來源用來記錄的 "c-hostexe" 欄位值。</span><span class="sxs-lookup"><span data-stu-id="d85e5-104">The value of the "c-hostexe" field that the network source uses for logging.</span></span> <span data-ttu-id="d85e5-105">應用程式可以將此屬性設定為主應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d85e5-105">Applications can set this property to the name of the host application.</span></span> <span data-ttu-id="d85e5-106">例如，如果應用程式是裝載在網頁中，則此值可能是 "iexplore.exe"。</span><span class="sxs-lookup"><span data-stu-id="d85e5-106">For example, the value could be "iexplore.exe" if the application is hosted in a webpage.</span></span>



<span data-ttu-id="d85e5-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="d85e5-107">Data type</span></span>

<span data-ttu-id="d85e5-108">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="d85e5-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d85e5-109">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="d85e5-109">PROPVARIANT member</span></span>

<span data-ttu-id="d85e5-110">寬字元字串 (**WCHAR** \*) </span><span class="sxs-lookup"><span data-stu-id="d85e5-110">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="d85e5-111">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="d85e5-111">VT\_LPWSTR</span></span>

<span data-ttu-id="d85e5-112">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="d85e5-112">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d85e5-113">備註</span><span class="sxs-lookup"><span data-stu-id="d85e5-113">Remarks</span></span>

<span data-ttu-id="d85e5-114">常數 **MFNETSOURCE \_ HOSTEXE** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d85e5-114">The constant **MFNETSOURCE\_HOSTEXE** defines the GUID for this property key.</span></span> <span data-ttu-id="d85e5-115"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="d85e5-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d85e5-116">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="d85e5-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="d85e5-117">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="d85e5-117">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="d85e5-118">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="d85e5-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d85e5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d85e5-119">Requirements</span></span>



| <span data-ttu-id="d85e5-120">需求</span><span class="sxs-lookup"><span data-stu-id="d85e5-120">Requirement</span></span> | <span data-ttu-id="d85e5-121">值</span><span class="sxs-lookup"><span data-stu-id="d85e5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d85e5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d85e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d85e5-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d85e5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d85e5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d85e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d85e5-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d85e5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d85e5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d85e5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d85e5-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d85e5-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d85e5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d85e5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d85e5-129">用戶端記錄</span><span class="sxs-lookup"><span data-stu-id="d85e5-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="d85e5-130">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="d85e5-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d85e5-131">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="d85e5-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




