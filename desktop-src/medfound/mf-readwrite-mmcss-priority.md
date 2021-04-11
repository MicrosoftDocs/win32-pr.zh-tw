---
description: 設定來源讀取器或接收寫入器的基底線程優先順序。
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: 'MF_READWRITE_MMCSS_PRIORITY 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027427"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a><span data-ttu-id="18d53-103">MF \_ READWRITE \_ MMCSS \_ PRIORITY 屬性</span><span class="sxs-lookup"><span data-stu-id="18d53-103">MF\_READWRITE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="18d53-104">設定來源讀取器或接收寫入器的基底線程優先順序。</span><span class="sxs-lookup"><span data-stu-id="18d53-104">Sets the base thread priority for the Source Reader or Sink Writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="18d53-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="18d53-105">Data type</span></span>

<span data-ttu-id="18d53-106">以 **UINT32** 儲存的 **INT32**</span><span class="sxs-lookup"><span data-stu-id="18d53-106">**INT32** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="18d53-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="18d53-107">Get/set</span></span>

<span data-ttu-id="18d53-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="18d53-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="18d53-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="18d53-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="18d53-110">備註</span><span class="sxs-lookup"><span data-stu-id="18d53-110">Remarks</span></span>

<span data-ttu-id="18d53-111">當您建立 [來源讀取](source-reader.md) 器或 [接收寫入器](sink-writer.md)的實例時，可選擇性地設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="18d53-111">Optionally set this attribute when you create an instance of the [Source Reader](source-reader.md) or [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="18d53-112">如果您設定此屬性，也請設定 [MF \_ READWRITE \_ MMCSS \_ 類別](mf-readwrite-mmcss-class.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="18d53-112">If you set this attribute, also set the [MF\_READWRITE\_MMCSS\_CLASS](mf-readwrite-mmcss-class.md) attribute.</span></span> <span data-ttu-id="18d53-113">否則，會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="18d53-113">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="18d53-114">當來源讀取器或接收寫入器向 [多媒體類別](../procthread/multimedia-class-scheduler-service.md)排程器服務註冊執行緒時，這個屬性的值會指定基底線程優先順序。</span><span class="sxs-lookup"><span data-stu-id="18d53-114">When the Source Reader or Sink Writer registers threads with the [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md), the value of this attribute specifies the base thread priority.</span></span> <span data-ttu-id="18d53-115">如果未設定此屬性，則預設值為零。</span><span class="sxs-lookup"><span data-stu-id="18d53-115">If this attribute is not set, the default value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d53-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="18d53-116">Requirements</span></span>



| <span data-ttu-id="18d53-117">需求</span><span class="sxs-lookup"><span data-stu-id="18d53-117">Requirement</span></span> | <span data-ttu-id="18d53-118">值</span><span class="sxs-lookup"><span data-stu-id="18d53-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d53-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18d53-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18d53-120">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18d53-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="18d53-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18d53-121">Minimum supported server</span></span><br/> | <span data-ttu-id="18d53-122">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18d53-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="18d53-123">標頭</span><span class="sxs-lookup"><span data-stu-id="18d53-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="18d53-124"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="18d53-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18d53-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18d53-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d53-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="18d53-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
