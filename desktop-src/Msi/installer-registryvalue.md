---
description: 安裝程式物件的 RegistryValue 方法會讀取指定之登錄機碼值的相關資訊。
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: 安裝程式. RegistryValue 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989651"
---
# <a name="installerregistryvalue-method"></a>安裝程式. RegistryValue 方法

[**安裝程式**](installer-object.md)物件的 **RegistryValue** 方法會讀取指定之登錄機碼值的相關資訊。 如果指定的索引鍵或值不存在，此方法會傳回9的錯誤：「下標超出範圍」。

## <a name="syntax"></a>語法


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*root* 
</dt> <dd>

在 Windows NT 4.0 中，登錄根目錄為數字根金鑰或電腦名稱稱，表示為字串。 電腦名稱稱一律為字串。 在 Windows 95、Windows 98 或 Windows Me 中，登錄根目錄只是數位的根機碼。 您只能存取遠端電腦上的 HKLM。



| Root                                                                                                                                                                                   | 意義      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <dt>**HKEY \_ 類別 \_ 根目錄**</dt> </dl>             | 0<br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <dt>**HKEY \_ 目前的 \_ 使用者**</dt> </dl>             | 1<br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <dt>**HKEY \_ 本機 \_ 電腦**</dt> </dl>          | 2<br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <dt>**HKEY \_ 使用者**</dt> </dl>                                   | 3<br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <dt>**HKEY \_ 效能 \_ 資料**</dt> </dl> | 4<br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <dt>**HKEY \_ 目前的設定 \_**</dt> </dl>       | 5<br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <dt>**HKEY \_ DYN \_ 資料**</dt> </dl>                         | 6<br/> |



 

</dd> <dt>

*key* 
</dt> <dd>

字串，包含來自根目錄的完整索引鍵路徑。

</dd> <dt>

*value* 
</dt> <dd>

這個選擇性參數會指定要針對指定的索引鍵傳回的關聯值。 值是下表所示的其中一個值。



| 值                                                                                                                                                                                                    | 意義                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <dt>**遺漏或空白**</dt> </dl> | 傳回布林值，指定索引鍵是否存在。<br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**字串**</dt> </dl>                                         | 如果值名稱不存在，則會傳回與所指定值相關聯的資料。<br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <dt>**正整數**</dt> </dl> | 傳回以1為基礎的列舉值名稱，如果不存在，則會是空的。 此選項會使用 [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) 函數。<br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <dt>**負整數**</dt> </dl> | 傳回以1為基礎的列舉子機碼名稱，如果不存在，則為空白。 此選項會使用 [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) 函數。<br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <dt>**零整數**</dt> </dl>                 | 傳回指定之索引鍵的字串類別名稱。<br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <dt>**空字串 ""**</dt> </dl> | 傳回登錄機碼的預設值。<br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 
