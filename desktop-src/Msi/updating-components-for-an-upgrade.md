---
description: 根據設計，虛構 MNP2000 產品的使用者絕對不應該使用升級的檔案，例如 Baseba01.txt。
ms.assetid: 5aca7ff5-c09f-4d00-b319-2b89550686ab
title: 更新升級的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 920bc955d3d3615941ef03ec885ca8871f79dc86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944973"
---
# <a name="updating-components-for-an-upgrade"></a>更新升級的元件

根據設計，虛構 MNP2000 產品的使用者絕對不應該使用升級的檔案，例如 Baseba01.txt。 因此，更新的檔案與原始產品的定義不相容，且 Windows Installer 的元件（例如棒球）必須指派新的元件碼。 新的檔案（例如 Opera01.txt）會以唯一的元件程式碼導入成為新元件的一部分。 因為原始產品和升級使用相同的「記事本」元件，所以這個元件的元件程式碼不會改變。 如需何時必須變更元件程式碼的詳細資訊，請參閱 [變更元件程式碼](changing-the-component-code.md)。

使用 Orca 或其他資料庫編輯器，在 MNP2001.msi 的 [元件資料表](component-table.md) 中輸入下列資料。 請勿在範例的 [元件] 資料行中重複使用如下所示的 Guid。

[元件資料表](component-table.md)



| 元件  | ComponentId                            | 目錄\_ | 屬性 | 條件 | Keypath      |
|------------|----------------------------------------|-------------|------------|-----------|--------------|
| 棒球   | {2951190A-6AF8-4D7F-AA16-D256405C277A} | SPORTDIR    | 2          |           | Baseba01.txt |
| 籃球 | {E1AAB6B0-FEC6-4F18-B765-3B05A81CEACB} | SPORTDIR    | 2          |           | Basket01.txt |
| 演唱會    | {C28C5064-AA84-4431-AC69-FC1321DF18AF} | ARTSDIR     | 2          |           | Concer01.txt |
| 舞蹈      | {1AC2B14D-D5F4-4642-9F7A-EE81BF59B3E2} | ARTSDIR     | 2          |           | Dance01.txt  |
| Opera      | {C2DABF7E-1EF6-458D-84B1-AAC1127CED26} | ARTSDIR     | 2          |           | Opera01.txt  |
| 足球   | {92AA30F4-7AC5-4DFA-801E-988CF3DAA4DC} | SPORTDIR    | 2          |           | Footba01.txt |
| Help       | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| 一月    | {E90CD0E6-ED8D-4F88-B000-27BD2B482C6C} | MONDIR      | 2          |           | Janua01.txt  |
| NewYears   | {1EEF8C53-F7C0-405C-8FE3-2B0FE54B0114} | HOLDIR      | 2          |           | NewYea01.txt |
| 紀念   | {BA81ACF7-4D43-424F-93B0-8845A2DF1C02} | HOLDIR      | 2          |           | Memori01.txt |
| [記事本]    | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

[繼續](updating-features-for-an-upgrade.md)

 

 



