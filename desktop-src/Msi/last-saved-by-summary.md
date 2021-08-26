---
description: 安裝程式會將 [上次儲存的摘要] 屬性設定為值，取決於這是否為安裝套件、轉換或修補套件。在安裝套件中，安裝程式會在系統管理安裝期間，將此屬性設定為 [LogonUser] 屬性的值。 資料庫編輯工具的開發人員可能會在開發程式中使用這個屬性，來追蹤最後一個修改安裝資料庫的人員。 在最後的出貨資料庫中，這個屬性應該設定為 Null。 安裝程式永遠不會使用這個屬性，而且使用者永遠不需要修改它。在轉換中，此摘要屬性包含資料庫在轉換之後應該具有的平臺和語言識別項 (s) 。 屬性會指定要在新資料庫中設定範本摘要的內容。在 patch 封裝中，此摘要屬性包含以分號分隔的轉換 substorage 名稱清單（依此修補程式套用的順序）。
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: 上次儲存的摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9299dc6a00af4e48eb3901842aba58a3c8d9a9c1d98d3a3e1e0f05bfccc4333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979448"
---
# <a name="last-saved-by-summary-property"></a>上次儲存的摘要屬性

安裝程式會將 [ **上次儲存的摘要** ] 屬性設定為值，取決於這是否為安裝套件、轉換或修補套件。

在安裝套件中，安裝程式會在系統 [管理安裝](administrative-installation.md)期間，將此屬性設定為 [ [**LogonUser**](logonuser.md) ] 屬性的值。 資料庫編輯工具的開發人員可能會在開發程式中使用這個屬性，來追蹤最後一個修改安裝資料庫的人員。 在最後的出貨資料庫中，這個屬性應該設定為 Null。 安裝程式永遠不會使用這個屬性，而且使用者永遠不需要修改它。

在轉換中，此摘要屬性包含資料庫在轉換之後應該具有的平臺和語言識別項 (s) 。 屬性會指定要在新資料庫中設定 [**範本摘要**](template-summary.md) 的內容。

在 patch 封裝中，此摘要屬性包含以分號分隔的轉換 substorage 名稱清單（依此修補程式套用的順序）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[摘要屬性描述](summary-property-descriptions.md)
</dt> </dl>

 

 




