---
description: 位元組資料流程屬性
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: 位元組資料流程屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000054"
---
# <a name="byte-stream-attributes"></a><span data-ttu-id="75ea5-103">位元組資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="75ea5-103">Byte Stream Attributes</span></span>

<span data-ttu-id="75ea5-104">下列屬性適用于某些位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="75ea5-104">The following attributes apply to some byte streams.</span></span> <span data-ttu-id="75ea5-105">若要找出位元組資料流程是否支援屬性，請查詢 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的位元組資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="75ea5-105">To find out whether a byte stream supports attributes, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>



| <span data-ttu-id="75ea5-106">屬性</span><span class="sxs-lookup"><span data-stu-id="75ea5-106">Attribute</span></span>                                                                                  | <span data-ttu-id="75ea5-107">描述</span><span class="sxs-lookup"><span data-stu-id="75ea5-107">Description</span></span>                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="75ea5-108">**MF \_ BYTESTREAM \_ 內容 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="75ea5-108">**MF\_BYTESTREAM\_CONTENT\_TYPE**</span></span>](mf-bytestream-content-type-attribute.md)              | <span data-ttu-id="75ea5-109">指定位元組資料流程的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="75ea5-109">Specifies the MIME type of a byte stream.</span></span>                         |
| [<span data-ttu-id="75ea5-110">**MF \_ BYTESTREAM \_ 持續期間**</span><span class="sxs-lookup"><span data-stu-id="75ea5-110">**MF\_BYTESTREAM\_DURATION**</span></span>](mf-bytestream-duration-attribute.md)                       | <span data-ttu-id="75ea5-111">指定位元組資料流程的持續時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="75ea5-111">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="75ea5-112">MF \_ BYTESTREAM \_ IFO \_ 檔案 \_ URI</span><span class="sxs-lookup"><span data-stu-id="75ea5-112">MF\_BYTESTREAM\_IFO\_FILE\_URI</span></span>](mf-bytestream-ifo-file-uri.md)                           | <span data-ttu-id="75ea5-113">指定相關聯 IFO 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="75ea5-113">Specifies the URL of an associated IFO file.</span></span>                      |
| [<span data-ttu-id="75ea5-114">**MF \_ BYTESTREAM \_ 上次 \_ 修改 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="75ea5-114">**MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME**</span></span>](mf-bytestream-last-modified-time-attribute.md) | <span data-ttu-id="75ea5-115">指定上一次修改位元組資料流程的時間。</span><span class="sxs-lookup"><span data-stu-id="75ea5-115">Specifies when a byte stream was last modified.</span></span>                   |
| [<span data-ttu-id="75ea5-116">**MF \_ BYTESTREAM \_ 來源 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="75ea5-116">**MF\_BYTESTREAM\_ORIGIN\_NAME**</span></span>](mf-bytestream-origin-name-attribute.md)                | <span data-ttu-id="75ea5-117">指定位元組資料流程的原始 URL。</span><span class="sxs-lookup"><span data-stu-id="75ea5-117">Specifies the original URL for a byte stream.</span></span>                     |



 

<span data-ttu-id="75ea5-118">下列屬性適用于位元組資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="75ea5-118">The following attributes apply to byte-stream handlers.</span></span>



| <span data-ttu-id="75ea5-119">屬性</span><span class="sxs-lookup"><span data-stu-id="75ea5-119">Attribute</span></span>                                                                                    | <span data-ttu-id="75ea5-120">描述</span><span class="sxs-lookup"><span data-stu-id="75ea5-120">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75ea5-121">MF \_ BYTESTREAMHANDLER \_ 接受 \_ 共用 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="75ea5-121">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE</span></span>](mf-bytestreamhandler-accepts-share-write.md) | <span data-ttu-id="75ea5-122">指定位元組資料流程處理常式是否可以使用開啟的位元組資料流程以供另一個執行緒寫入</span><span class="sxs-lookup"><span data-stu-id="75ea5-122">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="75ea5-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="75ea5-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ea5-124">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="75ea5-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[<span data-ttu-id="75ea5-125">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="75ea5-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



