---
description: 應用程式會在區域上執行點擊測試，以判斷目前資料指標位置的座標。
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: 點擊測試區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191941"
---
# <a name="hit-testing-regions"></a>點擊測試區域

應用程式會在區域上執行點擊測試，以判斷目前資料指標位置的座標。 然後，它會將這些座標和識別區域的控制碼傳遞給 [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) 函數。 您可以處理各種不同的滑鼠訊息（例如， [**wm \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) 、 [**wm \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) 、 [**wm \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) 和 [**wm \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md)）來抓取游標座標。 PtInRegion 的傳回值會指出游標位置是否在指定的區域內。

 

 
