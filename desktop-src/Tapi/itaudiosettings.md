---
description: ITAudioSettings 介面會公開方法，讓應用程式取得並設定參數來控制音訊裝置。
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: 'ITAudioSettings 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997023"
---
# <a name="itaudiosettings-interface"></a><span data-ttu-id="9b7c1-103">ITAudioSettings 介面</span><span class="sxs-lookup"><span data-stu-id="9b7c1-103">ITAudioSettings interface</span></span>

<span data-ttu-id="9b7c1-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。</span><span class="sxs-lookup"><span data-stu-id="9b7c1-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9b7c1-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="9b7c1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9b7c1-106">**ITAudioSettings** 介面會公開方法，讓應用程式取得並設定參數來控制音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="9b7c1-106">The **ITAudioSettings** interface exposes methods that allow an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="9b7c1-107">此介面是由 [IPCONF msp](ipconf-msp.md) 和 [H323 msp](h323-msp.md)所執行。</span><span class="sxs-lookup"><span data-stu-id="9b7c1-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="9b7c1-108">只有在呼叫使用這些服務提供者時，才會公開此服務提供者。</span><span class="sxs-lookup"><span data-stu-id="9b7c1-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="9b7c1-109">成員</span><span class="sxs-lookup"><span data-stu-id="9b7c1-109">Members</span></span>

<span data-ttu-id="9b7c1-110">**ITAudioSettings** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="9b7c1-110">The **ITAudioSettings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9b7c1-111">**ITAudioSettings** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9b7c1-111">**ITAudioSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="9b7c1-112">方法</span><span class="sxs-lookup"><span data-stu-id="9b7c1-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9b7c1-113">方法</span><span class="sxs-lookup"><span data-stu-id="9b7c1-113">Methods</span></span>

<span data-ttu-id="9b7c1-114">**ITAudioSettings** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9b7c1-114">The **ITAudioSettings** interface has these methods.</span></span>



| <span data-ttu-id="9b7c1-115">方法</span><span class="sxs-lookup"><span data-stu-id="9b7c1-115">Method</span></span>                                              | <span data-ttu-id="9b7c1-116">描述</span><span class="sxs-lookup"><span data-stu-id="9b7c1-116">Description</span></span>                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b7c1-117">**獲取**</span><span class="sxs-lookup"><span data-stu-id="9b7c1-117">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="9b7c1-118">取得指定之 [音訊設定屬性](audiosettingsproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="9b7c1-118">Gets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="9b7c1-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="9b7c1-119">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="9b7c1-120">取得指定之 [音訊設定屬性](audiosettingsproperty.md)的有效值範圍。</span><span class="sxs-lookup"><span data-stu-id="9b7c1-120">Gets the range of valid values for a given [audio setting property](audiosettingsproperty.md).</span></span><br/> |
| [<span data-ttu-id="9b7c1-121">**設定**</span><span class="sxs-lookup"><span data-stu-id="9b7c1-121">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="9b7c1-122">設定指定之 [音訊設定屬性](audiosettingsproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="9b7c1-122">Sets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="9b7c1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b7c1-123">Requirements</span></span>



| <span data-ttu-id="9b7c1-124">需求</span><span class="sxs-lookup"><span data-stu-id="9b7c1-124">Requirement</span></span> | <span data-ttu-id="9b7c1-125">值</span><span class="sxs-lookup"><span data-stu-id="9b7c1-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7c1-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="9b7c1-126">TAPI version</span></span><br/> | <span data-ttu-id="9b7c1-127">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="9b7c1-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="9b7c1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="9b7c1-128">Header</span></span><br/>       | <dl> <span data-ttu-id="9b7c1-129"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b7c1-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b7c1-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="9b7c1-130">Library</span></span><br/>      | <dl> <span data-ttu-id="9b7c1-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="9b7c1-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="9b7c1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9b7c1-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="9b7c1-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b7c1-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

