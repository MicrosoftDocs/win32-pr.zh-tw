---
description: 弦是一個區域，系結于橢圓形和稱為正向的線段的交集。 下圖顯示使用弦函數繪製的弦。
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: 關於 Chords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3bad0d17d34386ada7c7c3b46bb1bcc4db5f9a2ce572ce78c33f8f4b6af909
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400528"
---
# <a name="about-chords"></a>關於 Chords

*弦* 是一個區域，系結于橢圓形和稱為 *正* 向的線段的交集。 下圖顯示使用 [**弦**](/windows/desktop/api/Wingdi/nf-wingdi-chord) 函數繪製的弦。

![elipse 的圖例，顯示兩個 radials、正向和絃](images/csfsh-02.png)

呼叫 [**弦**](/windows/win32/api/wingdi/nf-wingdi-chord)時，應用程式會提供橢圓形周框的左上角和右下角的座標，以及兩個點的座標來定義兩個 radials。 放射狀線是從橢圓形周框的中心繪製到橢圓形上某個點的直線。

當系統繪製弦的弧形部分時，它會使用目前的弧形方向來指定裝置內容。 預設弧線方向是逆時針的。 您可以藉由呼叫 [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) 函式，讓您的應用程式重設弧線方向。

 

 
