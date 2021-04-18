---
description: PatchProperty 屬性會取得套用至特定產品實例之特定修補程式的相關資訊。 這個屬性會呼叫 MsiGetPatchInfoEx。
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: PatchProperty 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976130"
---
# <a name="patchpatchproperty-method"></a>PatchProperty 方法

**PatchProperty** 屬性會取得套用至特定產品實例之特定修補程式的相關資訊。 這個屬性會呼叫 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)。

## <a name="syntax"></a>語法


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*szProperty* 
</dt> <dd>

*SzProperty* 參數可以是下列其中一個值。



| Name          | 意義                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocalPackage  | 取得產品所使用的快取修補檔案。                                                                                                                                                                                                                                                                               |
| 轉換    | 取得上次修補安裝所套用至產品的一組修補程式轉換。 如果使用者未登入電腦，則每個使用者非受控應用程式可能無法使用此值。                                                                                                                     |
| InstallDate   | 取得修補程式套用至產品的日期。                                                                                                                                                                                                                                                                      |
| 可卸載 | 如果修補程式標示為可以從產品卸載，則會傳回 "1"。 在此情況下，如果另一個無法卸載的修補程式需要此修補程式，則安裝程式仍然可以封鎖卸載。                                                                                                          |
| 狀態         | 如果此修補程式目前套用至產品，則會傳回 "1"。 如果已由另一個修補程式取代此修補程式，則會傳回 "2"。 如果此修補程式已由另一個修補程式淘汰，則會傳回 "4"。 這些值會對應至 [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)的 *dwFilter* 參數所使用的常數。 |
| DisplayName   | 取得修補程式的註冊顯示名稱。 針對未在 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表中包含 DisplayName 屬性的修補程式，傳回的顯示名稱為空字串 ( "" ) 。                                                                                                      |
| MoreInfoURL   | 取得修補程式的已註冊支援資訊 URL。 針對未在 [MsiPatchMetadata](msipatchmetadata-table.md) 資料表中包含 MoreInfoURL 屬性的修補程式，傳回的支援資訊 URL 是 ( "" ) 的空字串。                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

\_ \_ 如果 [**修補程式**](patch-object.md)物件是以空字串來初始化， 則這個方法可能會傳回錯誤未知的修補程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




