---
description: 字串陣列，其中包含要傳送至記錄伺服器的參數。
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: 'MFNETSOURCE_LOGPARAMS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943780"
---
# <a name="mfnetsource_logparams-property"></a><span data-ttu-id="3c536-103">MFNETSOURCE \_ LOGPARAMS 屬性</span><span class="sxs-lookup"><span data-stu-id="3c536-103">MFNETSOURCE\_LOGPARAMS property</span></span>

<span data-ttu-id="3c536-104">字串陣列，其中包含要傳送至記錄伺服器的參數。</span><span class="sxs-lookup"><span data-stu-id="3c536-104">Array of strings with the parameters to send to the log server.</span></span>



<span data-ttu-id="3c536-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3c536-105">Data type</span></span>

<span data-ttu-id="3c536-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="3c536-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3c536-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="3c536-107">PROPVARIANT member</span></span>

<span data-ttu-id="3c536-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="3c536-108">\**WCHAR\** _</span></span>

<span data-ttu-id="3c536-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="3c536-109">VT\_LPWSTR</span></span>

<span data-ttu-id="3c536-110">_ *pwszVal*\*</span><span class="sxs-lookup"><span data-stu-id="3c536-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="3c536-111">備註</span><span class="sxs-lookup"><span data-stu-id="3c536-111">Remarks</span></span>

<span data-ttu-id="3c536-112">**MFNETSOURCE \_ LOGPARAMS** 常數會定義屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3c536-112">The **MFNETSOURCE\_LOGPARAMS** constant defines the GUID for the property key.</span></span> <span data-ttu-id="3c536-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="3c536-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="3c536-114">若要在網路來源上設定此屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="3c536-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="3c536-115">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="3c536-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c536-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c536-116">Requirements</span></span>



| <span data-ttu-id="3c536-117">需求</span><span class="sxs-lookup"><span data-stu-id="3c536-117">Requirement</span></span> | <span data-ttu-id="3c536-118">值</span><span class="sxs-lookup"><span data-stu-id="3c536-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c536-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c536-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c536-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c536-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3c536-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c536-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c536-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c536-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3c536-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3c536-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c536-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c536-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c536-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c536-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c536-126">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="3c536-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3c536-127">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="3c536-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




