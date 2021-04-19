---
description: 自訂動作 ProcessAccounts 和 UninstallAccounts 會產生延遲的自訂動作，以建立、移除或回復使用者帳戶。
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: 撰寫 InstallExecuteSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974415"
---
# <a name="authoring-the-installexecutesequence-table"></a>撰寫 InstallExecuteSequence 資料表

自訂動作 ProcessAccounts 和 UninstallAccounts 會產生延遲的自訂動作，以建立、移除或回復使用者帳戶。 您必須在要執行的 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 中輸入自訂動作 ProcessAccounts 和 UninstallAccounts。 將下列專案加入至 [InstallExecuteSequence 資料表](installexecutesequence-table.md)。 因為這些自訂動作必須是腳本產生的一部分，所以必須在 [InstallInitialize 動作](installinitialize-action.md)之後排序這兩個自訂動作。

ProcessAccounts 上的條件可確保下列各項。 請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

-   只有在元件 TestAccount 是在本機電腦上安裝時，才會執行 ProcessAccounts。
-   元件測試帳戶目前未安裝，或已安裝成從來源執行。

UninstallAccount 上的條件可確保下列各項：

-   只有在元件 TestAccount 是安裝在本機電腦上時，才會執行 UninstallAccounts。
-   元件測試帳戶正在移除，或已安裝成從來源執行。

[InstallExecuteSequence 資料表](installexecutesequence-table.md)



| 動作            | 條件                                                           | 順序 |
|-------------------|---------------------------------------------------------------------|----------|
| ProcessAccounts   | VersionNT 和 (？TestAccount = 2 或？TestAccount = 4) 且 $TestAccount = 3 | 1550     |
| UninstallAccounts | VersionNT 嗎？TestAccount = 3， ($TestAccount = 4 或 $TestAccount = 2)  | 1560     |



 

繼續 [撰寫密碼輸入的使用者介面](authoring-the-user-interface-for-password-input.md)。

 

 



