---
description: 為來源讀取器或接收寫入器指定多媒體類別排程器服務 (MMCSS) 類別。
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: 'MF_READWRITE_MMCSS_CLASS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694692"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a><span data-ttu-id="09f54-103">MF \_ READWRITE \_ MMCSS \_ 類別屬性</span><span class="sxs-lookup"><span data-stu-id="09f54-103">MF\_READWRITE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="09f54-104">為來源讀取器或接收寫入器指定 [多媒體類別](../procthread/multimedia-class-scheduler-service.md) 排程器服務 (MMCSS) 類別。</span><span class="sxs-lookup"><span data-stu-id="09f54-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) class for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="09f54-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="09f54-105">Data type</span></span>

<span data-ttu-id="09f54-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="09f54-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="09f54-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="09f54-107">Get/set</span></span>

<span data-ttu-id="09f54-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="09f54-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="09f54-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="09f54-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="09f54-110">備註</span><span class="sxs-lookup"><span data-stu-id="09f54-110">Remarks</span></span>

<span data-ttu-id="09f54-111">當您建立 [來源讀取](source-reader.md) 器或 [接收寫入器](sink-writer.md)的實例時，可選擇性地設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="09f54-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="09f54-112">屬性的值必須是有效的 MMCSS 類別名稱。</span><span class="sxs-lookup"><span data-stu-id="09f54-112">The value of the attribute must be a valid MMCSS class name.</span></span>

<span data-ttu-id="09f54-113">如果設定這個屬性，來源讀取器或接收寫入器會使用指定的 MMCSS 類別來註冊其所有線程。</span><span class="sxs-lookup"><span data-stu-id="09f54-113">If this attribute is set, the Source Reader or Sink Writer registers all of its threads with the specified MMCSS class.</span></span> <span data-ttu-id="09f54-114">MMCSS 可確保來源讀取器或接收寫入器中的資料處理優先順序高於其他系統工作。</span><span class="sxs-lookup"><span data-stu-id="09f54-114">The MMCSS ensures that data processing in the Source Reader or Sink Writer has priority over other system tasks.</span></span>

<span data-ttu-id="09f54-115">若要指定基本優先權，請設定 [ [MF \_ READWRITE \_ MMCSS \_ priority](mf-readwrite-mmcss-priority.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="09f54-115">To specify the base priority, set the [MF\_READWRITE\_MMCSS\_PRIORITY](mf-readwrite-mmcss-priority.md) attribute.</span></span> <span data-ttu-id="09f54-116">如果未設定該屬性，則基本優先權為零。</span><span class="sxs-lookup"><span data-stu-id="09f54-116">If that attribute is not set, the base priority is zero.</span></span>

<span data-ttu-id="09f54-117">針對音訊處理執行緒，如果 set) 覆寫此屬性，則 (的 [MF \_ READWRITE \_ MMCSS \_ 類別 \_ 音訊](mf-readwrite-mmcss-class-audio.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="09f54-117">For audio-processing threads, the [MF\_READWRITE\_MMCSS\_CLASS\_AUDIO](mf-readwrite-mmcss-class-audio.md) attribute (if set) overrides this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="09f54-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="09f54-118">Requirements</span></span>



| <span data-ttu-id="09f54-119">需求</span><span class="sxs-lookup"><span data-stu-id="09f54-119">Requirement</span></span> | <span data-ttu-id="09f54-120">值</span><span class="sxs-lookup"><span data-stu-id="09f54-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09f54-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09f54-121">Minimum supported client</span></span><br/> | <span data-ttu-id="09f54-122">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09f54-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="09f54-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09f54-123">Minimum supported server</span></span><br/> | <span data-ttu-id="09f54-124">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09f54-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="09f54-125">標頭</span><span class="sxs-lookup"><span data-stu-id="09f54-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="09f54-126"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="09f54-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09f54-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09f54-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f54-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="09f54-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
