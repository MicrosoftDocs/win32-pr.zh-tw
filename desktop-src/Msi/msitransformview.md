---
description: 此臨時表可針對由修補程式新增或更新的自訂動作，啟用自訂動作修補程式卸載選項。
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980598"
---
# <a name="msitransformview"></a>MsiTransformView

此臨時表可針對由修補程式新增或更新的自訂動作，啟用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md) 。

如果修補程式新增或更新具有 **msidbCustomActionTypePatchUninstall** 屬性的自訂動作，Windows Installer 會在卸載修補程式時執行新的或更新的自訂動作。 Windows Installer 會將修補程式內的更新提供給修補程式卸載自訂動作。 修補程式必須包含 MsiTransformView *<PatchGUID>* 資料表，以提供此資訊給 Windows Installer。 此表格中的資訊可供任何立即的自訂動作使用，並無法用於延後的自訂動作。

**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。 自 Windows Installer 4.5 開始提供 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md) 。

此資料表應命名為 MsiTransformView *<PatchGUID>* table，其中 *<PatchGUID>* 是可唯一識別修補程式的 GUID。 MsiTransformView *<PatchGUID>* 資料表具有下列資料行。



| Column  | 類型                         | 答案 | Nullable |
|---------|------------------------------|-----|----------|
| 資料表   | [識別碼](identifier.md) | Y   | N        |
| Column  | [Text](text.md)             | Y   | N        |
| 資料列     | [Text](text.md)             | Y   | Y        |
| 資料    | [Text](text.md)             | N   | Y        |
| 目前 | [Text](text.md)             | N   | Y        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>表
</dt> <dd>

改變的資料庫資料表名稱。

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>列
</dt> <dd>

改變的資料表資料行名稱，或插入、刪除、建立或卸載。

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>行
</dt> <dd>

以定位字元分隔的主鍵值清單。 Null 主鍵值是以單一空白字元表示。 此資料行中的 Null 值表示架構變更。

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>資料
</dt> <dd>

資料、資料流程的名稱或資料行定義。

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>當前
</dt> <dd>

參考資料庫的目前值，或資料行 a 數位。

</dd> </dl>

## <a name="remarks"></a>備註

修補程式卸載時，修補卸載自訂動作執行。 卸載產品時，不會執行這些功能。 使用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md) ，此資料表可在卸載修補程式時執行自訂。

修補程式可以更新原始封裝 ( .msi 檔案中提供的自訂動作。 ) 在卸載修補程式時執行自訂動作的更新版本，請在原始封裝中將 **msidbCustomActionTypePatchUninstall** 屬性標示為自訂動作。

 

 



