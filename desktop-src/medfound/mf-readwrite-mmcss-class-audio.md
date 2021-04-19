---
description: 指定多媒體類別排程器服務 (MMCSS 來源讀取器或接收寫入器中音訊處理執行緒的) 類別。
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: 'MF_READWRITE_MMCSS_CLASS_AUDIO 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981440"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a><span data-ttu-id="abf5b-103">MF \_ READWRITE \_ MMCSS \_ 類別 \_ 音訊屬性</span><span class="sxs-lookup"><span data-stu-id="abf5b-103">MF\_READWRITE\_MMCSS\_CLASS\_AUDIO attribute</span></span>

<span data-ttu-id="abf5b-104">指定 [多媒體類別](../procthread/multimedia-class-scheduler-service.md) 排程器服務 (MMCSS 來源讀取器或接收寫入器中音訊處理執行緒的) 類別。</span><span class="sxs-lookup"><span data-stu-id="abf5b-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for audio-processing threads in the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="abf5b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="abf5b-105">Data type</span></span>

<span data-ttu-id="abf5b-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="abf5b-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="abf5b-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="abf5b-107">Get/set</span></span>

<span data-ttu-id="abf5b-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="abf5b-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="abf5b-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="abf5b-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="abf5b-110">備註</span><span class="sxs-lookup"><span data-stu-id="abf5b-110">Remarks</span></span>

<span data-ttu-id="abf5b-111">當您建立 [來源讀取](source-reader.md) 器或 [接收寫入器](sink-writer.md)的實例時，可選擇性地設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="abf5b-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="abf5b-112">屬性的值必須是有效的 MMCSS 類別名稱。</span><span class="sxs-lookup"><span data-stu-id="abf5b-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="abf5b-113">如果設定這個屬性，來源讀取器或接收寫入器會使用指定的 MMCSS 類別來註冊其音訊處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="abf5b-113">If this attribute is set, the Source Reader or Sink Writer registers its audio-processing threads with the specified MMCSS class.</span></span> <span data-ttu-id="abf5b-114">MMCSS 可確保來源讀取器或接收寫入器中的資料處理優先順序高於其他系統工作。</span><span class="sxs-lookup"><span data-stu-id="abf5b-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="abf5b-115">若要指定音訊執行緒的基本優先權，請設定 [ [MF \_ READWRITE \_ MMCSS \_ priority \_ 音訊](mf-readwrite-mmcss-priority-audio.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="abf5b-115">To specify the base priority for audio threads, set the [MF\_READWRITE\_MMCSS\_PRIORITY\_AUDIO](mf-readwrite-mmcss-priority-audio.md) attribute.</span></span> <span data-ttu-id="abf5b-116">如果未設定該屬性，則音訊執行緒的基本優先權為零。</span><span class="sxs-lookup"><span data-stu-id="abf5b-116">If that attribute is not set, the base priority for audio threads is zero.</span></span>

<span data-ttu-id="abf5b-117">這個屬性會覆寫音訊處理執行緒的 [MF \_ READWRITE \_ MMCSS \_ 類別](mf-readwrite-mmcss-class.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="abf5b-117">This attribute overrides the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute for audio-processing threads.</span></span> <span data-ttu-id="abf5b-118">如果未設定這兩個屬性，則不會向 MCSS 註冊音訊執行緒。</span><span class="sxs-lookup"><span data-stu-id="abf5b-118">If neither attribute is set, audio threads are not registered with MCSS.</span></span>

<span data-ttu-id="abf5b-119">對於大部分的應用程式而言，音訊瑕疵比影片瑕疵更加明顯，因此較不容易接受。</span><span class="sxs-lookup"><span data-stu-id="abf5b-119">For most applications, audio glitching is much more noticeable to the user than video glitching, and therefore less acceptable.</span></span> <span data-ttu-id="abf5b-120">基於這個理由，應用程式通常應該將 MF \_ readwrite \_ MMCSS \_ 類別 \_ 音訊設定為比 [MF \_ readwrite \_ MMCSS \_ 類別](mf-readwrite-mmcss-class.md)更高優先順序的 MMCSS 類別。</span><span class="sxs-lookup"><span data-stu-id="abf5b-120">For this reason, an application should typically set MF\_READWRITE\_MMCSS\_CLASS\_AUDIO to a higher-priority MMCSS class than [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md).</span></span> <span data-ttu-id="abf5b-121">這可確保音訊處理的優先順序高於其他工作。</span><span class="sxs-lookup"><span data-stu-id="abf5b-121">This ensures that audio processing is given higher priority than other tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="abf5b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="abf5b-122">Requirements</span></span>



| <span data-ttu-id="abf5b-123">需求</span><span class="sxs-lookup"><span data-stu-id="abf5b-123">Requirement</span></span> | <span data-ttu-id="abf5b-124">值</span><span class="sxs-lookup"><span data-stu-id="abf5b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="abf5b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="abf5b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="abf5b-126">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abf5b-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="abf5b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="abf5b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="abf5b-128">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abf5b-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="abf5b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="abf5b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="abf5b-130"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="abf5b-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abf5b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abf5b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf5b-132">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="abf5b-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
