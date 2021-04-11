---
description: 範例規格包括在自訂動作建立或移除使用者帳戶時傳送 ActionData 訊息，以及在無法建立帳戶時報告錯誤。
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: 撰寫 ActionText 和錯誤資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848958"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>撰寫 ActionText 和錯誤資料表

範例規格包括在自訂動作建立或移除使用者帳戶時傳送 ActionData 訊息，以及在無法建立帳戶時報告錯誤。

在 ActionText 資料表中輸入下列專案，以提供 ActionText 訊息所使用的資訊。

[ActionText 資料表](actiontext-table.md)



| 動作            | 描述                                                       | 範本                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| ProcessAccounts   | 正在產生可在本機電腦上建立使用者帳戶的動作。 | 帳戶： \[ 1 \] ，屬性： \[ 2\] |
| CreateAccount     | 在本機電腦上建立使用者帳戶。                      | 帳戶： \[ 1\]                    |
| RemoveAccount     | 正在從本機電腦移除使用者帳戶。                    | 帳戶： \[ 1\]                    |
| RollbackAccount   | 正在復原在本機電腦上建立使用者帳戶。 | 帳戶： \[ 1\]                    |
| UninstallAccounts | 產生動作以移除本機電腦上的使用者帳戶。 | 帳戶： \[ 1\]                    |



 

在錯誤資料表中輸入下列專案，以提供錯誤報表所使用的資訊。

[錯誤資料表](error-table.md)



| 錯誤 | 訊息                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | 無法 \[ 在本機電腦上建立使用者帳戶 ' 2 \] '。 錯誤碼： \[ 3 \] 。 |
| 25002 | \[ \] 本機電腦上已有使用者帳戶 ' 2 '。                      |
| 25003 | 無法移除 \[ \] 本機電腦上的使用者帳戶 ' 2 '。 錯誤碼： \[ 3 \] 。 |
| 25004 | 使用者帳戶 ' \[ 2 \] ' 不存在於本機電腦上。                      |



 

繼續 [撰寫 InstallExecuteSequence 資料表](authoring-the-installexecutesequence-table.md)。

 

 



