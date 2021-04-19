---
description: 指定接收寫入器是否限制傳入資料的速率。
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: 'MF_SINK_WRITER_DISABLE_THROTTLING 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999938"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a><span data-ttu-id="c40ba-103">MF \_ 接收 \_ 寫入器 \_ 停用 \_ 節流屬性</span><span class="sxs-lookup"><span data-stu-id="c40ba-103">MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute</span></span>

<span data-ttu-id="c40ba-104">指定接收寫入器是否限制傳入資料的速率。</span><span class="sxs-lookup"><span data-stu-id="c40ba-104">Specifies whether the sink writer limits the rate of incoming data.</span></span>

## <a name="data-type"></a><span data-ttu-id="c40ba-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c40ba-105">Data type</span></span>

<span data-ttu-id="c40ba-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c40ba-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c40ba-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="c40ba-107">Get/set</span></span>

<span data-ttu-id="c40ba-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="c40ba-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c40ba-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="c40ba-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="c40ba-110">備註</span><span class="sxs-lookup"><span data-stu-id="c40ba-110">Remarks</span></span>

<span data-ttu-id="c40ba-111">根據預設，接收寫入器的 [**IMFSinkWriter：： WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) 方法會封鎖呼叫的執行緒，以限制資料的速率。</span><span class="sxs-lookup"><span data-stu-id="c40ba-111">By default, the sink writer's [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method limits the data rate by blocking the calling thread.</span></span> <span data-ttu-id="c40ba-112">這可防止應用程式太快傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="c40ba-112">This prevents the application from delivering samples too quickly.</span></span> <span data-ttu-id="c40ba-113">若要停用此行為，請 \_ \_ \_ \_ 在建立接收寫入器時 ，將 [MF 接收寫入器停用節流] 屬性設定為 [TRUE]。</span><span class="sxs-lookup"><span data-stu-id="c40ba-113">To disable this behavior, set the MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute to **TRUE** when you create the sink writer.</span></span>

<span data-ttu-id="c40ba-114">使用這個屬性搭配下列函數：</span><span class="sxs-lookup"><span data-stu-id="c40ba-114">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="c40ba-115">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="c40ba-115">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="c40ba-116">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="c40ba-116">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="c40ba-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c40ba-117">Requirements</span></span>



| <span data-ttu-id="c40ba-118">需求</span><span class="sxs-lookup"><span data-stu-id="c40ba-118">Requirement</span></span> | <span data-ttu-id="c40ba-119">值</span><span class="sxs-lookup"><span data-stu-id="c40ba-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c40ba-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c40ba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c40ba-121">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c40ba-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c40ba-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c40ba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c40ba-123">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c40ba-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c40ba-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c40ba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c40ba-125"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="c40ba-125"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c40ba-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c40ba-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c40ba-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c40ba-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c40ba-128">接收寫入器屬性</span><span class="sxs-lookup"><span data-stu-id="c40ba-128">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




