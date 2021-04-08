---
title: 從畫面格緩衝區讀取色彩值
description: 使用從畫面格緩衝區中讀取色彩值的函式時，請留意在真色彩裝置和以選擇區為基礎的裝置上讀取 RGBA 值和色彩索引值之間的差異。
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- Windows 上的 OpenGL，從 framebuffers 讀取色彩值
- 從 framebuffers OpenGL 讀取色彩值
- framebuffers，讀取色彩值 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672439"
---
# <a name="reading-color-values-from-the-framebuffer"></a>從畫面格緩衝區讀取色彩值

使用從畫面格緩衝區中讀取色彩值的函式時，請留意在真色彩裝置和以選擇區為基礎的裝置上讀取 RGBA 值和色彩索引值之間的差異。

在真彩色裝置上：

-   RGBA 值僅限於裝置中的通道。
-   色彩索引值會以 RGBA 值的形式儲存在畫面格緩衝區中。 使用這些值時，您必須執行從 RGBA 到邏輯調色板索引的反向轉譯。 如果有兩個邏輯索引具有相同的 RGBA 值，則可能會傳回錯誤的索引。

在以選擇區為基礎的裝置上：

-   RGBA 值是從系統元件中的索引讀取的。 邏輯索引是從反向資料表中取得，而 RGBA 元件則會解壓縮。
-   色彩索引值會從索引讀取至系統選擇區，而反向資料表則用來取得邏輯調色板索引。

 

 




