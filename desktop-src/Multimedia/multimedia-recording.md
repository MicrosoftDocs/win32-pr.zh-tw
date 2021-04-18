---
title: 多媒體錄製
description: 多媒體錄製
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- MCIWndCreate 函式
- MCIWndNew 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372157"
---
# <a name="multimedia-recording"></a>多媒體錄製

您可以使用內建于 MCIWnd 的使用者介面，在您的應用程式中執行錄製功能。 您可以使用 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函式和 [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) 宏來提供用於啟動和停止錄製的控制項，以及用來儲存記錄資訊的控制項。 使用 **MCIWndCreate**，您可以指定視窗樣式來顯示 MCIWnd 視窗，以及將 [ **記錄** ] 按鈕包含在工具列上。 使用 **MCIWndNew**，您可以指定要記錄的裝置類型，並指定要在新檔案中捕捉資訊。

如果您的應用程式需要更複雜的資訊，您可以使用 [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) 宏來自動化和自訂錄製。 如需詳細資訊，請參閱 [自訂錄製流程](customizing-the-recording-process.md)。

> [!Note]  
> 有些裝置，例如 CD 音訊和 MCIAVI，僅供播放。 其他裝置（例如波形音訊裝置）可以用來錄製。 如果您指定無法錄製的裝置，MCIWnd 會省略工具列中的 [ **記錄** ] 按鈕。

 

 

 




