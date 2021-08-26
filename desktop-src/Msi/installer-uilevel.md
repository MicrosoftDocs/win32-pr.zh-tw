---
description: 安裝程式物件的 UILevel 屬性是讀寫屬性，它會指出在目前的進程空間內開啟和處理後續封裝時，所要使用的使用者介面型別。
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: UILevel 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3004675ee8e07c3503ec4442832c00975364066fa4a0c770b0b081fc7b64c3c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043568"
---
# <a name="installeruilevel-property"></a>UILevel 屬性

[**安裝程式**](installer-object.md)物件的 **UILevel** 屬性是讀寫屬性，它會指出在目前的進程空間內開啟和處理後續封裝時，所要使用的使用者介面型別。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註



| 使用者介面層級   | 值 | 描述                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msiUILevelNoChange     | 0     | 不會變更 UI 層級。                                                                                                                                                                          |
| msiUILevelDefault      | 1     | 使用預設的 UI 層級。                                                                                                                                                                             |
| msiUILevelNone         | 2     | 無訊息安裝。                                                                                                                                                                               |
| msiUILevelBasic        | 3     | 簡單的進度和錯誤處理。                                                                                                                                                                |
| msiUILevelReduced      | 4     | 已隱藏撰寫的 UI 和 wizard 對話方塊。                                                                                                                                                    |
| msiUILevelFull         | 5     | 使用嚮導、進度和錯誤撰寫的 UI。                                                                                                                                                    |
| msiUILevelHideCancel   | 32    | 如果與 msiUILevelBasic 值結合，安裝程式會顯示進度對話方塊，但不會在對話方塊中顯示 [ **取消** ] 按鈕，以防止使用者取消安裝。 |
| msiUILevelProgressOnly | 64    | 如果與 msiUILevelBasic 值結合，安裝程式會顯示進度對話方塊，但不會顯示任何強制回應對話方塊或錯誤對話方塊。                                        |
| msiUILevelEndDialog    | 128   | 如果與上述任何值結合，安裝程式會在安裝成功或發生錯誤時，顯示模式對話方塊。 如果使用者取消，則不會顯示任何對話方塊。 |



 

另請參閱， [從自訂動作判斷 UI 層級](determining-ui-level-from-a-custom-action.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




