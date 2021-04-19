---
description: ITMedia 介面是會話描述項通訊協定 (SDP 中媒體的標記法，請參閱 RFC 2327) 。
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: 'ITMedia 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982662"
---
# <a name="itmedia-interface"></a><span data-ttu-id="93123-103">ITMedia 介面</span><span class="sxs-lookup"><span data-stu-id="93123-103">ITMedia interface</span></span>

<span data-ttu-id="93123-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="93123-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="93123-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="93123-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="93123-106">**ITMedia** 介面是會話描述項通訊協定 (SDP 中媒體的標記法，請參閱 RFC 2327) 。</span><span class="sxs-lookup"><span data-stu-id="93123-106">The **ITMedia** interface is a representation of media in a Session Descriptor Protocol (SDP, see RFC 2327).</span></span> <span data-ttu-id="93123-107">此介面會匯出方法來取得和設定基本媒體屬性，例如類型。</span><span class="sxs-lookup"><span data-stu-id="93123-107">This interface exports methods to get and set basic media properties, such as type.</span></span> <span data-ttu-id="93123-108">[**ITMediaCollection：： get \_ 專案**](itmediacollection-get-item.md)和 [**ITMediaCollection：： Create**](itmediacollection-create.md)方法會建立 **ITMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="93123-108">The [**ITMediaCollection::get\_Item**](itmediacollection-get-item.md) and [**ITMediaCollection::Create**](itmediacollection-create.md) methods create the **ITMedia** interface.</span></span>

## <a name="members"></a><span data-ttu-id="93123-109">成員</span><span class="sxs-lookup"><span data-stu-id="93123-109">Members</span></span>

<span data-ttu-id="93123-110">**ITMedia** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="93123-110">The **ITMedia** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="93123-111">**ITMedia** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="93123-111">**ITMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="93123-112">方法</span><span class="sxs-lookup"><span data-stu-id="93123-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="93123-113">方法</span><span class="sxs-lookup"><span data-stu-id="93123-113">Methods</span></span>

<span data-ttu-id="93123-114">**ITMedia** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="93123-114">The **ITMedia** interface has these methods.</span></span>



| <span data-ttu-id="93123-115">方法</span><span class="sxs-lookup"><span data-stu-id="93123-115">Method</span></span>                                                          | <span data-ttu-id="93123-116">描述</span><span class="sxs-lookup"><span data-stu-id="93123-116">Description</span></span>                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93123-117">**取得 \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="93123-117">**get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)             | <span data-ttu-id="93123-118">取得媒體承載格式碼的清單。</span><span class="sxs-lookup"><span data-stu-id="93123-118">Gets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="93123-119">**取得 \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="93123-119">**get\_MediaName**</span></span>](itmedia-get-medianame.md)                 | <span data-ttu-id="93123-120">取得媒體名稱。</span><span class="sxs-lookup"><span data-stu-id="93123-120">Gets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="93123-121">**取得 \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="93123-121">**get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)               | <span data-ttu-id="93123-122">取得媒體標題。</span><span class="sxs-lookup"><span data-stu-id="93123-122">Gets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="93123-123">**取得 \_ NumPorts**</span><span class="sxs-lookup"><span data-stu-id="93123-123">**get\_NumPorts**</span></span>](itmedia-get-numports.md)                   | <span data-ttu-id="93123-124">取得會話所需的埠數目。</span><span class="sxs-lookup"><span data-stu-id="93123-124">Gets the number of ports needed for the session.</span></span><br/>                                      |
| [<span data-ttu-id="93123-125">**取得 \_ StartPort**</span><span class="sxs-lookup"><span data-stu-id="93123-125">**get\_StartPort**</span></span>](itmedia-get-startport.md)                 | <span data-ttu-id="93123-126">取得第一個埠的16位埠值。</span><span class="sxs-lookup"><span data-stu-id="93123-126">Gets the 16-bit port value for the first port.</span></span><br/>                                        |
| [<span data-ttu-id="93123-127">**取得 \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="93123-127">**get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md) | <span data-ttu-id="93123-128">取得傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="93123-128">Gets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="93123-129">**put \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="93123-129">**put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)             | <span data-ttu-id="93123-130">設定媒體承載格式代碼的清單。</span><span class="sxs-lookup"><span data-stu-id="93123-130">Sets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="93123-131">**put \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="93123-131">**put\_MediaName**</span></span>](itmedia-put-medianame.md)                 | <span data-ttu-id="93123-132">設定媒體名稱。</span><span class="sxs-lookup"><span data-stu-id="93123-132">Sets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="93123-133">**put \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="93123-133">**put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)               | <span data-ttu-id="93123-134">設定媒體標題。</span><span class="sxs-lookup"><span data-stu-id="93123-134">Sets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="93123-135">**put \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="93123-135">**put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md) | <span data-ttu-id="93123-136">設定傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="93123-136">Sets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="93123-137">**SetPortInfo**</span><span class="sxs-lookup"><span data-stu-id="93123-137">**SetPortInfo**</span></span>](itmedia-setportinfo.md)                      | <span data-ttu-id="93123-138">設定第一個埠的16位埠值，以及會話所需的埠數目。</span><span class="sxs-lookup"><span data-stu-id="93123-138">Sets the 16-bit port value for the first port and number of ports needed for session.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="93123-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="93123-139">Requirements</span></span>



| <span data-ttu-id="93123-140">需求</span><span class="sxs-lookup"><span data-stu-id="93123-140">Requirement</span></span> | <span data-ttu-id="93123-141">值</span><span class="sxs-lookup"><span data-stu-id="93123-141">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93123-142">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="93123-142">TAPI version</span></span><br/> | <span data-ttu-id="93123-143">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="93123-143">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="93123-144">標頭</span><span class="sxs-lookup"><span data-stu-id="93123-144">Header</span></span><br/>       | <dl> <span data-ttu-id="93123-145"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="93123-145"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="93123-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="93123-146">Library</span></span><br/>      | <dl> <span data-ttu-id="93123-147"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="93123-147"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="93123-148">DLL</span><span class="sxs-lookup"><span data-stu-id="93123-148">DLL</span></span><br/>          | <dl> <span data-ttu-id="93123-149"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93123-149"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93123-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93123-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93123-151">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="93123-151">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="93123-152">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="93123-152">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="93123-153">**ITSDP**</span><span class="sxs-lookup"><span data-stu-id="93123-153">**ITSDP**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="93123-154">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="93123-154">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

