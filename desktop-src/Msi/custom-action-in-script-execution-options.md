---
description: 您可以使用下列選項旗標來指定自訂動作的腳本執行。
ms.assetid: 6c608151-cdbe-4424-9b16-6dbff28190ab
title: 自訂動作 In-Script 執行選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f779d117196164a1c0738a6cee3aa48b3b0a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994568"
---
# <a name="custom-action-in-script-execution-options"></a>自訂動作 In-Script 執行選項

您可以使用下列選項旗標來指定自訂動作的腳本執行。 這些選項會將動作程式碼複製到執行、復原或認可腳本中。 若要設定選項，請將此資料表中的值加入至 [CustomAction 資料表](customaction-table.md)之 [類型] 欄位中的值。

請注意，每個選項都必須包含 **msidbCustomActionTypeInScript** 。



| 詞彙                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_none_"></span><span id="_NONE_"></span> (無) <br/>                                                                                                                                                                                                                                                                                                                                                                                                                      | 十六進位：0x00000000<br/> Decimal：0<br/> 立即執行。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="msidbCustomActionTypeInScript"></span><span id="msidbcustomactiontypeinscript"></span><span id="MSIDBCUSTOMACTIONTYPEINSCRIPT"></span>**msidbCustomActionTypeInScript**<br/>                                                                                                                                                                                                                                                                                             | 十六進位：0x00000400<br/> Decimal：1024<br/> 在腳本中排程點執行的佇列。 此旗標指定這是 [延後執行自訂動作](deferred-execution-custom-actions.md)。<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="msidbCustomActionTypeInScript____msidbCustomActionTypeRollback"></span><span id="msidbcustomactiontypeinscript____msidbcustomactiontyperollback"></span><span id="MSIDBCUSTOMACTIONTYPEINSCRIPT____MSIDBCUSTOMACTIONTYPEROLLBACK"></span>**msidbCustomActionTypeInScript**  + **msidbCustomActionTypeRollback**<br/>                                                                                                                                                      | 十六進位： 0x00000400 + 0x00000100<br/> Decimal：1280<br/> 在腳本中排程點執行的佇列。 只有在安裝復原時才會執行。 此旗標指定這是 [復原自訂動作](rollback-custom-actions.md)。<br/>                                                                                                                                                                                                                                                                             |
| <span id="msidbCustomActionTypeInScript____msidbCustomActionTypeCommit"></span><span id="msidbcustomactiontypeinscript____msidbcustomactiontypecommit"></span><span id="MSIDBCUSTOMACTIONTYPEINSCRIPT____MSIDBCUSTOMACTIONTYPECOMMIT"></span>**msidbCustomActionTypeInScript**  + **msidbCustomActionTypeCommit**<br/>                                                                                                                                                              | 十六進位： 0x00000400 + 0x00000200<br/> Decimal：1536<br/> 在腳本中排程點執行的佇列。 只有在安裝認可時才會執行。 此旗標指定這是 [認可自訂動作](commit-custom-actions.md)。<br/>                                                                                                                                                                                                                                                                                           |
| <span id="msidbCustomActionTypeInScript___msidbCustomActionTypeNoImpersonate"></span><span id="msidbcustomactiontypeinscript___msidbcustomactiontypenoimpersonate"></span><span id="MSIDBCUSTOMACTIONTYPEINSCRIPT___MSIDBCUSTOMACTIONTYPENOIMPERSONATE"></span>**msidbCustomActionTypeInScript**  + **msidbCustomActionTypeNoImpersonate**<br/>                                                                                                                                     | 十六進位： 0x00000400 + 0x00000800<br/> Decimal：3072<br/> 在腳本中排程點執行的佇列。 執行，不使用使用者模擬。 在系統內容中執行。<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="msidbCustomActionTypeInScript___msidbCustomActionTypeNoImpersonate___msidbCustomActionTypeRollback"></span><span id="msidbcustomactiontypeinscript___msidbcustomactiontypenoimpersonate___msidbcustomactiontyperollback"></span><span id="MSIDBCUSTOMACTIONTYPEINSCRIPT___MSIDBCUSTOMACTIONTYPENOIMPERSONATE___MSIDBCUSTOMACTIONTYPEROLLBACK"></span>**msidbCustomActionTypeInScript**  + **msidbCustomActionTypeNoImpersonate**  + **msidbCustomActionTypeRollback**<br/> | 十六進位： 0x00000400 + 0x00000800 + 0x00000100<br/> Decimal：3328<br/> 在腳本中排程點執行的佇列。 執行，不使用使用者模擬。 在系統內容中執行。 此旗標組合指定這是 [復原自訂動作](rollback-custom-actions.md)。<br/>                                                                                                                                                                                                                                    |
| <span id="msidbCustomActionTypeInScript___msidbCustomActionTypeNoImpersonate___msidbCustomActionTypeCommit"></span><span id="msidbcustomactiontypeinscript___msidbcustomactiontypenoimpersonate___msidbcustomactiontypecommit"></span><span id="MSIDBCUSTOMACTIONTYPEINSCRIPT___MSIDBCUSTOMACTIONTYPENOIMPERSONATE___MSIDBCUSTOMACTIONTYPECOMMIT"></span>**msidbCustomActionTypeInScript**  + **msidbCustomActionTypeNoImpersonate**  + **msidbCustomActionTypeCommit**<br/>         | 十六進位： 0x00000400 + 0x00000800 + 0x00000200<br/> Decimal：3584<br/> 在腳本中排程點執行的佇列。 執行，不使用使用者模擬。 在系統內容中執行。 此旗標組合指定這是 [認可自訂動作](commit-custom-actions.md)。<br/>                                                                                                                                                                                                                                        |
| <span id="msidbCustomActionTypeTSAware___msidbCustomActionTypeInScript"></span><span id="msidbcustomactiontypetsaware___msidbcustomactiontypeinscript"></span><span id="MSIDBCUSTOMACTIONTYPETSAWARE___MSIDBCUSTOMACTIONTYPEINSCRIPT"></span>**msidbCustomActionTypeTSAware**  + **msidbCustomActionTypeInScript**<br/>                                                                                                                                                             | 十六進位： 0x00000400 + 0x00004000<br/> Decimal：17408<br/> 在腳本中排程點執行的佇列。 使用使用者模擬來執行。 在執行終端機伺服器角色服務的伺服器上進行每部電腦安裝時，以使用者模擬的方式執行。 一般的順延強制自訂動作（沒有此屬性）在每部電腦安裝期間不會在終端機伺服器上執行任何使用者模擬。 如果動作也有 msidbCustomActionTypeNoImpersonate 屬性，則這個屬性不會有任何作用。<br/> |
| <span id="msidbCustomActionTypeTSAware___msidbCustomActionTypeInScript___msidbCustomActionTypeRollback"></span><span id="msidbcustomactiontypetsaware___msidbcustomactiontypeinscript___msidbcustomactiontyperollback"></span><span id="MSIDBCUSTOMACTIONTYPETSAWARE___MSIDBCUSTOMACTIONTYPEINSCRIPT___MSIDBCUSTOMACTIONTYPEROLLBACK"></span>**msidbCustomActionTypeTSAware**  + **msidbCustomActionTypeInScript**  + **msidbCustomActionTypeRollback**<br/>                         | 十六進位： 0x00000400 + 0x00004000 + 0x00000100<br/> Decimal：17664<br/> 在腳本中排程點執行的佇列。 只有在安裝復原時才執行。 以使用者模擬執行。 在終端機伺服器上進行個別電腦安裝時，以使用者模擬的方式執行。<br/>                                                                                                                                                                                                                                           |
| <span id="msidbCustomActionTypeTSAware___msidbCustomActionTypeInScript___msidbCustomActionTypeCommit"></span><span id="msidbcustomactiontypetsaware___msidbcustomactiontypeinscript___msidbcustomactiontypecommit"></span><span id="MSIDBCUSTOMACTIONTYPETSAWARE___MSIDBCUSTOMACTIONTYPEINSCRIPT___MSIDBCUSTOMACTIONTYPECOMMIT"></span>**msidbCustomActionTypeTSAware**  + **msidbCustomActionTypeInScript**  + **msidbCustomActionTypeCommit**<br/>                                 | 十六進位： 0x00000400 + 0x00004000 + 0x00000200<br/> Decimal：17920<br/> 在腳本中排程點執行的佇列。 只有在安裝認可時才會執行。 使用使用者模擬來執行。 在終端機伺服器上進行個別電腦安裝時，以使用者模擬的方式執行。<br/>                                                                                                                                                                                                                                                |



 

如需只在卸載修補程式時執行的自訂動作相關資訊，請參閱 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂動作參考](custom-action-reference.md)
</dt> <dt>

[關於自訂動作](about-custom-actions.md)
</dt> <dt>

[使用自訂動作](using-custom-actions.md)
</dt> </dl>

 

 




