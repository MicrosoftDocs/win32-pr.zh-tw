---
description: ITCallQualityControl 介面會公開方法，讓應用程式取得和設定通話品質控制的參數。
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: 'ITCallQualityControl 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995938"
---
# <a name="itcallqualitycontrol-interface"></a><span data-ttu-id="24562-103">ITCallQualityControl 介面</span><span class="sxs-lookup"><span data-stu-id="24562-103">ITCallQualityControl interface</span></span>

<span data-ttu-id="24562-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。</span><span class="sxs-lookup"><span data-stu-id="24562-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="24562-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="24562-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="24562-106">**ITCallQualityControl** 介面會公開方法，讓應用程式取得和設定通話品質控制的參數。</span><span class="sxs-lookup"><span data-stu-id="24562-106">The **ITCallQualityControl** interface exposes methods that allow an application to get and set parameters for call quality control.</span></span>

<span data-ttu-id="24562-107">此介面是由 [IPCONF msp](ipconf-msp.md) 和 [H323 msp](h323-msp.md)所執行。</span><span class="sxs-lookup"><span data-stu-id="24562-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="24562-108">只有在呼叫使用這些服務提供者時，才會公開此服務提供者。</span><span class="sxs-lookup"><span data-stu-id="24562-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="24562-109">成員</span><span class="sxs-lookup"><span data-stu-id="24562-109">Members</span></span>

<span data-ttu-id="24562-110">**ITCallQualityControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="24562-110">The **ITCallQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="24562-111">**ITCallQualityControl** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="24562-111">**ITCallQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="24562-112">方法</span><span class="sxs-lookup"><span data-stu-id="24562-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="24562-113">方法</span><span class="sxs-lookup"><span data-stu-id="24562-113">Methods</span></span>

<span data-ttu-id="24562-114">**ITCallQualityControl** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="24562-114">The **ITCallQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="24562-115">方法</span><span class="sxs-lookup"><span data-stu-id="24562-115">Method</span></span>                                            | <span data-ttu-id="24562-116">描述</span><span class="sxs-lookup"><span data-stu-id="24562-116">Description</span></span>                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24562-117">**獲取**</span><span class="sxs-lookup"><span data-stu-id="24562-117">**Get**</span></span>](itcallqualitycontrol-get.md)           | <span data-ttu-id="24562-118">取得指定之 [通話品質控制項屬性](callqualityproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="24562-118">Gets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="24562-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="24562-119">**GetRange**</span></span>](itcallqualitycontrol-getrange.md) | <span data-ttu-id="24562-120">取得指定之 [呼叫品質控制項屬性](callqualityproperty.md)的有效值範圍。</span><span class="sxs-lookup"><span data-stu-id="24562-120">Gets the range of valid values for a given [call quality control property](callqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="24562-121">**設定**</span><span class="sxs-lookup"><span data-stu-id="24562-121">**Set**</span></span>](itcallqualitycontrol-set.md)           | <span data-ttu-id="24562-122">設定指定之 [通話品質控制項屬性](callqualityproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="24562-122">Sets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="24562-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="24562-123">Requirements</span></span>



| <span data-ttu-id="24562-124">需求</span><span class="sxs-lookup"><span data-stu-id="24562-124">Requirement</span></span> | <span data-ttu-id="24562-125">值</span><span class="sxs-lookup"><span data-stu-id="24562-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="24562-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="24562-126">TAPI version</span></span><br/> | <span data-ttu-id="24562-127">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="24562-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="24562-128">標頭</span><span class="sxs-lookup"><span data-stu-id="24562-128">Header</span></span><br/>       | <dl> <span data-ttu-id="24562-129"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="24562-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="24562-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="24562-130">Library</span></span><br/>      | <dl> <span data-ttu-id="24562-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="24562-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="24562-132">DLL</span><span class="sxs-lookup"><span data-stu-id="24562-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="24562-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24562-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

