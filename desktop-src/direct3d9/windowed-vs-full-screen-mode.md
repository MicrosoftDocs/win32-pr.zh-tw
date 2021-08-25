---
description: Direct3D 應用程式可在兩種模式中執行：全螢幕或視窗化。
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: " (Direct3D 9) 的視窗型 vs Full-Screen 模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a845c464e6c402c46cc4aff09196ccfde65ad90371187045b0c14c41315a9f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025748"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a> (Direct3D 9) 的視窗型 vs Full-Screen 模式

Direct3D 應用程式可在兩種模式中執行：全螢幕或視窗化。

全螢幕模式表示應用程式執行所在的視窗涵蓋整個桌面，隱藏所有正在執行的應用程式， (包括您的開發環境) 。 通常遊戲預設為全螢幕模式，隱藏執行的所有應用程式，為使用者提供身歷其境的遊戲體驗。 在視窗模式中執行的應用程式，會與所有正在執行的應用程式共用桌面。 全螢幕模式和視窗模式之間的程式碼差異很小。

由於以全螢幕模式執行的應用程式會接管螢幕，偵錯應用程式需要其他監視器或使用遠端的偵錯工具。 使用 [DirectX 主控台工具](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) 來啟用多重監視器的調試。 視窗模式應用程式的其中一個優點是，您可以在偵錯工具中逐步執行程式碼，不需要多個監視器或遠端偵錯工具。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 裝置](direct3d-devices.md)
</dt> </dl>

 

 



