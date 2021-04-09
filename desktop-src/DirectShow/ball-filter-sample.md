---
description: 球形濾波器範例
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: 球形濾波器範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846731"
---
# <a name="ball-filter-sample"></a>球形濾波器範例

## <a name="description"></a>Description

球形濾波器是一個影片來源篩選器，可產生彈跳球的影像。 此範例說明格式的協商，以及使用來源篩選基類 [**CSource**](csource.md) 和 [**CSourceStream**](csourcestream.md)。

Fball 和 Fball 中的程式碼會管理篩選介面。 這兩個檔案大約包含來源篩選器所需的最少程式碼。 球形和球 .cpp 檔案包含彈跳球的程式碼。

此篩選器具有單一輸出圖釘，可提供影片串流，以顯示在框架中跳動的球。 球濾波器也接受來自下游篩選的品質管制要求，其說明簡單的品質管理原則。 此篩選準則會針對該目的來實行 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 介面。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： \[ *SDK 根* \] \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ 球。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 範例](directshow-samples.md)
</dt> </dl>

 

 



