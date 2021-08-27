---
title: 檢查協助工具參數的狀態
description: 下列程式碼片段會使用 GetSystemMetrics 函式來檢查 [聲音] 參數。 如果 GetSystemMetrics 傳回 TRUE，則應用程式應該以視覺化形式呈現所有重要資訊。
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374520612ce96522edc1b879a49f5f30a9c7a857f9bb46a562a4ab48effebe9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122248"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>檢查協助工具參數的狀態

下列程式碼片段會使用 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式來檢查 [聲音] 參數。 如果 **GetSystemMetrics** 傳回 **TRUE**，則應用程式應該以視覺化形式呈現所有重要資訊。


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 