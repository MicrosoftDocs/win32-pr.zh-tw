---
title: 複合檔案優化
description: 非同步存放裝置可讓應用程式精確配置複合檔案，讓資料可依應用程式的要求順序提供。
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- 複合檔案優化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb55d4d9ba7b264c1a0aac4252d879a7ba98b6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671667"
---
# <a name="compound-file-optimization"></a><span data-ttu-id="97256-104">複合檔案優化</span><span class="sxs-lookup"><span data-stu-id="97256-104">Compound File Optimization</span></span>

<span data-ttu-id="97256-105">非同步存放裝置可讓應用程式精確配置複合檔案，讓資料可依應用程式的要求順序提供。</span><span class="sxs-lookup"><span data-stu-id="97256-105">Asynchronous storage enables applications to precisely layout compound files so that data is available in the order in which applications will require it.</span></span> <span data-ttu-id="97256-106">如果應用程式只需要部分資料來顯示第一頁的資訊，則可以將此資料放在檔案的開頭，即使它邏輯上位於資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="97256-106">If an application requires only part of its data to display a first page of information, this data can be placed at the beginning of the file, even if it logically resides at the end of a stream.</span></span> <span data-ttu-id="97256-107">來自不同資料流程的資料可以交錯。</span><span class="sxs-lookup"><span data-stu-id="97256-107">Data from different streams can be interleaved.</span></span> <span data-ttu-id="97256-108">例如，音訊和影片資料可以交錯，讓後續的讀取作業同時抓取，這是多媒體應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="97256-108">Audio and video data, for example, can be interleaved so that subsequent read operations retrieve both simultaneously, a requirement for multimedia applications.</span></span>

<span data-ttu-id="97256-109">[**IStorage：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) 可以用來配置 e，藉此改善大部分案例的效能。</span><span class="sxs-lookup"><span data-stu-id="97256-109">[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) can be used to layout a docfile, thus improving performance in most scenarios.</span></span>

 

 




