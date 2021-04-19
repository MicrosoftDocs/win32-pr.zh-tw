---
description: 使用這些函數可在 Windows Installer 資料庫的目錄資料表中，尋找指定資料夾的來源或目標。
ms.assetid: 8f9971da-cca8-4623-bdd2-079c4f4859f9
title: 使用資料夾位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22485f7bf0ae2a680c9a0bf52eb9fe62858acf09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971870"
---
# <a name="working-with-folder-locations"></a>使用資料夾位置

使用下列函式來尋找 [目錄資料表](directory-table.md)中指定之資料夾的來源或目標：

-   藉由呼叫 [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) 函數，取得指定之源資料夾的路徑。
-   藉由呼叫 [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) 函式來取得指定之目的檔案夾的路徑。
-   使用 [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) 函數來變更資料夾的目標位置。

 

 



