---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型35。
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: 自訂動作類型35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a724fa5a7fc469ea688c64e5935242f088c010da02d963f2f1dc4b05f5eb5e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947966"
---
# <a name="custom-action-type-35"></a>自訂動作類型35

此自訂動作會從格式化的文字字串設定安裝目錄。 如需詳細資訊，請參閱 [變更目錄的目標位置。](changing-the-target-location-for-a-directory.md)

## <a name="source"></a>來源

[CustomAction 資料表](customaction-table.md)的來源欄位包含[目錄資料表](directory-table.md)的索引鍵。 指定的目錄是使用 [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)，以目標欄位中的格式化字串來設定。 這會將目標路徑和相關聯的屬性設定為目標欄位中格式化文字字串的展開值。 在 [維護安裝](maintenance-installation.md)期間，請勿嘗試變更目標目錄的位置。 如果已針對任何使用者安裝使用該路徑的某些元件，請不要嘗試變更目標目錄路徑。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定基本的數數值型別。



| 常數                                                              | 十六進位 | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  + **msidbCustomActionTypeDirectory** | 0x023       | 35      |



 

## <a name="target"></a>目標

[CustomAction 資料表](customaction-table.md)的目標資料行包含使用 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (中指定的功能來格式化的文字字串，而不含數值欄位規範) 。 要取代的參數會以方括弧括住 \[ \] ，而且可能是屬性、環境變數 (% prefix) 、檔案路徑 (\# 首碼) 或元件目錄路徑 ($ prefix) 。 請注意，目錄路徑一律以目錄分隔符號結尾。

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

 

 



