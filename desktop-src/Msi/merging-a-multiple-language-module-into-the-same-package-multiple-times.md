---
description: 當模組支援多種語言時，您可以將它合併到相同的 Windows Installer 資料庫多次，但請確定每個合併都使用不同的語言。
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: 將多個語言模組合併成相同的封裝多次
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a96f3830b2caa4069eddc69b0b68de1deff35d00c5b4fdb81d4d21d4355bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129258"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a>將多個語言模組合併成相同的封裝多次

當模組支援多種語言時，您可以將它合併到相同的 Windows Installer 資料庫多次，但請確定每個合併都使用不同的語言。 在每次合併之前，請向模組要求不同的語言。 產生的 .msi 資料庫在每個模組合併的 [ModuleSignature 資料表](modulesignature-table.md) 中都會有一筆記錄。 在語言之間共用的元件只會在 [元件資料表](component-table.md)中存在一次，但會與 [ModuleComponents 資料表](modulecomponents-table.md)中的每個語言相關聯。

將模組的多個語言合併成相同的封裝時，每個合併都必須滿足與單一語言模組相同的字碼頁限制。 這些模組不能包含不同字碼頁中的字串。

將模組多次合併成單一 .msi 檔案時，您可能需要修改檔案 [資料表](file-table.md) 中檔案的順序，以直接在安裝中使用模組中的現有 .cab。 檔案資料表中的檔案順序必須符合 .cab 中的檔案順序。 將模組多次合併到安裝資料庫時，可能會修改序列，因為語言之間共用的檔案可能已存在於先前合併的模組中，而且具有不同的相對序號。

 

 



