---
description: '\_ \_ 當安裝程式提示使用者插入 cd-rom 時，就會有 MsiPromptForCD Mutex。'
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba2c829cb0102192b4c2bc2670892f8849000a6ed9cad2a88e7f3e3e557b259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764288"
---
# <a name="__msipromptforcd-mutex"></a>\_\_MsiPromptForCD Mutex

\_ \_ 當安裝程式提示使用者插入 cd-rom 時，就會有 MsiPromptForCD Mutex。 自動播放程式應該會在 \_ \_ 開始之前，檢查 MsiPromptForCD mutex 目前未設定。 請注意，在進行 InProgress 按鍵或 MSIExecute Mutex 之前，可能會出現 CD-ROM 提示 \_ 。

 

 



