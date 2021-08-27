---
title: 螢幕讀取器參數
description: 螢幕讀取器參數會指出應用程式是否應該在以圖形方式呈現資訊的情況下，提供文字資訊。
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818ad36cfe833c1c9a3f39047cd88e6b4e8be55972d521ce524bb1e0618a48ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098418"
---
# <a name="screen-reader-parameter"></a>螢幕讀取器參數

螢幕讀取器參數會指出應用程式是否應該在以圖形方式呈現資訊的情況下，提供文字資訊。

此參數通常是由協助工具協助工具（例如螢幕讀取器）設定。 應用程式會使用 **spi \_ GETSCREENREADER** 和 **spi \_ SETSCREENREADER** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來取得和設定螢幕讀取器參數。

> [!Note]  
> 「朗讀程式」（Windows 隨附的螢幕讀取器）不會設定 **spi \_ SETSCREENREADER** 或 **spi \_ GETSCREENREADER** 旗標。

 

 

 