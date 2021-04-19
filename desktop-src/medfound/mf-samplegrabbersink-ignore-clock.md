---
description: 指定範例-捕獲接收是否使用呈現時鐘來排程範例。
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: 'MF_SAMPLEGRABBERSINK_IGNORE_CLOCK 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978208"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a><span data-ttu-id="08184-103">MF \_ SAMPLEGRABBERSINK \_ 忽略 \_ 時鐘屬性</span><span class="sxs-lookup"><span data-stu-id="08184-103">MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute</span></span>

<span data-ttu-id="08184-104">指定範例-捕獲接收是否使用呈現時鐘來排程範例。</span><span class="sxs-lookup"><span data-stu-id="08184-104">Specifies whether the sample-grabber sink uses the presentation clock to schedule samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="08184-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="08184-105">Data type</span></span>

<span data-ttu-id="08184-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="08184-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="08184-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="08184-107">Get/set</span></span>

<span data-ttu-id="08184-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="08184-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="08184-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="08184-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="08184-110">備註</span><span class="sxs-lookup"><span data-stu-id="08184-110">Remarks</span></span>

<span data-ttu-id="08184-111">您可以在 [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) 函數所建立的啟用物件上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="08184-111">You can set this attribute on the activation object created by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="08184-112">在啟用物件上呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法之前，請先設定屬性。</span><span class="sxs-lookup"><span data-stu-id="08184-112">Set the attribute before calling the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method on the activation object.</span></span>

<span data-ttu-id="08184-113">根據預設，當範例抓取器接收到範例時，它會等候範例的呈現時間叫用應用程式的回呼。</span><span class="sxs-lookup"><span data-stu-id="08184-113">By default, when the sample-grabber sink receives a sample, it waits until the presentation time of the sample to invoke the application's callback.</span></span> <span data-ttu-id="08184-114">如果 MF \_ SAMPLEGRABBERSINK \_ 忽略 \_ 時鐘屬性為非零值，則範例抓取器接收會忽略標記法，並在收到每個範例時立即叫用回呼。</span><span class="sxs-lookup"><span data-stu-id="08184-114">If the MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute is nonzero, the sample-grabber sink ignores the presentation clock and invokes the callback as soon as it receives each sample.</span></span>

<span data-ttu-id="08184-115">建議使用方式：</span><span class="sxs-lookup"><span data-stu-id="08184-115">Recommended usage:</span></span>

-   <span data-ttu-id="08184-116">如果您想要儘快處理範例，請將此屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="08184-116">If you want to process samples as quickly as possible, set this attribute to **TRUE**.</span></span>
-   <span data-ttu-id="08184-117">如果您想要讓回呼方法的呼叫與時鐘同步，請不要設定這個屬性，或將它設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="08184-117">If you want the calls to the callback method to be synchronized with the clock, either do not set this attribute or set it to **FALSE**.</span></span> <span data-ttu-id="08184-118">您可以藉由設定 [ [**MF \_ SAMPLEGRABBERSINK \_ SAMPLE \_ TIME \_ OFFSET**](mf-samplegrabbersink-sample-time-offset-attribute.md) ] 屬性，以稍微早于時鐘的方式取得範例，仍保持同步處理。</span><span class="sxs-lookup"><span data-stu-id="08184-118">You can get samples slightly ahead of the clock, while still remaining synchronized, by setting the [**MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET**](mf-samplegrabbersink-sample-time-offset-attribute.md) attribute.</span></span>

<span data-ttu-id="08184-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="08184-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="08184-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="08184-120">Requirements</span></span>



| <span data-ttu-id="08184-121">需求</span><span class="sxs-lookup"><span data-stu-id="08184-121">Requirement</span></span> | <span data-ttu-id="08184-122">值</span><span class="sxs-lookup"><span data-stu-id="08184-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08184-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08184-123">Minimum supported client</span></span><br/> | <span data-ttu-id="08184-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08184-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="08184-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08184-125">Minimum supported server</span></span><br/> | <span data-ttu-id="08184-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08184-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="08184-127">標頭</span><span class="sxs-lookup"><span data-stu-id="08184-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="08184-128"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="08184-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08184-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08184-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08184-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="08184-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08184-131">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="08184-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




