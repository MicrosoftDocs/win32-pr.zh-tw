---
description: 'VMR Renderless 播放模式 (自訂配置器-展示者) '
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: 'VMR Renderless 播放模式 (自訂配置器-展示者) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693752"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a>VMR Renderless 播放模式 (自訂配置器-展示者) 

在 renderless 播放模式中，VMR 不會執行轉譯。 相反地，它會使用應用程式所提供的自訂配置器提供者。 這種模式適用于具有複雜影片效果的遊戲和其他類型的應用程式。 Renderless 播放模式可讓應用程式建立和控制自己的 DirectDraw 介面 (VMR-7) 或 Direct3D 介面 (VMR 9) ，以及在簡報時存取影片位。

在 renderless 模式中，VMR-9 不會自動載入其混音器元件。

在 renderless 播放模式中，應用程式會執行下列工作：

-   管理播放視窗。
-   配置 DirectDraw 或 Direct3D 物件和最終的框架緩衝區。
-   通知所使用物件的其餘播放系統。
-   提供正確時間的框架緩衝區。
-   處理所有解決模式變更、監視變更和介面遺失。 它必須建議這些事件的其餘播放系統。

VMR 會執行下列動作：

-   處理與呈現影片框架相關的所有時間。
-   提供品質控制資訊給應用程式和其餘的播放系統。
-   為播放系統的上游元件提供一致的介面，這並不知道應用程式是否提供框架緩衝區配置和執行轉譯。
-   提供轉譯之前可能需要的任何影片資料流程混合。

由於去交錯是由混音器所執行，因此配置器呈現者一律會收到 deinterlaced 的畫面格。 如需詳細資訊，請參閱 [設定隔行掃描喜好設定](setting-deinterlace-preferences.md)。

如需提供自訂配置器-展示者的詳細資訊，請參閱下列主題：

-   [提供 VMR-7 的自訂 Allocator-Presenter](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [提供 VMR-9 的自訂 Allocator-Presenter](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [將 VMR 同步處理至監視器的更新速率](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



