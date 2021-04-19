---
description: 指定位元組資料流程處理常式是否可以使用開啟的位元組資料流程，以供另一個執行緒寫入。
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: 'MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974367"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a><span data-ttu-id="b28f9-103">MF \_ BYTESTREAMHANDLER \_ 接受 \_ 共用 \_ 寫入屬性</span><span class="sxs-lookup"><span data-stu-id="b28f9-103">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute</span></span>

<span data-ttu-id="b28f9-104">指定位元組資料流程處理常式是否可以使用開啟的位元組資料流程，以供另一個執行緒寫入。</span><span class="sxs-lookup"><span data-stu-id="b28f9-104">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread.</span></span>

## <a name="data-type"></a><span data-ttu-id="b28f9-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b28f9-105">Data type</span></span>

<span data-ttu-id="b28f9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b28f9-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b28f9-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="b28f9-107">Get/set</span></span>

<span data-ttu-id="b28f9-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="b28f9-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b28f9-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="b28f9-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b28f9-110">備註</span><span class="sxs-lookup"><span data-stu-id="b28f9-110">Remarks</span></span>

<span data-ttu-id="b28f9-111">位元組資料流程處理常式可以支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="b28f9-111">Byte-stream handlers can support this attribute.</span></span> <span data-ttu-id="b28f9-112">若要取得或設定屬性，請先查詢 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的位元組資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="b28f9-112">To get or set the attribute, first query the byte-stream handler for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="b28f9-113">然後呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 或 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span><span class="sxs-lookup"><span data-stu-id="b28f9-113">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) or [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span></span>

<span data-ttu-id="b28f9-114">如果這個屬性為 **TRUE**，則表示位元組資料流程處理常式可以在另一個執行緒寫入相同的資料流程時，從資料流程讀取。</span><span class="sxs-lookup"><span data-stu-id="b28f9-114">If this attribute is **TRUE**, it means that the byte-stream handler can read from a stream while another thread writes to the same stream.</span></span> <span data-ttu-id="b28f9-115">開啟資料流程以供另一個執行緒寫入時， [**IMFByteStream：： GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) 方法會傳回 **MFBYTESTREAM \_ 共用 \_ 寫入** 旗標。</span><span class="sxs-lookup"><span data-stu-id="b28f9-115">When a stream is opened for writing by another thread, the [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) method returns the **MFBYTESTREAM\_SHARE\_WRITE** flag.</span></span>

<span data-ttu-id="b28f9-116">這個屬性會影響來源解析。</span><span class="sxs-lookup"><span data-stu-id="b28f9-116">This attribute affects source resolution.</span></span> <span data-ttu-id="b28f9-117">如果位元組資料流程已設定 **MFBYTESTREAM \_ 共用 \_ 寫入** 旗標，則 [來源解析](source-resolver.md) 程式將不會將該資料流程傳遞至位元組資料流程處理常式，除非處理常式的 MF \_ BYTESTREAMHANDLER \_ 接受 \_ 共用 \_ 寫入屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="b28f9-117">If a byte stream has the **MFBYTESTREAM\_SHARE\_WRITE** flag set, the [Source Resolver](source-resolver.md) will not pass that stream to a byte-stream handler unless the handler has the MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute set to **TRUE**.</span></span>

<span data-ttu-id="b28f9-118">**MFBYTESTREAM \_ SHARE \_ WRITE** 旗標是在處理常式從它讀取時，資料流程長度可能會變更的提示。</span><span class="sxs-lookup"><span data-stu-id="b28f9-118">The **MFBYTESTREAM\_SHARE\_WRITE** flag is a hint that the length of the stream might change while the handler is reading from it.</span></span>

<span data-ttu-id="b28f9-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="b28f9-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b28f9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b28f9-120">Requirements</span></span>



| <span data-ttu-id="b28f9-121">需求</span><span class="sxs-lookup"><span data-stu-id="b28f9-121">Requirement</span></span> | <span data-ttu-id="b28f9-122">值</span><span class="sxs-lookup"><span data-stu-id="b28f9-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b28f9-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b28f9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b28f9-124">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b28f9-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b28f9-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b28f9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b28f9-126">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b28f9-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b28f9-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b28f9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b28f9-128"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b28f9-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b28f9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b28f9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b28f9-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b28f9-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b28f9-131">配置處理常式和 Byte-Stream 處理常式</span><span class="sxs-lookup"><span data-stu-id="b28f9-131">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




