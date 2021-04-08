---
title: MCI 裝置功能
description: MCI 裝置功能
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- MCIWndCanConfig 宏
- MCIWndCanEject 宏
- MCIWndCanPlay 宏
- MCIWndCanRecord 宏
- MCIWndCanSave 宏
- MCIWndCanWindow 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021999"
---
# <a name="mci-device-capabilities"></a>MCI 裝置功能

MCIWnd 包含下列宏，可讓您查詢 MCI 裝置的功能。



| 巨集                                      | Description                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | 判斷裝置是否具有設定對話方塊，可支援多個設定，例如 MCIAVI 裝置。                   |
| [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | 判斷裝置是否有軟體控制的退出功能。                                                                       |
| [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | 判斷裝置是否可以播放現有的內容。                                                                                  |
| [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | 判斷裝置是否可以錄製。                                                                                                     |
| [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | 判斷裝置是否可以儲存資料。                                                                                                 |
| [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | 判斷裝置是否支援 MCI 視窗命令 (例如 [**window**](window.md)、 [**put**](put.md) 和 [**where**](where.md)) 。 |



 

如果裝置支援特定功能，這些宏會傳回 **TRUE** ，否則會傳回 **FALSE** 。

 

 




