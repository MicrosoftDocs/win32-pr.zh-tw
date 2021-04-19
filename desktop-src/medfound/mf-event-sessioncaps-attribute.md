---
description: 包含根據目前的簡報定義媒體會話功能的旗標。
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: 'MF_EVENT_SESSIONCAPS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981480"
---
# <a name="mf_event_sessioncaps-attribute"></a><span data-ttu-id="1367c-103">MF \_ 事件 \_ SESSIONCAPS 屬性</span><span class="sxs-lookup"><span data-stu-id="1367c-103">MF\_EVENT\_SESSIONCAPS attribute</span></span>

<span data-ttu-id="1367c-104">包含根據目前的簡報定義媒體會話功能的旗標。</span><span class="sxs-lookup"><span data-stu-id="1367c-104">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="1367c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="1367c-105">Data type</span></span>

<span data-ttu-id="1367c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1367c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1367c-107">備註</span><span class="sxs-lookup"><span data-stu-id="1367c-107">Remarks</span></span>

<span data-ttu-id="1367c-108">這個屬性包含零或多個旗標的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="1367c-108">This attribute contains a bitwise **OR** of zero or more flags.</span></span> <span data-ttu-id="1367c-109">如需可能旗標的清單，請參閱 [**IMFMediaSession：： GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities)。</span><span class="sxs-lookup"><span data-stu-id="1367c-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span>

<span data-ttu-id="1367c-110">這個屬性會與 [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) 事件一起使用。</span><span class="sxs-lookup"><span data-stu-id="1367c-110">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="1367c-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="1367c-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1367c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1367c-112">Requirements</span></span>



| <span data-ttu-id="1367c-113">需求</span><span class="sxs-lookup"><span data-stu-id="1367c-113">Requirement</span></span> | <span data-ttu-id="1367c-114">值</span><span class="sxs-lookup"><span data-stu-id="1367c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1367c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1367c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1367c-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1367c-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1367c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1367c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1367c-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1367c-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1367c-119">標頭</span><span class="sxs-lookup"><span data-stu-id="1367c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1367c-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1367c-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1367c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1367c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1367c-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1367c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1367c-123">事件屬性</span><span class="sxs-lookup"><span data-stu-id="1367c-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="1367c-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1367c-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1367c-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1367c-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




