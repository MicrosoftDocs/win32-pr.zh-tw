---
description: 當標準動作不足以執行安裝時，Windows Installer 套件的開發人員可能會選擇使用自訂動作類型22。
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: 自訂動作類型22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe14690ec1d966abfe1ead0b7856360270570f30e2aaf2e93ea81181962ec8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637902"
---
# <a name="custom-action-type-22"></a>自訂動作類型22

此自訂動作是以 VBScript 撰寫的。 另請參閱 [腳本](scripts.md)。

## <a name="source"></a>來源

腳本會在目前的會話期間與應用程式一起安裝。 [CustomAction 資料表](customaction-table.md)的來源欄位包含檔案[資料表](file-table.md)的索引鍵。 自訂動作程式碼的位置取決於此檔案的目標路徑解析;因此，必須在安裝檔案之後以及移除之前呼叫這個自訂動作。

## <a name="type-value"></a>類型值

在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定32位自訂動作的基本數數值型別。



| 常數                                                               | 十六進位 | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeSourceFile** | 0x016       | 22      |



 

Windows安裝程式可能會在64位作業系統上使用64位自訂動作。 以腳本為基礎的64位自訂動作必須在其數數值型別中包含 **msidbCustomActionType64BitScript** 位。 如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。 在 [CustomAction 資料表](customaction-table.md) 的 Type 資料行中包含下列值，以指定64位自訂動作的基本數數值型別。



| 常數                                                                                                      | 十六進位 | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  + **msidbCustomActionTypeSourceFile**  + **msidbCustomActionType64BitScript** | 0x0001016   | 4118    |



 

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

以 JScript 或 VBScript 撰寫的自訂動作需要安裝 [**會話物件**](session-object.md)。 這是 **Session 物件** 類型，而安裝程式會將它附加至名稱為 "Session" 的腳本。 因為 **會話** 物件在安裝復原期間可能不存在，所以在腳本中撰寫的延遲自訂動作必須使用在 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)一節中所述之 **會話** 物件的其中一個方法或屬性，以取得其內容。

參考已安裝檔案作為其來源的自訂動作（例如自訂動作類型 22 (VBcript) ）必須遵守下列排序限制：

-   自訂動作必須在 [CostFinalize 動作](costfinalize-action.md)之後排序。 如此一來，自訂動作就可以解析找出包含 VBScript 的原始程式檔所需的路徑。
-   如果來源檔案尚未安裝在電腦上，則必須在 [InstallFiles 動作](installfiles-action.md)之後，將此類型的自訂動作延遲 (腳本內) 自訂動作。
-   如果來源檔案尚未安裝在電腦上，則必須在 [InstallFinalize 動作](installfinalize-action.md)之後排序此類型的非延遲自訂動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂 \_ 動作](custom-actions.md)
</dt> </dl>

 

 



