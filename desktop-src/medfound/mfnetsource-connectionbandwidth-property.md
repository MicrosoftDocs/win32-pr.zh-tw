---
description: 指定網路來源的連結頻寬（以位/秒為單位）。
ms.assetid: 1b71dce1-8744-4114-9629-2a9d0afb7c43
title: 'MFNETSOURCE_CONNECTIONBANDWIDTH 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b852b3eb8dbfe5d3abc85e2223e868c5be708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512249"
---
# <a name="mfnetsource_connectionbandwidth-property"></a><span data-ttu-id="fe908-103">MFNETSOURCE \_ CONNECTIONBANDWIDTH 屬性</span><span class="sxs-lookup"><span data-stu-id="fe908-103">MFNETSOURCE\_CONNECTIONBANDWIDTH property</span></span>

<span data-ttu-id="fe908-104">指定網路來源的連結頻寬（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="fe908-104">Specifies the link bandwidth for the network source, in bits per second.</span></span>



<span data-ttu-id="fe908-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="fe908-105">Data type</span></span>

<span data-ttu-id="fe908-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="fe908-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="fe908-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="fe908-107">PROPVARIANT member</span></span>

<span data-ttu-id="fe908-108">**DWORD** (儲存為 **LONG**) </span><span class="sxs-lookup"><span data-stu-id="fe908-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="fe908-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fe908-109">VT\_I4</span></span>

<span data-ttu-id="fe908-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="fe908-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="fe908-111">備註</span><span class="sxs-lookup"><span data-stu-id="fe908-111">Remarks</span></span>

<span data-ttu-id="fe908-112">常數 **MFNETSOURCE \_ CONNECTIONBANDWIDTH** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="fe908-112">The constant **MFNETSOURCE\_CONNECTIONBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="fe908-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="fe908-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="fe908-114">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="fe908-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="fe908-115">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="fe908-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="fe908-116">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="fe908-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe908-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe908-117">Requirements</span></span>



| <span data-ttu-id="fe908-118">需求</span><span class="sxs-lookup"><span data-stu-id="fe908-118">Requirement</span></span> | <span data-ttu-id="fe908-119">值</span><span class="sxs-lookup"><span data-stu-id="fe908-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe908-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe908-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe908-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe908-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fe908-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe908-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe908-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe908-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fe908-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fe908-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe908-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe908-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe908-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe908-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe908-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="fe908-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="fe908-128">網路來源功能</span><span class="sxs-lookup"><span data-stu-id="fe908-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="fe908-129">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="fe908-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




