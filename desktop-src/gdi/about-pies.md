---
description: 圓形圖是以橢圓形曲線和兩個 radials 的交集來限定的區域。 下圖顯示使用圓形圖函數繪製的圓形圖。
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: 關於圓形圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e447e313a3088bbf9a72c790115fb3bb25770017cf13ce7922685fd18ccfe671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966458"
---
# <a name="about-pies"></a>關於圓形圖

*圓形圖* 是以橢圓形曲線和兩個 radials 的交集來限定的區域。 下圖顯示使用 [**圓形圖**](/windows/desktop/api/Wingdi/nf-wingdi-pie) 函數繪製的圓形圖。

![圖例顯示具有陰影圓形圖的橢圓形](images/csfsh-03.png)

呼叫 [**圓形圖**](/windows/win32/api/wingdi/nf-wingdi-pie)時，應用程式會提供橢圓形周框的左上角和右下角的座標，以及兩個點的座標來定義兩個 radials。

當系統繪製圓形圖的弧形部分時，它會針對指定的裝置內容使用目前的弧形方向。 預設弧線方向是逆時針的。 應用程式可以藉由呼叫 [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) 函數來重設弧線方向。

 

 
