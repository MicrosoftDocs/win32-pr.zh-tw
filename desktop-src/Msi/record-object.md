---
description: 記錄物件是用來保存和傳送變數值數目的容器。
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Record 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984327"
---
# <a name="record-object"></a>Record 物件

**記錄** 物件是用來保存和傳送變數值數目的容器。 記錄中的欄位是以數位的索引，而且可以包含字串、整數、物件和 null 值。 超過配置記錄大小的欄位會被視為具有永久 null 值。 欄位編號0是保留的。

## <a name="members"></a>成員

**記錄** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**記錄** 物件有這些方法。



| 方法                                  | 描述                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**ClearData**](record-cleardata.md)   | 清除所有欄位中的資料，並將其設定為 null。<br/>                                      |
| [**FormatText**](record-formattext.md) | 根據欄位0中的範本來格式化欄位。<br/>                                      |
| [**ReadStream**](record-readstream.md) | 從保存資料流程資料的記錄欄位讀取指定的位元組數目。<br/>                |
| [**SetStream**](record-setstream.md)   | 將指定之檔案的內容複寫到指定的記錄欄位中，做為資料流程資料。<br/> |



 

### <a name="properties"></a>屬性

**記錄** 物件具有這些屬性。



| 屬性                                             | 存取類型           | Description                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**DataSize**](record-datasize.md)<br/>       |                       | 傳回指定欄位的資料大小。<br/>                             |
| [**FieldCount**](record-fieldcount.md)<br/>   |                       | 傳回記錄中的欄位數目。<br/>                                        |
| [**IntegerData**](record-integerdata.md)<br/> | 讀取/寫入<br/> | 將32位整數資料傳入或移出記錄內的指定欄位。<br/> |
| [**IsNull**](record-isnull.md)<br/>           |                       | 如果指定的欄位為 null，則傳回 True，如果欄位包含資料，則傳回 False。<br/>  |
| [**至 convertfrom-stringdata**](record-stringdata.md)<br/>   | 讀取/寫入<br/> | 將字串資料傳入或傳出記錄內的指定欄位。<br/>         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateRecord 方法**](installer-createrecord.md)
</dt> <dt>

[Windows Installer 腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




