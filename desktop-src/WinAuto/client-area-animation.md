---
title: 用戶端區域動畫參數
description: 用戶端區域動畫旗標會指出使用者是否想要停用 UI 元素中的動畫。
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4d451424da0a02fa55efaead05ab285b3f07936167bb6e4376de4fd25ae11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325957"
---
# <a name="client-area-animation-parameter"></a>用戶端區域動畫參數

用戶端區域動畫參數會指出使用者是否想要停用 UI 元素中的動畫。 顯示功能（例如閃爍、閃爍、閃爍和移動內容）可能會在具有相片相關癲癇的使用者中造成 seizures。 此參數可讓您啟用或停用所有這類動畫。

應用程式會使用 **spi \_ GETCLIENTAREAANIMATION** 和 **spi \_ SETCLIENTAREAANIMATION** 旗標搭配 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式，來開啟或關閉用戶端區域動畫。

 

 