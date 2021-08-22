---
title: 擴充 OpenGL 函數
description: OpenGL 程式庫支援其函式的多個實作為。
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- Windows 上的 OpenGL，擴充功能函式
- 擴充功能 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dce68498d5a3e672e63da1ae05d9bb513a4121d110237d90cdad75df0ff84d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361340"
---
# <a name="extending-opengl-functions"></a>擴充 OpenGL 函數

OpenGL 程式庫支援其函式的多個實作為。 在不同的轉譯內容中，不一定支援在某個轉譯內容中支援的擴充功能。 針對應用程式中使用擴充函數的指定轉譯內容，只使用 [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) 函式所傳回的函數位址。

 

 




