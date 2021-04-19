---
description: ITConnection 介面功能如下所示。
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: 'ITConnection 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981403"
---
# <a name="itconnection-interface"></a><span data-ttu-id="1ca6b-103">ITConnection 介面</span><span class="sxs-lookup"><span data-stu-id="1ca6b-103">ITConnection interface</span></span>

<span data-ttu-id="1ca6b-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1ca6b-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="1ca6b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1ca6b-106">**ITConnection** 介面提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="1ca6b-106">The **ITConnection** interface provides the following functionality:</span></span>

-   <span data-ttu-id="1ca6b-107">提供會話的位址和存留時間 (TTL) 資訊的存取權。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-107">Provides access to the address and time to live (TTL) information for the session.</span></span>
-   <span data-ttu-id="1ca6b-108">提供頻寬資訊的存取。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-108">Provides access to the bandwidth information.</span></span>
-   <span data-ttu-id="1ca6b-109">啟用加密金鑰的操作。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-109">Enables manipulation of the encryption key.</span></span>

<span data-ttu-id="1ca6b-110">**ITConnection** 介面是藉由在 [**ITConferenceBlob**](itconferenceblob.md)上呼叫 **QueryInterface** 來建立。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-110">The **ITConnection** interface is created by calling **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

## <a name="members"></a><span data-ttu-id="1ca6b-111">成員</span><span class="sxs-lookup"><span data-stu-id="1ca6b-111">Members</span></span>

<span data-ttu-id="1ca6b-112">**ITConnection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-112">The **ITConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1ca6b-113">**ITConnection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1ca6b-113">**ITConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="1ca6b-114">方法</span><span class="sxs-lookup"><span data-stu-id="1ca6b-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1ca6b-115">方法</span><span class="sxs-lookup"><span data-stu-id="1ca6b-115">Methods</span></span>

<span data-ttu-id="1ca6b-116">**ITConnection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-116">The **ITConnection** interface has these methods.</span></span>



| <span data-ttu-id="1ca6b-117">方法</span><span class="sxs-lookup"><span data-stu-id="1ca6b-117">Method</span></span>                                                               | <span data-ttu-id="1ca6b-118">描述</span><span class="sxs-lookup"><span data-stu-id="1ca6b-118">Description</span></span>                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ca6b-119">**取得 \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-119">**get\_AddressType**</span></span>](itconnection-get-addresstype.md)             | <span data-ttu-id="1ca6b-120">取得網址類別型。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-120">Gets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="1ca6b-121">**取得 \_ 頻寬**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-121">**get\_Bandwidth**</span></span>](itconnection-get-bandwidth.md)                 | <span data-ttu-id="1ca6b-122">取得頻寬值。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-122">Gets bandwidth value.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="1ca6b-123">**取得 \_ BandwidthModifier**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-123">**get\_BandwidthModifier**</span></span>](itconnection-get-bandwidthmodifier.md) | <span data-ttu-id="1ca6b-124">取得頻寬修飾詞。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-124">Gets the bandwidth modifier.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="1ca6b-125">**取得 \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-125">**get\_NetworkType**</span></span>](itconnection-get-networktype.md)             | <span data-ttu-id="1ca6b-126">取得網路類型。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-126">Gets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="1ca6b-127">**取得 \_ NumAddresses**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-127">**get\_NumAddresses**</span></span>](itconnection-get-numaddresses.md)           | <span data-ttu-id="1ca6b-128">取得要用於會話的位址數目。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-128">Gets the number of addresses to be used for the session.</span></span><br/>                                                                            |
| [<span data-ttu-id="1ca6b-129">**取得 \_ StartAddress**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-129">**get\_StartAddress**</span></span>](itconnection-get-startaddress.md)           | <span data-ttu-id="1ca6b-130">取得要用於會話的第一個位址。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-130">Gets the first address to be used for the session.</span></span><br/>                                                                                  |
| [<span data-ttu-id="1ca6b-131">**取得 \_ Ttl**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-131">**get\_Ttl**</span></span>](itconnection-get-ttl.md)                             | <span data-ttu-id="1ca6b-132">取得位址上傳輸 (TTL) 範圍的 [*存留時間*](t-tapgloss.md) 。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-132">Gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span><br/> |
| [<span data-ttu-id="1ca6b-133">**GetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-133">**GetEncryptionKey**</span></span>](itconnection-getencryptionkey.md)            | <span data-ttu-id="1ca6b-134">取得加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-134">Gets the encryption key.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="1ca6b-135">**put \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-135">**put\_AddressType**</span></span>](itconnection-put-addresstype.md)             | <span data-ttu-id="1ca6b-136">設定網址類別型。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-136">Sets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="1ca6b-137">**put \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-137">**put\_NetworkType**</span></span>](itconnection-put-networktype.md)             | <span data-ttu-id="1ca6b-138">設定網路類型。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-138">Sets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="1ca6b-139">**SetAddressInfo**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-139">**SetAddressInfo**</span></span>](itconnection-setaddressinfo.md)                | <span data-ttu-id="1ca6b-140">設定位址資訊。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-140">Sets address information.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="1ca6b-141">**SetBandwidthInfo**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-141">**SetBandwidthInfo**</span></span>](itconnection-setbandwidthinfo.md)            | <span data-ttu-id="1ca6b-142">設定頻寬值。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-142">Sets the bandwidth value.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="1ca6b-143">**SetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="1ca6b-143">**SetEncryptionKey**</span></span>](itconnection-setencryptionkey.md)            | <span data-ttu-id="1ca6b-144">設定解密會話所需的加密金鑰，或用來取得以外部方式取得可用金鑰之機制的指示。</span><span class="sxs-lookup"><span data-stu-id="1ca6b-144">Sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="1ca6b-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ca6b-145">Requirements</span></span>



| <span data-ttu-id="1ca6b-146">需求</span><span class="sxs-lookup"><span data-stu-id="1ca6b-146">Requirement</span></span> | <span data-ttu-id="1ca6b-147">值</span><span class="sxs-lookup"><span data-stu-id="1ca6b-147">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca6b-148">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="1ca6b-148">TAPI version</span></span><br/> | <span data-ttu-id="1ca6b-149">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1ca6b-149">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1ca6b-150">標頭</span><span class="sxs-lookup"><span data-stu-id="1ca6b-150">Header</span></span><br/>       | <dl> <span data-ttu-id="1ca6b-151"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ca6b-151"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ca6b-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ca6b-152">Library</span></span><br/>      | <dl> <span data-ttu-id="1ca6b-153"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="1ca6b-153"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1ca6b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="1ca6b-154">DLL</span></span><br/>          | <dl> <span data-ttu-id="1ca6b-155"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ca6b-155"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

