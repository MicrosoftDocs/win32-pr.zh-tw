---
description: 累積的周框是最小的矩形，可封閉受最近繪圖作業影響的視窗或工作區部分。
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: 累積的周框
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512928"
---
# <a name="accumulated-bounding-rectangle"></a>累積的周框

累積的周 *框* 是最小的矩形，可封閉受最近繪圖作業影響的視窗或工作區部分。 應用程式可以使用這個矩形，輕鬆地判斷繪圖作業所造成的變更範圍。 它有時會與 [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) 搭配使用，以判斷在清除更新鎖定之後必須重新繪製的工作區部分。

應用程式會使用 [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) 函數 (指定 DCB \_ 讓) 開始累積周框。 系統隨後會累積周框的點，因為應用程式會使用指定的顯示裝置內容。 應用程式可以使用 [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) 函數，隨時取得目前的周框矩形。 應用程式會再次呼叫 **SetBoundsRect** 來停止累積，並指定 DCB \_ DISABLE 值。

 

 



