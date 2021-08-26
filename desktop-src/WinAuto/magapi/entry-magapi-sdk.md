---
title: 放大 API
description: 放大 API 可讓應用程式放大整個螢幕或畫面的部分，並套用色彩效果。
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 2a6c7a7ffb103b39c506c41b6b7b88f82319685226aff0d479558977caa9d46b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998430"
---
# <a name="magnification-api"></a>放大 API

## <a name="purpose"></a>目的

放大 API 可讓應用程式放大整個螢幕或畫面的部分，並套用色彩效果。

## <a name="where-applicable"></a>適用時

藉由使用放大 API，開發人員可以建立以 Windows 為基礎的輔助技術應用程式，以放大螢幕並將色彩效果套用至放大的螢幕內容。 對於視力較低的使用者，放大的影像大小和色彩效果有助於讓電腦更容易查看和使用。

## <a name="developer-audience"></a>開發人員對象

放大 API 主要是針對瞭解 Windows 程式設計的 c 和 c + + 開發人員，以及熟悉圖形程式設計概念的人員所設計。

## <a name="run-time-requirements"></a>執行階段需求求

Windows Vista 和更新版本的作業系統上，支援放大 API 的初始版本。 第二個版本新增了全螢幕放大功能，並支援 Windows 8 和更新版本。

Magnification.dll 支援 API。 若要編譯您的應用程式，請包含放大和連結至放大程式庫。

> [!Note]  
> 在 WOW64 下不支援放大 API;也就是說，32位的放大鏡應用程式將無法在64位 Windows 上正確執行。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|:---|:---|
| [放大 API 總覽](magapi-intro.md)<br/> | 本主題說明放大 API，並說明如何在應用程式中使用它。<br/> |
| [參考](entry-magapi-ref.md)<br/>  | 本章節包含縮放 API 的參考資訊。<br/>|
| [範例](magapi-samples-entry.md)<br/> | 下列範例應用程式會示範如何使用放大 API 來建立放大整個畫面的全螢幕放大鏡，以及視窗中放大和顯示幕幕一部分的視窗放大鏡。<br/> |

## <a name="related-topics"></a>相關主題

[Microsoft 協助工具網站](https://www.microsoft.com/accessibility/)， [Windows 10 的協助工具](/windows/apps/accessibility)
