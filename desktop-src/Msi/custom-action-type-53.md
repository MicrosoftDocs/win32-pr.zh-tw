---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型53。
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: 自訂動作類型53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b78c2dbc8aa233175eeacfa8d16521968dfceeb6b97504e639946c6284b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947889"
---
# <a name="custom-action-type-53"></a>自訂動作類型53

此自訂動作是以 JScript （例如 ECMA 262）來撰寫。 Windows安裝程式不支援 JScript 1.0。 如需詳細資訊，請參閱 [腳本](scripts.md)。

## <a name="source"></a>來源

[CustomAction 資料表](customaction-table.md)的 [來源] 欄位包含屬性名稱，或是包含腳本文字之屬性的[屬性工作表](property-table.md)索引鍵。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。



| 常數                                                            | 十六進位 | Decimal |
|----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  + **msidbCustomActionTypeProperty** | 0x035       | 53      |



 

Windows安裝程式可能會在64位作業系統上使用64位自訂動作。 以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。 如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。 在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。



| 常數                                                                                                   | 十六進位 | Decimal |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  + **msidbCustomActionTypeProperty**  + **msidbCustomActionType64BitScript** | 0x0001035   | 4149    |



 

## <a name="target"></a>目標

[CustomAction 資料表](customaction-table.md)的目標欄位包含選擇性腳本函數。 處理會先傳送腳本進行剖析，然後呼叫選擇性腳本函數。

## <a name="return-processing-options"></a>傳回處理選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。 如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

## <a name="execution-scheduling-options"></a>執行排程選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。 這些選項控制多個自訂動作的執行。 如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。

## <a name="in-script-execution-options"></a>In-Script 執行選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。 這些選項會將動作程式碼複製到執行、復原或認可腳本中。 如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

## <a name="return-values"></a>傳回值

以腳本撰寫的選擇性函式必須傳回[JScript 和 VBScript 自訂動作](return-values-of-jscript-and-vbscript-custom-actions.md)的傳回值中所述的其中一個值。

## <a name="remarks"></a>備註

在 JScript 中撰寫的自訂動作需要安裝 [**會話**](session-object.md)物件。 因為 **會話** 物件在安裝復原期間可能不存在，所以以腳本撰寫的延遲自訂動作會使用 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)中所述的其中一個方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> </dl>

 

 



