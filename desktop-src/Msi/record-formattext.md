---
description: 記錄物件的 FormatText 方法會根據欄位0中的範本來格式化欄位。
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: FormatText 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999644"
---
# <a name="recordformattext-method"></a>FormatText 方法

[**記錄**](record-object.md)物件的 **FormatText** 方法會根據欄位0中的範本來格式化欄位。

## <a name="syntax"></a>語法


```JScript
Record.FormatText()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果 **MsiFormatRecord** 傳遞了 null 安裝程式控制碼做為第一個參數，則 **FormatText** 方法會遵循 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)函式的功能。 如此一來，就只會處理記錄欄位參數，而且無法使用屬性來進行替代。

例如，"format this field： \[ 1 \] ，format this property： \[ property" 的字串 \] 會解析為 "format this field： value from field 1，format this property： \[ property \] 。"

要[格式化](formatted.md)的參數會以方括弧括 \[ 住 ... \] 可以反復執行方括弧，因為會從內部輸出中解析替代。

如果字串的一部分是以大括弧 {} 括住，且未包含方括弧，則會保持不變，包括大括弧。

請注意，在 [延後執行自訂動作](deferred-execution-custom-actions.md)的情況下， **FormatText** 只支援一組有限的屬性： CustomActionData 和 ProductCode 屬性。 如需詳細資訊，請參閱 [取得順延強制自訂動作的內容資訊](obtaining-context-information-for-deferred-execution-custom-actions.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[格式 化](formatted.md)
</dt> <dt>

[資料行資料類型](column-data-types.md)
</dt> </dl>

 

 




