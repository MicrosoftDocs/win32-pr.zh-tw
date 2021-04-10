---
title: 擴充 OpenGL 函數
description: OpenGL 程式庫支援其函式的多個實作為。
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- Windows 上的 OpenGL，擴充功能函式
- 擴充功能 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932476"
---
# <a name="extending-opengl-functions"></a>擴充 OpenGL 函數

OpenGL 程式庫支援其函式的多個實作為。 在不同的轉譯內容中，不一定支援在某個轉譯內容中支援的擴充功能。 針對應用程式中使用擴充函數的指定轉譯內容，只使用 [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) 函式所傳回的函數位址。

 

 




