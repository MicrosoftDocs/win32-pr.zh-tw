---
description: 伺服器用來識別用戶端的唯一識別碼。
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: 'MFNETSOURCE_CLIENTGUID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114001"
---
# <a name="mfnetsource_clientguid-property"></a><span data-ttu-id="52baf-103">MFNETSOURCE \_ CLIENTGUID 屬性</span><span class="sxs-lookup"><span data-stu-id="52baf-103">MFNETSOURCE\_CLIENTGUID property</span></span>

<span data-ttu-id="52baf-104">伺服器用來識別用戶端的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="52baf-104">Unique identifier by which the server identifies the client.</span></span>



<span data-ttu-id="52baf-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="52baf-105">Data type</span></span>

<span data-ttu-id="52baf-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="52baf-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="52baf-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="52baf-107">PROPVARIANT member</span></span>

<span data-ttu-id="52baf-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="52baf-108">**GUID**</span></span>

<span data-ttu-id="52baf-109">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="52baf-109">VT\_CLSID</span></span>

<span data-ttu-id="52baf-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="52baf-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="52baf-111">備註</span><span class="sxs-lookup"><span data-stu-id="52baf-111">Remarks</span></span>

<span data-ttu-id="52baf-112">**MFNETSOURCE \_ CLIENTGUID** 常數會定義屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="52baf-112">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="52baf-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="52baf-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="52baf-114">若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="52baf-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="52baf-115">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="52baf-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="52baf-116">如果未設定或設定為 **GUID \_ Null**，Microsoft 媒體基礎會產生每個會話的匿名 GUID，以確保使用者的隱私權。</span><span class="sxs-lookup"><span data-stu-id="52baf-116">If not set or set as **GUID\_NULL**, Microsoft Media Foundation generates an anonymous GUID per session that ensures the user's privacy.</span></span>

## <a name="requirements"></a><span data-ttu-id="52baf-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="52baf-117">Requirements</span></span>



| <span data-ttu-id="52baf-118">需求</span><span class="sxs-lookup"><span data-stu-id="52baf-118">Requirement</span></span> | <span data-ttu-id="52baf-119">值</span><span class="sxs-lookup"><span data-stu-id="52baf-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52baf-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52baf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="52baf-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52baf-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="52baf-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52baf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="52baf-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52baf-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="52baf-124">標頭</span><span class="sxs-lookup"><span data-stu-id="52baf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="52baf-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="52baf-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52baf-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52baf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52baf-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="52baf-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="52baf-128">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="52baf-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




