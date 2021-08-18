---
description: SetODBCFolders 動作會檢查系統上是否有現有的 ODBC 驅動程式，並將每個新驅動程式的目標目錄設定為現有驅動程式的位置。
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: SetODBCFolders 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceaefc2e9722b82ab0753c46b9e1e85a0ab3628a83b9f3abe66cf183c543fbe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628638"
---
# <a name="setodbcfolders-action"></a>SetODBCFolders 動作

SetODBCFolders 動作會檢查系統上是否有現有的 ODBC 驅動程式，並將每個新驅動程式的目標目錄設定為現有驅動程式的位置。

## <a name="sequence-restrictions"></a>順序限制

SetODBCFolders 動作必須在 [CostFinalize 動作](costfinalize-action.md) 之後，以及在 [InstallValidate 動作](installvalidate-action.md)之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                                                          |
|-------|-------------------------------------------------------------------------------------|
| \[1\] | 驅動程式描述。 ODBC 驅動程式金鑰。                                            |
| \[2\] | 新驅動程式的原始檔案夾位置。                                         |
| \[3\] | 新驅動程式的新資料夾位置。 這是現有驅動程式的位置。 |



 

## <a name="remarks"></a>備註

此動作會將新的驅動程式放入與要取代之現有驅動程式相同的目錄中。 SetODBCFolders 動作會使用 [目錄資料表](directory-table.md) 來設定即將取代之現有驅動程式的位置。

 

 



