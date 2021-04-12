---
description: 來源解析程式
ms.assetid: 93eecf10-308b-4bb4-92f9-fd32d6ecdb04
title: 來源解析程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a844893b0348546d4fd174b0b24405812efcef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318728"
---
# <a name="source-resolver"></a><span data-ttu-id="5948a-103">來源解析程式</span><span class="sxs-lookup"><span data-stu-id="5948a-103">Source Resolver</span></span>

<span data-ttu-id="5948a-104">來源解析程式會接受 URL 或位元組資料流，然後為該內容建立適當的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="5948a-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="5948a-105">來源解析程式是應用程式建立媒體來源的標準方式。</span><span class="sxs-lookup"><span data-stu-id="5948a-105">The source resolver is the standard way for the applications to create media sources.</span></span>

<span data-ttu-id="5948a-106">來源解析程式會在內部使用 *處理常式* 物件：</span><span class="sxs-lookup"><span data-stu-id="5948a-106">Internally, the source resolver uses *handler* objects:</span></span>

-   <span data-ttu-id="5948a-107">*配置處理常式* 會使用 URL，並建立媒體來源或位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="5948a-107">*Scheme handlers* take a URL and create a media source or a byte stream.</span></span>
-   <span data-ttu-id="5948a-108">*位元組資料流程處理常式* 會採用位元組資料流程並建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="5948a-108">*Byte stream handlers* take a byte stream and create a media source.</span></span>

<span data-ttu-id="5948a-109">您可以執行自訂處理常式，並將它新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="5948a-109">You can implement a custom handler and add it to the registry.</span></span> <span data-ttu-id="5948a-110">配置處理常式是由 URL 配置所註冊，而位元組資料流程處理常式是由副檔名或 MIME 型別所註冊。</span><span class="sxs-lookup"><span data-stu-id="5948a-110">Scheme handlers are registered by URL scheme, and byte stream handlers are registered by file name extension or MIME type.</span></span>

<span data-ttu-id="5948a-111">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="5948a-111">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="5948a-112">使用來源解析程式</span><span class="sxs-lookup"><span data-stu-id="5948a-112">Using the Source Resolver</span></span>](using-the-source-resolver.md)
-   [<span data-ttu-id="5948a-113">設定媒體來源</span><span class="sxs-lookup"><span data-stu-id="5948a-113">Configuring a Media Source</span></span>](configuring-a-media-source.md)
-   [<span data-ttu-id="5948a-114">配置處理常式和 Byte-Stream 處理常式</span><span class="sxs-lookup"><span data-stu-id="5948a-114">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="5948a-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="5948a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5948a-116">媒體來源</span><span class="sxs-lookup"><span data-stu-id="5948a-116">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



