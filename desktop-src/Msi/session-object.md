---
description: 會話物件會控制安裝程式。
ms.assetid: 013959d9-900c-45f7-b742-17b0365d6107
title: '會話物件 (Windows Installer) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c391249d5ccc58fe9a947c9db761a77521c9776d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997743"
---
# <a name="session-object-windows-installer"></a>會話物件 (Windows Installer) 

**會話** 物件會控制安裝程式。 它會開啟安裝程式資料庫，其中包含安裝資料表和資料。 這個物件與一組標準動作函式相關聯，每個都對一或多個資料表的資料執行特定作業。 您可以針對特定產品安裝新增額外的自訂動作。 基本引擎函數是從指定順序資料表中提取順序記錄、評估任何指定的條件運算式，並執行指定動作的 sequencer。 引擎無法辨識的動作會延後至 UI 處理常式物件以進行處理，通常是對話方塊序列。

請注意，單一進程只能開啟一個 **會話** 物件。

## <a name="members"></a>成員

**Session** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Session** 物件有這些方法。



| 方法                                                 | 描述                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dataadapter.doaction**](session-doaction.md)                   | 執行指定的動作。 <br/>                                                                                                                                                                                                                                |
| [**EvaluateCondition**](session-evaluatecondition.md) | 評估包含符號和值的邏輯運算式，並傳回列舉 msiEvaluateConditionErrorEnum 的整數。<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | 傳回 [**FeatureInfo**](featureinfo-object.md) 物件，其中包含指定功能的描述性資訊。<br/>                                                                                                                                       |
| [**FormatRecord**](session-formatrecord.md)           | 從範本和記錄資料傳回格式化的字串。<br/>                                                                                                                                                                                                      |
| [**消息**](session-message.md)                     | 執行任何已啟用的記錄作業，並順延強制與引擎相關聯的 UI 處理常式物件。<br/>                                                                                                                                              |
| [**序列**](session-sequence.md)                   | 在指定的資料表上開啟查詢，並依 [順序] 資料行中的數位排序動作。 針對每個提取的資料列，如果任何提供的條件運算式未評估為 False，則會呼叫 [**dataadapter.doaction**](session-doaction.md) 方法。<br/> |
| [**SetInstallLevel**](session-setinstalllevel.md)     | 將目前安裝的安裝層級設定為指定的值，並重新計算所有功能的 [選取] 和 [已安裝] 狀態。<br/>                                                                                                                    |



 

### <a name="properties"></a>屬性

**Session** 物件具有這些屬性。



| 屬性                                                                  | 存取類型           | Description                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComponentCosts**](session-componentcosts.md)<br/>               |                       | 傳回 [**RecordList**](recordlist-object.md) 物件，此物件會列舉安裝元件所需的每個磁片磁碟機的磁碟空間。<br/>                                  |
| [**ComponentCurrentState**](session-componentcurrentstate.md)<br/> |                       | 傳回指定元件目前已安裝的狀態。<br/>                                                                                                |
| [**ComponentRequestState**](session-componentrequeststate.md)<br/> |                       | 取得或要求元件資料表中資料列的動作狀態變更。<br/>                                                                               |
| [**資料庫**](session-database.md)<br/>                           |                       | 傳回目前安裝會話的資料庫。<br/>                                                                                                      |
| [**FeatureCost**](session-featurecost.md)<br/>                     |                       | 傳回指定功能所需的磁碟空間總量 (（以512位元組為單位）) ) 的功能資料表的根目錄 (。<br/> |
| [**FeatureCurrentState**](session-featurecurrentstate.md)<br/>     |                       | 傳回指定功能目前已安裝的狀態。<br/>                                                                                                  |
| [**FeatureRequestState**](session-featurerequeststate.md)<br/>     | 讀取/寫入<br/> | 取得或要求功能記錄和子記錄的選取狀態變更。<br/>                                                                          |
| [**FeatureValidStates**](session-featurevalidstates.md)<br/>       |                       | 傳回代表位旗標的整數，每個相關位表示指定功能的有效安裝狀態。<br/>                             |
| [**安裝程式**](session-installer.md)<br/>                         |                       | 傳回使用中的安裝程式物件。<br/>                                                                                                                            |
| [**Language (Session 物件)**](session-language.md)<br/>          |                       | 表示目前安裝會話所使用的數位語言識別項。<br/>                                                                            |
| [**模式**](session-mode.md)<br/>                                   |                       | 這個屬性是一個值，代表目前安裝會話的指定模式旗標。<br/>                                                            |
| [**ProductProperty**](session-productproperty.md)<br/>             |                       | 表示命名安裝程式屬性的字串值。<br/>                                                                                                      |
| [**屬性 (會話物件)**](session-session.md)<br/>           | 讀取/寫入<br/> | 從產品資料庫抓取產品屬性。<br/>                                                                                                         |
| [**SourcePath**](session-sourcepath.md)<br/>                       |                       | 提供來源媒體或伺服器映射上指定之資料夾的完整路徑。<br/>                                                                            |
| [**TargetPath**](session-targetpath.md)<br/>                       | 讀取/寫入<br/> | 提供安裝目標磁片磁碟機上所指定資料夾的完整路徑。<br/>                                                                               |
| [**VerifyDiskSpace**](session-verifydiskspace.md)<br/>             |                       | 如果有足夠的磁碟空間，則傳回 true，如果磁片已滿，則傳回 false。<br/>                                                                                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows Installer 腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




