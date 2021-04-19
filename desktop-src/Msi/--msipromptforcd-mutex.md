---
description: '\_ \_ 當安裝程式提示使用者插入 cd-rom 時，就會有 MsiPromptForCD Mutex。'
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e646b23a003d10cce29807297e56abaebf3d935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975054"
---
# <a name="__msipromptforcd-mutex"></a>\_\_MsiPromptForCD Mutex

\_ \_ 當安裝程式提示使用者插入 cd-rom 時，就會有 MsiPromptForCD Mutex。 自動播放程式應該會在 \_ \_ 開始之前，檢查 MsiPromptForCD mutex 目前未設定。 請注意，在進行 InProgress 按鍵或 MSIExecute Mutex 之前，可能會出現 CD-ROM 提示 \_ 。

 

 



