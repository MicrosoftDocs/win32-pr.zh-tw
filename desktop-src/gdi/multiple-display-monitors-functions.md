---
description: 下列函式提供多個監視器的支援。
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: 多重顯示器監視函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e35ab6fef353f793257721077074271915a3628859471a2f5d89694f6d47440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779138"
---
# <a name="multiple-display-monitors-functions"></a>多重顯示器監視函式

下列函式提供多個監視器的支援。



| 函式                                           | 描述                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | 列舉與指定裁剪矩形交集以及裝置內容可見區域交集形成之區域的顯示監視器。 |
| [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | 抓取顯示監視器的相關資訊。                                                                                                               |
| [**MonitorEnumProc**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)函式所呼叫的應用程式定義回呼函數。                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | 抓取顯示監視器的控制碼，其中包含指定的點。                                                                                   |
| [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | 使用指定的矩形，抓取具有最大區域交集的顯示監視器控制碼。                                              |
| [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | 抓取顯示監視器的控制碼，該控點與指定視窗的周框有最大的交集區域。                       |



 

 

 



