---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型51。
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: 自訂動作類型51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e780c1a38b60c855f4bfe665f5f68a3f6a037a078f4a2875d1a2ea57c5e7e8dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075048"
---
# <a name="custom-action-type-51"></a>自訂動作類型51

此自訂動作會從格式化的文字字串設定屬性。

若要影響元件或功能的條件中所使用的屬性，自訂動作必須在動作順序中的 [CostFinalize 動作](costfinalize-action.md) 之前。

## <a name="source"></a>來源

[CustomAction 資料表](customaction-table.md)的來源欄位可以包含屬性的名稱或[屬性資料表](property-table.md)的索引鍵。 這個屬性是由目標欄位中使用 [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)的格式化字串所設定。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。



| 常數                                                             | 十六進位 | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  + **msidbCustomActionTypeProperty** | 0x033       | 51      |



 

## <a name="target"></a>目標

[CustomAction 資料表](customaction-table.md)的目標資料行包含使用 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (中指定的功能來格式化的文字字串，而不含數值欄位規範) 。 要取代的參數會以方括弧（...）括住， \[ \] 而且可能是屬性、環境變數 (% prefix) 、檔案路徑 (\# 首碼) 或元件目錄路徑 ($ prefix) 。

## <a name="return-processing-options"></a>傳回處理選項

自訂動作不會使用這些選項。

## <a name="execution-scheduling-options"></a>執行排程選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。 這些選項控制多個自訂動作的執行。 如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。

## <a name="in-script-execution-options"></a>In-Script 執行選項

自訂動作不會使用這些選項。

## <a name="return-values"></a>傳回值

請參閱 [自訂動作傳回值](custom-action-return-values.md)。

## <a name="remarks"></a>備註

如果您在 UI 序列中，藉由在其中一個使用者介面順序資料表中撰寫自訂動作來設定 [私用屬性](private-properties.md) ，該屬性就不會在執行順序中設定。 若要在執行順序中設定屬性，您也必須在執行順序資料表中放置自訂動作。 或者，您可以將屬性設為 [公用屬性](public-properties.md) ，並將它包含在 [**SecureCustomProperties 屬性**](securecustomproperties.md)中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> <dt>

[格式化的文本自訂動作](formatted-text-custom-actions.md)
</dt> </dl>

 

 



