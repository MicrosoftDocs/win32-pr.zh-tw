---
title: 設定自訂任意資料流程
description: 設定自訂任意資料流程
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- 串流，設定自訂任意資料流程
- 編解碼器，設定自訂任意資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672975"
---
# <a name="configuring-custom-arbitrary-streams"></a><span data-ttu-id="efa37-105">設定自訂任意資料流程</span><span class="sxs-lookup"><span data-stu-id="efa37-105">Configuring Custom Arbitrary Streams</span></span>

<span data-ttu-id="efa37-106">使用您自己的任意資料類型時，您必須建立 GUID 值做為它的主要媒體類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="efa37-106">When using your own arbitrary data type, you must create a GUID value to serve as the major media type identifier for it.</span></span> <span data-ttu-id="efa37-107">當寫入器遇到具有無法辨識之主要類型的設定檔中的資料流程時，它會假設資料流程是自訂的任意資料。</span><span class="sxs-lookup"><span data-stu-id="efa37-107">When the writer encounters a stream in a profile with a major type it does not recognize, it assumes that the stream is custom arbitrary data.</span></span> <span data-ttu-id="efa37-108">它會接受您的範例、packetize 它們，並將它們與檔案中其他資料流程的範例合併，而不需要以任何方式驗證資料。</span><span class="sxs-lookup"><span data-stu-id="efa37-108">It will accept your samples, packetize them, and combine them with samples from the other streams in the file without verifying the data in any way.</span></span>

<span data-ttu-id="efa37-109">您也可以建立自己的子類型 GUID 識別碼，來定義自訂資料的子類別。</span><span class="sxs-lookup"><span data-stu-id="efa37-109">You can also create your own subtype GUID identifiers to define subcategories of your custom data.</span></span> <span data-ttu-id="efa37-110">寫入器會完全忽略這些子類型，但會保留在 ASF 檔案的標頭區段中，讓您的讀取應用程式可以取出這些子類型，並根據它們進行決策。</span><span class="sxs-lookup"><span data-stu-id="efa37-110">The writer will ignore these subtypes completely, but they will be preserved in the header section of the ASF file, so your reading application can retrieve them and make decisions based on them.</span></span>

<span data-ttu-id="efa37-111">任意的資料流程需要位元速率和緩衝區視窗，而且必須具有已清除值的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構，但主要媒體類型和子類型除外 (如果使用一個) 。</span><span class="sxs-lookup"><span data-stu-id="efa37-111">An arbitrary stream requires a bit rate and buffer window, and must have a [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure with the values cleared except for the major media type and subtype(if using one).</span></span>

## <a name="related-topics"></a><span data-ttu-id="efa37-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="efa37-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efa37-113">**所有資料流程通用的設定**</span><span class="sxs-lookup"><span data-stu-id="efa37-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="efa37-114">**設定任意資料流程類型**</span><span class="sxs-lookup"><span data-stu-id="efa37-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="efa37-115">**自訂任意資料流程**</span><span class="sxs-lookup"><span data-stu-id="efa37-115">**Custom Arbitrary Data Streams**</span></span>](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




