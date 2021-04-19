---
description: ITStreamQualityControl 會公開方法，讓應用程式取得和設定 stream 品質控制項的參數。
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: 'ITStreamQualityControl 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990667"
---
# <a name="itstreamqualitycontrol-interface"></a><span data-ttu-id="55037-103">ITStreamQualityControl 介面</span><span class="sxs-lookup"><span data-stu-id="55037-103">ITStreamQualityControl interface</span></span>

<span data-ttu-id="55037-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。</span><span class="sxs-lookup"><span data-stu-id="55037-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="55037-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="55037-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="55037-106">**ITStreamQualityControl** 會公開方法，讓應用程式取得和設定 stream 品質控制項的參數。</span><span class="sxs-lookup"><span data-stu-id="55037-106">The **ITStreamQualityControl** exposes methods that allow an application to get and set parameters for stream quality control.</span></span>

<span data-ttu-id="55037-107">此介面是由 [IPCONF msp](ipconf-msp.md) 和 [H323 msp](h323-msp.md)所執行。</span><span class="sxs-lookup"><span data-stu-id="55037-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="55037-108">只有在呼叫使用這些服務提供者時，才會公開此服務提供者。</span><span class="sxs-lookup"><span data-stu-id="55037-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="55037-109">成員</span><span class="sxs-lookup"><span data-stu-id="55037-109">Members</span></span>

<span data-ttu-id="55037-110">**ITStreamQualityControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="55037-110">The **ITStreamQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="55037-111">**ITStreamQualityControl** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="55037-111">**ITStreamQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="55037-112">方法</span><span class="sxs-lookup"><span data-stu-id="55037-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="55037-113">方法</span><span class="sxs-lookup"><span data-stu-id="55037-113">Methods</span></span>

<span data-ttu-id="55037-114">**ITStreamQualityControl** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="55037-114">The **ITStreamQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="55037-115">方法</span><span class="sxs-lookup"><span data-stu-id="55037-115">Method</span></span>                                              | <span data-ttu-id="55037-116">描述</span><span class="sxs-lookup"><span data-stu-id="55037-116">Description</span></span>                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55037-117">**獲取**</span><span class="sxs-lookup"><span data-stu-id="55037-117">**Get**</span></span>](itstreamqualitycontrol-get.md)           | <span data-ttu-id="55037-118">取得指定之 [資料流程品質屬性](streamqualityproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="55037-118">Gets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="55037-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="55037-119">**GetRange**</span></span>](itstreamqualitycontrol-getrange.md) | <span data-ttu-id="55037-120">取得指定之 [資料流程品質屬性](streamqualityproperty.md)的有效值範圍。</span><span class="sxs-lookup"><span data-stu-id="55037-120">Gets the range of valid values for a given [stream quality property](streamqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="55037-121">**設定**</span><span class="sxs-lookup"><span data-stu-id="55037-121">**Set**</span></span>](itstreamqualitycontrol-set.md)           | <span data-ttu-id="55037-122">設定指定之 [資料流程品質屬性](streamqualityproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="55037-122">Sets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="55037-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="55037-123">Requirements</span></span>



| <span data-ttu-id="55037-124">需求</span><span class="sxs-lookup"><span data-stu-id="55037-124">Requirement</span></span> | <span data-ttu-id="55037-125">值</span><span class="sxs-lookup"><span data-stu-id="55037-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55037-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="55037-126">TAPI version</span></span><br/> | <span data-ttu-id="55037-127">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="55037-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="55037-128">標頭</span><span class="sxs-lookup"><span data-stu-id="55037-128">Header</span></span><br/>       | <dl> <span data-ttu-id="55037-129"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="55037-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="55037-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="55037-130">Library</span></span><br/>      | <dl> <span data-ttu-id="55037-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="55037-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="55037-132">DLL</span><span class="sxs-lookup"><span data-stu-id="55037-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="55037-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55037-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

