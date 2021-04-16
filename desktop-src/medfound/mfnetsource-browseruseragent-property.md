---
description: '\#網路來源用於記錄的 &0034; cs (使用者代理程式) &0034; 欄位的第一個部分值 \# 。'
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: 'MFNETSOURCE_BROWSERUSERAGENT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cbb4dcd5558c59da20e75209529c16fc0c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512252"
---
# <a name="mfnetsource_browseruseragent-property"></a><span data-ttu-id="a74eb-103">MFNETSOURCE \_ BROWSERUSERAGENT 屬性</span><span class="sxs-lookup"><span data-stu-id="a74eb-103">MFNETSOURCE\_BROWSERUSERAGENT property</span></span>

<span data-ttu-id="a74eb-104">網路來源用於記錄的 [cs (使用者代理程式) ] 欄位的第一個部分值。</span><span class="sxs-lookup"><span data-stu-id="a74eb-104">The value of the first portion of the "cs(User-Agent)" field that the network source uses for logging.</span></span> <span data-ttu-id="a74eb-105">應用程式可以將此屬性設定為任何字串值。</span><span class="sxs-lookup"><span data-stu-id="a74eb-105">Applications can set this property to any string value.</span></span>



<span data-ttu-id="a74eb-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="a74eb-106">Data type</span></span>

<span data-ttu-id="a74eb-107">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="a74eb-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a74eb-108">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="a74eb-108">PROPVARIANT member</span></span>

<span data-ttu-id="a74eb-109">寬字元字串 (**WCHAR** \*) </span><span class="sxs-lookup"><span data-stu-id="a74eb-109">Wide-character string (**WCHAR**\*)</span></span>

<span data-ttu-id="a74eb-110">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="a74eb-110">VT\_LPWSTR</span></span>

<span data-ttu-id="a74eb-111">**pwszVal**</span><span class="sxs-lookup"><span data-stu-id="a74eb-111">**pwszVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a74eb-112">備註</span><span class="sxs-lookup"><span data-stu-id="a74eb-112">Remarks</span></span>

<span data-ttu-id="a74eb-113">常數 **MFNETSOURCE \_ BROWSERUSERAGENT** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a74eb-113">The constant **MFNETSOURCE\_BROWSERUSERAGENT** defines the GUID for this property key.</span></span> <span data-ttu-id="a74eb-114"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="a74eb-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a74eb-115">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="a74eb-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="a74eb-116">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="a74eb-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a74eb-117">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="a74eb-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a74eb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a74eb-118">Requirements</span></span>



| <span data-ttu-id="a74eb-119">需求</span><span class="sxs-lookup"><span data-stu-id="a74eb-119">Requirement</span></span> | <span data-ttu-id="a74eb-120">值</span><span class="sxs-lookup"><span data-stu-id="a74eb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a74eb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a74eb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a74eb-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a74eb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a74eb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a74eb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a74eb-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a74eb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a74eb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a74eb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a74eb-126"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a74eb-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a74eb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a74eb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74eb-128">用戶端記錄</span><span class="sxs-lookup"><span data-stu-id="a74eb-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="a74eb-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="a74eb-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a74eb-130">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="a74eb-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a74eb-131">**MFNETSOURCE \_ PLAYERUSERAGENT**</span><span class="sxs-lookup"><span data-stu-id="a74eb-131">**MFNETSOURCE\_PLAYERUSERAGENT**</span></span>](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




