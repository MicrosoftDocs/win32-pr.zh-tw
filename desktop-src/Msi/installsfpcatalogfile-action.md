---
description: InstallSFPCatalogFile 動作會安裝 Windows Me 用來 Windows 檔案保護的目錄。
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: InstallSFPCatalogFile 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f3992a64e5e3150759fdbc2c8221e6bd8672a2c75e72343280fb3e552f3cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787008"
---
# <a name="installsfpcatalogfile-action"></a>InstallSFPCatalogFile 動作

InstallSFPCatalogFile 動作會安裝 Windows Me 用來 Windows 檔案保護的目錄。 InstallSFPCatalogFile 會查詢 [Component 資料表](component-table.md)、 [File table](file-table.md)、 [FileSFPCatalog table](filesfpcatalog-table.md) 和 [SFPCatalog 資料表](sfpcatalog-table.md)。 如果目錄與元件中針對本機安裝所設定的檔案相關聯，或是與在本機安裝的元件中修復的檔案相關聯，就會安裝目錄。

## <a name="sequence-restrictions"></a>順序限制

InstallSFPCatalogFile 動作必須在 [InstallFiles](installfiles-action.md) 之前和 [CostFinalize](costfinalize-action.md)之後排序。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                                    |
|-------|---------------------------------------------------------------|
| \[1\] | 要安裝的目錄名稱。                          |
| \[2\] | 此目錄安裝所依據的目錄名稱。 |



 

## <a name="remarks"></a>備註

相依于在父類別目錄之後安裝之其他目錄的目錄。

 

 



