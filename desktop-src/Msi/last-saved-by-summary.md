---
description: 安裝程式會將 [上次儲存的摘要] 屬性設定為值，取決於這是否為安裝套件、轉換或修補套件。在安裝套件中，安裝程式會在系統管理安裝期間，將此屬性設定為 [LogonUser] 屬性的值。 資料庫編輯工具的開發人員可能會在開發程式中使用這個屬性，來追蹤最後一個修改安裝資料庫的人員。 在最後的出貨資料庫中，這個屬性應該設定為 Null。 安裝程式永遠不會使用這個屬性，而且使用者永遠不需要修改它。在轉換中，此摘要屬性包含資料庫在轉換之後應該具有的平臺和語言識別項 (s) 。 屬性會指定要在新資料庫中設定範本摘要的內容。在 patch 封裝中，此摘要屬性包含以分號分隔的轉換 substorage 名稱清單（依此修補程式套用的順序）。
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: 上次儲存的摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999375"
---
# <a name="last-saved-by-summary-property"></a>上次儲存的摘要屬性

安裝程式會將 [ **上次儲存的摘要** ] 屬性設定為值，取決於這是否為安裝套件、轉換或修補套件。

在安裝套件中，安裝程式會在系統 [管理安裝](administrative-installation.md)期間，將此屬性設定為 [ [**LogonUser**](logonuser.md) ] 屬性的值。 資料庫編輯工具的開發人員可能會在開發程式中使用這個屬性，來追蹤最後一個修改安裝資料庫的人員。 在最後的出貨資料庫中，這個屬性應該設定為 Null。 安裝程式永遠不會使用這個屬性，而且使用者永遠不需要修改它。

在轉換中，此摘要屬性包含資料庫在轉換之後應該具有的平臺和語言識別項 (s) 。 屬性會指定要在新資料庫中設定 [**範本摘要**](template-summary.md) 的內容。

在 patch 封裝中，此摘要屬性包含以分號分隔的轉換 substorage 名稱清單（依此修補程式套用的順序）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[摘要屬性描述](summary-property-descriptions.md)
</dt> </dl>

 

 




