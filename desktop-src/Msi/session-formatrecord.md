---
description: Session 物件的 FormatRecord 方法會從範本傳回格式化的字串，並記錄資料。
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: FormatRecord 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992912"
---
# <a name="sessionformatrecord-method"></a>FormatRecord 方法

[**Session**](session-object.md)物件的 **FormatRecord** 方法會從範本傳回格式化的字串，並記錄資料。

## <a name="syntax"></a>語法


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*記錄* 
</dt> <dd>

必要的 **記錄** 物件，其中包含要格式化的範本和資料。 您必須在欄位0中設定範本字串，後面接著任何參考的資料參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**FormatRecord** 方法會使用下列格式進程。

要[格式化](formatted.md)的參數會以方括弧括住 \[ ... \] 可以反復執行方括弧，因為會從外部解析出替代。

如果字串的一部分是以大括弧 {} 括住，且未包含方括弧，則部分會保持不變，包括大括弧。

如果字串的一部分是以大括弧括住，且包含一或多個屬性名稱，而且如果找到所有屬性，則會顯示具有已解析之替代的文字 () 不含大括弧。 如果找不到任何屬性，則會移除大括弧和大括弧本身中的所有文字。

**若要使用 FormatRecord 方法將字串格式化**

1.  藉由將標記取代為對應的 [記錄] 欄位的值，並在不產生任何文字的情況下，使用遺漏或 Null 值來取代數值參數。
2.  藉由以對應的值取代非記錄參數來處理結果的字串，如下列描述所述。
    -   如果遇到 "propertyname" 格式的子字串，則會 \[ \] 由屬性的值取代。
    -   如果找到 "% environmentvariable" 格式的子字串 \[ \] ，則會取代環境變數的值。
    -   如果找到 filekey 格式的子字串，則會以檔案的 \[ \#  \] 完整路徑來取代它，而值 *filekey* 會用來做為檔案 [資料表](file-table.md)中的索引鍵。 Filekey 的值 \[ \#  \] 會保持空白，而且在安裝程式執行[CostInitialize 動作](costinitialize-action.md)、 [FileCost 動作](filecost-action.md)和[CostFinalize 動作](costfinalize-action.md)之前，不會由路徑取代。 Filekey 的值 \[ \#  \] 取決於檔案所屬元件的安裝狀態。 如果元件是從來源執行，則此值為檔案來源位置的路徑。 如果元件是在本機執行，則此值是安裝之後檔案目標位置的路徑。 如果元件不存在，則路徑是空白的。 如需有關檢查元件安裝狀態的詳細資訊，請參閱 [檢查功能、元件、](checking-the-installation-of-features-components-files.md)檔案的安裝。
    -   如果找到 $componentkey 格式的子字串 \[  \] ，就會由元件的安裝目錄取代，並在 [元件資料表](component-table.md)中將值 *componentkey* 當做索引鍵使用。 Componentkey 的值 \[ $  \] 會保持空白，而且在安裝程式執行[CostInitialize 動作](costinitialize-action.md)、 [FileCost 動作](filecost-action.md)和[CostFinalize 動作](costfinalize-action.md)之前，不會以目錄取代。 Componentkey 的值 \[ $  \] 取決於元件的安裝狀態。 如果元件是從來源執行，則此值為檔案的來原始目錄。 如果元件是在本機執行，則在安裝之後，此值會是目標目錄。 如果元件不存在，此值會保留空白。 如需有關檢查元件安裝狀態的詳細資訊，請參閱 [檢查功能、元件、](checking-the-installation-of-features-components-files.md)檔案的安裝。
    -   如果找到 "c" 格式的子字串，則會 \[ \\ \] 由字元取代，而不需要進一步處理。 只保留反斜線之後的第一個字元;所有其他專案都已移除。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[格式 化](formatted.md)
</dt> <dt>

[資料行資料類型](column-data-types.md)
</dt> </dl>

 

 




