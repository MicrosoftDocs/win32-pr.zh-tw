---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型38。
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: 自訂動作類型38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9372cd5035d27c02feaef3ed455ddeb756c449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944762"
---
# <a name="custom-action-type-38"></a>自訂動作類型38

此自訂動作是以 VBScript 撰寫的。 另請參閱 [腳本](scripts.md)。

## <a name="source"></a>來源

[CustomAction 資料表](customaction-table.md)的來源欄位包含 null 值。 自訂動作的腳本程式碼會以常值腳本文字的字串儲存在目標欄位中。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。



| 常數                                                              | 十六進位 | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeDirectory** | 0x026       | 38      |



 

Windows Installer 可以在64位作業系統上使用64位自訂動作。 以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。 如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。 在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。



| 常數                                                                                                     | 十六進位 | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeDirectory**  + **msidbCustomActionType64BitScript** | 0x0001026   | 4134    |



 

## <a name="target"></a>目標

[CustomAction 資料表](customaction-table.md)的 [目標] 欄位包含自訂動作的腳本程式碼，做為常值腳本文字的字串。

## <a name="return-processing-options"></a>傳回處理選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定傳回處理選項。 如需選項和值的描述，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。

## <a name="execution-scheduling-options"></a>執行排程選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定執行排程選項。 這些選項控制多個自訂動作的執行。 如需選項的描述，請參閱 [自訂動作執行排程選項](custom-action-execution-scheduling-options.md)。

## <a name="in-script-execution-options"></a>In-Script 執行選項

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含選擇性旗標位，以指定腳本內執行選項。 這些選項會將動作程式碼複製到執行、復原或認可腳本中。 如需選項的描述，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

## <a name="return-values"></a>傳回值

此自訂動作類型一律會傳回成功。

## <a name="remarks"></a>備註

以 JScript 或 VBScript 撰寫的自訂動作需要安裝 [**會話**](session-object.md) 物件。 安裝程式會將 **會話物件** 附加至名稱為 "Session" 的腳本。 因為 **會話** 物件在安裝復原期間可能不存在，所以在腳本中撰寫的延遲自訂動作必須使用在 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)一節中所述之 **會話** 物件的其中一個方法或屬性，以取得其內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> </dl>

 

 



