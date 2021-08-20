---
description: 如果 wua 應用程式是在次要登入服務的內容中執行，則 Windows Update 代理程式 (wua) 應用程式無法安裝需要使用者互動的更新。
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: 從次要登入使用 WUA (以) 進程的方式執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a659b9c46429100393138751039fdc1ce529191970a35c76d36e45bb16eb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049086"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>從次要登入使用 WUA (以) 進程的方式執行

如果 wua 應用程式是在次要登入服務的內容中執行，則 Windows Update 代理程式 (wua) 應用程式無法安裝需要使用者互動的更新。

如果呼叫 WUA 的進程是在 RunAs 服務或次要登入服務的內容中執行，則嘗試安裝需要使用者互動的更新會失敗，並傳回 **WU \_ 電子 \_ 沒有 \_ 互動式 \_ 使用者** 錯誤。

在 Microsoft Windows 中，您可以使用與目前登入的使用者不同的使用者身分來執行程式。 若要這樣做，次要登入服務必須正在執行。

 

 



