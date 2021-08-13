---
description: RMCCPSearch 動作會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: RMCCPSearch 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d18431a6806d055c824bf51331d6390a6f669100aa9a33db9665b9d7b37008c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625897"
---
# <a name="rmccpsearch-action"></a>RMCCPSearch 動作

RMCCPSearch 動作會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。

## <a name="sequence-restrictions"></a>順序限制

RMCCPSearch 動作應該撰寫到 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。 如果動作已在 InstallUISequence 序列中執行，則安裝程式會防止 RMCCPSearch 在 InstallExecuteSequence 序列中執行。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

RMCCPSearch 動作要求 [**CCP \_ 磁片磁碟機**](ccp-drive.md) 屬性必須設定為卸載式 [*磁片*](v-gly.md) 區上的根路徑，該磁片區具有任何合格產品的安裝。

在使用 [DrLocator](drlocator-table.md)資料表之 [**CCP \_ 磁片磁碟機**](ccp-drive.md)屬性所參考的路徑下，搜尋 CCPSearch 資料表中的每個檔案簽章。 簽 [章資料表缺少](signature-table.md) 簽章代表目錄。 如果有任何簽章確定存在，RMCCPSearch 動作就會終止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CCPSearch 資料表](ccpsearch-table.md)
</dt> </dl>

 

 



