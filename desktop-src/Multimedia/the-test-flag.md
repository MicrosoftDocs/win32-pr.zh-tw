---
title: 測試旗標
description: 測試旗標
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST 旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837b7812a904ed39fa0350d703b1525bbffa6f981b4736d25927840395932f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801472"
---
# <a name="the-test-flag"></a>測試旗標

「測試」 (MCI \_ 測試) 旗標會查詢裝置，以判斷它是否可以執行命令。 如果裝置無法執行命令，則會傳回錯誤。 如果可以處理命令，則不會傳回任何錯誤。 當您指定這個旗標時，MCI 會將控制權傳回給應用程式，而不會執行命令。

所有命令都支援此旗標，但 [**open**](open.md) ([**MCI \_ 開啟**](mci-open.md)) 並 [**關閉**](close.md) ([**MCI \_ 關閉**](mci-close.md)) 。

 

 




