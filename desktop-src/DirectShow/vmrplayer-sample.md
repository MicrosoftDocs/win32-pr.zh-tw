---
description: VMRPlayer 範例
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: VMRPlayer 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6281147e2c140541ade480e5b2a5e0f0a1d4146dde59b4871441b68fec6f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071912"
---
# <a name="vmrplayer-sample"></a>VMRPlayer 範例

## <a name="description"></a>描述

此範例使用影片混合轉譯器 9 (VMR-9) 篩選至 Alpha blend 一或兩個執行中的影片和靜態影像。

## <a name="usage"></a>使用方式

若要開啟第一部影片，請從 [檔案 **] 功能表中選擇 [** **開啟主要資料流程**]。 若要開啟第二部影片，請從 [檔案 **] 功能表中選擇 [** **開啟次要資料流程**] (您必須先) 開啟主要串流。 若要播放影片，請按一下 [ **播放** ] 按鈕。

您可以從 [ **VMR 屬性**] 功能表中選取 [**主要資料流程**] 或 [ **Secondard 資料流程**]，以設定影片的位置、大小和 Alpha 值。

若要在影片上新增靜態點陣圖，請從 [ **VMR 屬性**] 功能表選擇 [**靜態應用程式映射**]，然後按一下 [**顯示應用程式影像**] 方塊。 您可以使用相同的對話方塊來控制點陣圖的位置、大小和 Alpha 值。

若要捕獲混合的影片影像，請從 [ **VMR 屬性**] 功能表選擇 [**捕捉點陣圖影像**]。

您也可以從命令列指定主要映射資料流程：

**VMRPlayer** **/p** *檔案名*

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的[Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow樣品](directshow-samples.md)
</dt> </dl>

 

 



