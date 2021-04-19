---
description: IH323LineEx 介面是由 H323 MSP 所執行，而且僅適用于 .H 位址物件。 此介面會公開方法，以啟用 H323 和 SDP 用戶端間通訊的終端機建立和操作。
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: 'IH323LineEx 介面 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992991"
---
# <a name="ih323lineex-interface"></a><span data-ttu-id="dff15-104">IH323LineEx 介面</span><span class="sxs-lookup"><span data-stu-id="dff15-104">IH323LineEx interface</span></span>

<span data-ttu-id="dff15-105">\[**IH323LineEx** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="dff15-105">\[**IH323LineEx** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dff15-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="dff15-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dff15-107">**IH323LineEx** 介面是由 [H323 MSP](h323-msp.md)所執行，而且僅適用于 .h 位址物件。</span><span class="sxs-lookup"><span data-stu-id="dff15-107">The **IH323LineEx** interface is implemented by the [H323 MSP](h323-msp.md) and is available only on H.323 address objects.</span></span> <span data-ttu-id="dff15-108">此介面會公開方法，以啟用 H323 和 SDP 用戶端間通訊的終端機建立和操作。</span><span class="sxs-lookup"><span data-stu-id="dff15-108">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span>

> [!Note]  
> <span data-ttu-id="dff15-109">此介面中的所有方法都應該只在註冊此位址的撥入電話之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="dff15-109">All methods in this interface should be called only after registering for incoming calls on this address.</span></span>

 

## <a name="members"></a><span data-ttu-id="dff15-110">成員</span><span class="sxs-lookup"><span data-stu-id="dff15-110">Members</span></span>

<span data-ttu-id="dff15-111">**IH323LineEx** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="dff15-111">The **IH323LineEx** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dff15-112">**IH323LineEx** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dff15-112">**IH323LineEx** also has these types of members:</span></span>

-   [<span data-ttu-id="dff15-113">方法</span><span class="sxs-lookup"><span data-stu-id="dff15-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dff15-114">方法</span><span class="sxs-lookup"><span data-stu-id="dff15-114">Methods</span></span>

<span data-ttu-id="dff15-115">**IH323LineEx** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dff15-115">The **IH323LineEx** interface has these methods.</span></span>



| <span data-ttu-id="dff15-116">方法</span><span class="sxs-lookup"><span data-stu-id="dff15-116">Method</span></span>                                                                                 | <span data-ttu-id="dff15-117">描述</span><span class="sxs-lookup"><span data-stu-id="dff15-117">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="dff15-118">**SetAlias**</span><span class="sxs-lookup"><span data-stu-id="dff15-118">**SetAlias**</span></span>](ih323lineex-setalias.md)                                               | <span data-ttu-id="dff15-119">為位址設定預設的 H. 323 別名。</span><span class="sxs-lookup"><span data-stu-id="dff15-119">Configures a default H.323 alias for the address.</span></span><br/>             |
| [<span data-ttu-id="dff15-120">**SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="dff15-120">**SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md) | <span data-ttu-id="dff15-121">設定預設功能的喜好設定加權。</span><span class="sxs-lookup"><span data-stu-id="dff15-121">Configures the preference weighting for default capabilities.</span></span><br/> |
| [<span data-ttu-id="dff15-122">**SetExternalT120Address**</span><span class="sxs-lookup"><span data-stu-id="dff15-122">**SetExternalT120Address**</span></span>](ih323lineex-setexternalt120address.md)                   | <span data-ttu-id="dff15-123">為數據交換設定外部的 T. 120 位址。</span><span class="sxs-lookup"><span data-stu-id="dff15-123">Configures an external T.120 address for data exchange.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="dff15-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="dff15-124">Requirements</span></span>



| <span data-ttu-id="dff15-125">需求</span><span class="sxs-lookup"><span data-stu-id="dff15-125">Requirement</span></span> | <span data-ttu-id="dff15-126">值</span><span class="sxs-lookup"><span data-stu-id="dff15-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dff15-127">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="dff15-127">TAPI version</span></span><br/> | <span data-ttu-id="dff15-128">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="dff15-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dff15-129">標頭</span><span class="sxs-lookup"><span data-stu-id="dff15-129">Header</span></span><br/>       | <dl> <span data-ttu-id="dff15-130"><dt>H323priv。h</dt></span><span class="sxs-lookup"><span data-stu-id="dff15-130"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="dff15-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="dff15-131">Library</span></span><br/>      | <dl> <span data-ttu-id="dff15-132"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="dff15-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dff15-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dff15-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="dff15-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dff15-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dff15-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dff15-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff15-136">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="dff15-136">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

