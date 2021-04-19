---
description: ITFormatControl 介面會公開方法，以允許應用程式抓取有關呼叫之接收或傳輸資料流程格式的資訊。
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: 'ITFormatControl 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996254"
---
# <a name="itformatcontrol-interface"></a><span data-ttu-id="441eb-103">ITFormatControl 介面</span><span class="sxs-lookup"><span data-stu-id="441eb-103">ITFormatControl interface</span></span>

<span data-ttu-id="441eb-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。</span><span class="sxs-lookup"><span data-stu-id="441eb-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="441eb-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="441eb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="441eb-106">**ITFormatControl** 介面會公開方法，以允許應用程式抓取有關呼叫之接收或傳輸資料流程格式的資訊。</span><span class="sxs-lookup"><span data-stu-id="441eb-106">The **ITFormatControl** interface exposes methods that allow an application to retrieve information concerning the format of a receive or transmit stream for a call.</span></span>

<span data-ttu-id="441eb-107">此介面是由 [H323 MSP](h323-msp.md) 所執行，而且只會在呼叫使用此服務提供者時公開。</span><span class="sxs-lookup"><span data-stu-id="441eb-107">This interface is implemented by the [H323 MSP](h323-msp.md) and is exposed only when a call uses this service provider.</span></span>

## <a name="members"></a><span data-ttu-id="441eb-108">成員</span><span class="sxs-lookup"><span data-stu-id="441eb-108">Members</span></span>

<span data-ttu-id="441eb-109">**ITFormatControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="441eb-109">The **ITFormatControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="441eb-110">**ITFormatControl** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="441eb-110">**ITFormatControl** also has these types of members:</span></span>

-   [<span data-ttu-id="441eb-111">方法</span><span class="sxs-lookup"><span data-stu-id="441eb-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="441eb-112">方法</span><span class="sxs-lookup"><span data-stu-id="441eb-112">Methods</span></span>

<span data-ttu-id="441eb-113">**ITFormatControl** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="441eb-113">The **ITFormatControl** interface has these methods.</span></span>



| <span data-ttu-id="441eb-114">方法</span><span class="sxs-lookup"><span data-stu-id="441eb-114">Method</span></span>                                                                     | <span data-ttu-id="441eb-115">描述</span><span class="sxs-lookup"><span data-stu-id="441eb-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="441eb-116">**GetCurrentFormat**</span><span class="sxs-lookup"><span data-stu-id="441eb-116">**GetCurrentFormat**</span></span>](itformatcontrol-getcurrentformat.md)               | <span data-ttu-id="441eb-117">取得目前資料流程的媒體格式。</span><span class="sxs-lookup"><span data-stu-id="441eb-117">Gets the media format of the current stream.</span></span><br/>                        |
| [<span data-ttu-id="441eb-118">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="441eb-118">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md) | <span data-ttu-id="441eb-119">取得與目前格式相關聯的功能數目。</span><span class="sxs-lookup"><span data-stu-id="441eb-119">Gets the number of capabilities associated with the current format.</span></span><br/> |
| [<span data-ttu-id="441eb-120">**GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="441eb-120">**GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)                     | <span data-ttu-id="441eb-121">取得與指定之格式索引相關聯的功能。</span><span class="sxs-lookup"><span data-stu-id="441eb-121">Gets the capabilities associated with a given format index.</span></span><br/>         |
| [<span data-ttu-id="441eb-122">**ReleaseFormat**</span><span class="sxs-lookup"><span data-stu-id="441eb-122">**ReleaseFormat**</span></span>](itformatcontrol-releaseformat.md)                     | <span data-ttu-id="441eb-123">釋放與格式相關聯的結構。</span><span class="sxs-lookup"><span data-stu-id="441eb-123">Releases the structure associated with the format.</span></span><br/>                  |
| [<span data-ttu-id="441eb-124">**ReOrderCapabilities**</span><span class="sxs-lookup"><span data-stu-id="441eb-124">**ReOrderCapabilities**</span></span>](itformatcontrol-reordercapabilities.md)         | <span data-ttu-id="441eb-125">設定格式功能的新順序。</span><span class="sxs-lookup"><span data-stu-id="441eb-125">Sets a new order for format capabilities.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="441eb-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="441eb-126">Requirements</span></span>



| <span data-ttu-id="441eb-127">需求</span><span class="sxs-lookup"><span data-stu-id="441eb-127">Requirement</span></span> | <span data-ttu-id="441eb-128">值</span><span class="sxs-lookup"><span data-stu-id="441eb-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="441eb-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="441eb-129">TAPI version</span></span><br/> | <span data-ttu-id="441eb-130">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="441eb-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="441eb-131">標頭</span><span class="sxs-lookup"><span data-stu-id="441eb-131">Header</span></span><br/>       | <dl> <span data-ttu-id="441eb-132"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="441eb-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="441eb-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="441eb-133">Library</span></span><br/>      | <dl> <span data-ttu-id="441eb-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="441eb-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="441eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="441eb-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="441eb-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="441eb-136"><dt>Tapi3.dll</dt></span></span> </dl> |



 

