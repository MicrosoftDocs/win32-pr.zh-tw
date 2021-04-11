---
description: 設定 WTV 媒體來源的資料流程設定。
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: 'MFPKEY_SBESourceMode 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943908"
---
# <a name="mfpkey_sbesourcemode-property"></a><span data-ttu-id="bae9b-103">MFPKEY \_ SBESourceMode 屬性</span><span class="sxs-lookup"><span data-stu-id="bae9b-103">MFPKEY\_SBESourceMode property</span></span>

<span data-ttu-id="bae9b-104">設定 WTV 媒體來源的資料流程設定。</span><span class="sxs-lookup"><span data-stu-id="bae9b-104">Sets the stream configuration for the WTV media source.</span></span>



<span data-ttu-id="bae9b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="bae9b-105">Data type</span></span>

<span data-ttu-id="bae9b-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="bae9b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="bae9b-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="bae9b-107">PROPVARIANT member</span></span>

<span data-ttu-id="bae9b-108">**INT**</span><span class="sxs-lookup"><span data-stu-id="bae9b-108">**INT**</span></span>

<span data-ttu-id="bae9b-109">VT \_ INT</span><span class="sxs-lookup"><span data-stu-id="bae9b-109">VT\_INT</span></span>

<span data-ttu-id="bae9b-110">**intVal**</span><span class="sxs-lookup"><span data-stu-id="bae9b-110">**intVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="bae9b-111">備註</span><span class="sxs-lookup"><span data-stu-id="bae9b-111">Remarks</span></span>

<span data-ttu-id="bae9b-112">使用此屬性可設定 WTV 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="bae9b-112">Use this property to configure the WTV media source.</span></span> <span data-ttu-id="bae9b-113">若要設定屬性，請將 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="bae9b-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="bae9b-114">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="bae9b-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="bae9b-115">WTV 媒體來源會讀取 Windows 錄製的電視節目， ( WTV 和 winspool.drv) 檔。</span><span class="sxs-lookup"><span data-stu-id="bae9b-115">The WTV media source reads Windows Recorded TV Show (.wtv and .ms-drv) files.</span></span>

<span data-ttu-id="bae9b-116">這個屬性必須具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bae9b-116">This property must have one of the following values.</span></span>

-   <span data-ttu-id="bae9b-117">1：根據系統本機，將可用的音訊串流對應至單一輸出。</span><span class="sxs-lookup"><span data-stu-id="bae9b-117">1: Map available audio streams to a single output, based on the system local.</span></span> <span data-ttu-id="bae9b-118">此模式適用于播放。</span><span class="sxs-lookup"><span data-stu-id="bae9b-118">This mode is appropriate for playback.</span></span> <span data-ttu-id="bae9b-119">(預設值。)</span><span class="sxs-lookup"><span data-stu-id="bae9b-119">(Default.)</span></span>
-   2. <span data-ttu-id="bae9b-120">系統會選取所有音訊串流和子串流 (例如標題和資料流程) 。</span><span class="sxs-lookup"><span data-stu-id="bae9b-120">All audio streams and substreams (such as caption and data streams) are selected.</span></span> <span data-ttu-id="bae9b-121">此模式適用于 remuxing 或轉碼。</span><span class="sxs-lookup"><span data-stu-id="bae9b-121">This mode is appropriate for remuxing or transcoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="bae9b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="bae9b-122">Requirements</span></span>



| <span data-ttu-id="bae9b-123">需求</span><span class="sxs-lookup"><span data-stu-id="bae9b-123">Requirement</span></span> | <span data-ttu-id="bae9b-124">值</span><span class="sxs-lookup"><span data-stu-id="bae9b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bae9b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bae9b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bae9b-126">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bae9b-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="bae9b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bae9b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bae9b-128">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bae9b-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="bae9b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="bae9b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bae9b-130"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bae9b-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bae9b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bae9b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae9b-132">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="bae9b-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
