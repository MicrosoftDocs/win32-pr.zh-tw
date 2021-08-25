---
description: 安裝程式物件的 ShortcutTarget 屬性會檢查快捷方式，並傳回其產品、功能名稱和元件（如果有的話）。
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: ShortcutTarget 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b54e334314c0bfd0fb721b175d0a14894d8a509ea02ff36e324903bb1fdbffaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893998"
---
# <a name="installershortcuttarget-property"></a>ShortcutTarget 屬性

[**安裝程式**](installer-object.md)物件的 **ShortcutTarget** 屬性會檢查快捷方式，並傳回其產品、功能名稱和元件（如果有的話）。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>屬性值

檔案的完整路徑和檔案名。

## <a name="remarks"></a>備註

ShortcutTarget 會傳回包含三個欄位的 [**記錄物件**](record-object.md) ：

-   [欄位 1] 是快捷方式的產品代碼 GUID （如果有的話）。 這個欄位可以是 null。
-   欄位2是快捷方式的功能識別碼（如果有的話）。 這個欄位可以是 null。
-   欄位3是元件程式碼的 GUID （如果有的話）。 這個欄位可以是 null。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




