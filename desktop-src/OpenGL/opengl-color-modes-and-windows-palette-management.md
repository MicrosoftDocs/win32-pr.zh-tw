---
title: OpenGL 色彩模式和 Windows 調色板管理
description: Microsoft 在 Windows 中執行 OpenGL 支援兩種色彩圖元資料模式 RGBA 和色彩索引模式。 Windows 提供兩種類似的方式來處理色彩真色彩和調色板管理。
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- Windows 上的 OpenGL、色彩模式
- Windows 上的 OpenGL，管理元件管理
- 調色板管理 OpenGL
- 色彩模式 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf91ebb45e99368596cb48cb625f0eb6de025e6664144f104f6a9c17951a1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144131"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>OpenGL 色彩模式和 Windows 調色板管理

Microsoft 在 Windows 中執行 OpenGL 支援兩種色彩圖元資料模式： RGBA 和色彩索引模式。 Windows 提供兩種類似的方式來處理色彩： true 色彩和調色板管理。

若為真色彩裝置，每圖元可以接受16、24或更多位的色彩資訊，則可以同時顯示數十萬個、數十個或更多的色彩。 但是，當應用程式必須在選擇區類型的裝置上管理 RGBA 或色彩索引模式時，就會發生複雜性問題。 選擇區類型的裝置（例如256色 VGA 顯示器）受限於可同時顯示的色彩數目。 應用程式必須處理一些複雜的詳細資料，才能成功使用多元件類型的裝置。 由於色彩索引模式程式並不會使用硬體選擇區，因此比起使用 RGBA 模式的程式更難搭配使用真實色彩裝置。

 

 




