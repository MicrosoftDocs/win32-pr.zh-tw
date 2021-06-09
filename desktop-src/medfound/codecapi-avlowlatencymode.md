---
description: 在編解碼器中啟用低延遲模式。
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: 'CODECAPI_AVLowLatencyMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826902"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="8080c-103">CODECAPI \_ AVLowLatencyMode 屬性</span><span class="sxs-lookup"><span data-stu-id="8080c-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="8080c-104">在編解碼器中啟用低延遲模式。</span><span class="sxs-lookup"><span data-stu-id="8080c-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="8080c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8080c-105">Data type</span></span>

<span data-ttu-id="8080c-106">**ULONG** (**VT \_ BOOL**) </span><span class="sxs-lookup"><span data-stu-id="8080c-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8080c-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="8080c-107">Property GUID</span></span>

<span data-ttu-id="8080c-108">**CODECAPI \_ AVLowLatencyMode**</span><span class="sxs-lookup"><span data-stu-id="8080c-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="8080c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8080c-109">Property value</span></span>

<span data-ttu-id="8080c-110">如果此值為非零值，則會啟用低延遲模式。</span><span class="sxs-lookup"><span data-stu-id="8080c-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="8080c-111">如果值為零，則會停用低延遲模式。</span><span class="sxs-lookup"><span data-stu-id="8080c-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="8080c-112">備註</span><span class="sxs-lookup"><span data-stu-id="8080c-112">Remarks</span></span>

<span data-ttu-id="8080c-113">此屬性同時適用于編碼器和解碼器。</span><span class="sxs-lookup"><span data-stu-id="8080c-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="8080c-114">當延遲時間應降至最低時，低延遲模式適用于即時通訊或即時捕捉。</span><span class="sxs-lookup"><span data-stu-id="8080c-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="8080c-115">但是，低延遲模式也可能會減少解碼或編碼品質。</span><span class="sxs-lookup"><span data-stu-id="8080c-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="8080c-116">編碼器預期不會因為編碼程式中的畫面格重新排列而新增任何範例延遲，而且一個輸入範例應該會產生一個輸出範例。</span><span class="sxs-lookup"><span data-stu-id="8080c-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="8080c-117">B 配量/框架可以存在，只要它們並未在編碼器中引進任何畫面格重新排序。</span><span class="sxs-lookup"><span data-stu-id="8080c-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

> [!WARNING] 
> <span data-ttu-id="8080c-118">在目前的執行中，媒體基礎 h.264 解碼會針對此屬性使用類型 **VT_UI4** 。</span><span class="sxs-lookup"><span data-stu-id="8080c-118">In the current implementation, the Media Foundation H.264 decoder uses the type **VT_UI4** for this property.</span></span> <span data-ttu-id="8080c-119">所有其他的執行（包括 h.264 編碼器）都會使用類型 **VT_BOOL**。</span><span class="sxs-lookup"><span data-stu-id="8080c-119">All other implementations, including the H.264 encoder, use the type **VT_BOOL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8080c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8080c-120">Requirements</span></span>



| <span data-ttu-id="8080c-121">需求</span><span class="sxs-lookup"><span data-stu-id="8080c-121">Requirement</span></span> | <span data-ttu-id="8080c-122">值</span><span class="sxs-lookup"><span data-stu-id="8080c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8080c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8080c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8080c-124">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8080c-124">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="8080c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8080c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8080c-126">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8080c-126">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8080c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8080c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8080c-128"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="8080c-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8080c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8080c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8080c-130">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="8080c-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8080c-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8080c-131">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

