---
description: Patch 物件代表已註冊或套用之修補程式的唯一實例。您可以使用 Patch 屬性將物件具現化為 &\# 0034;WindowsInstaller： Patch (PatchCode、ProductCode、UserSid、CoNtext) &\# 0034;。
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Patch 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9e337af735a39312cb5aa740283cb8b4d8b508be33f28c302788a1207f89472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074838"
---
# <a name="patch-object"></a>Patch 物件

**Patch** 物件代表已註冊或套用之修補程式的唯一實例。

您可以使用 Patch 屬性將此物件具 **現** 化為 "WindowsInstaller"， (*PatchCode*、 *ProductCode*、 *UserSid*、 *CoNtext*) "。 若為電腦內容， *UserSid* 參數必須是空字串。 您可以針對只註冊但尚未套用至任何產品的修補程式，將 *ProductCode* 設定為空字串。 只有在讀取或更新修補程式的來源清單資訊時，才能將 *ProductCode* 設定為空字串。

## <a name="members"></a>成員

**Patch** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Patch** 物件有這些方法。



| 方法                                                               | 描述                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)       | 將磁片新增至已註冊的磁片集。<br/>                                                                                   |
| [**SourceListAddSource**](patch-sourcelistaddsource.md)             | 將網路或 URL 來源新增至來源清單。 <br/>                                                                             |
| [**SourceListClearAll**](patch-sourcelistclearall.md)               | 清除指定類型來源的完整來源清單。<br/>                                                            |
| [**SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)   | 從來源清單中移除已註冊磁片集的磁片。 <br/>                                                        |
| [**SourceListClearSource**](patch-sourcelistclearsource.md)         | 從來源清單中移除網路或 URL 來源。<br/>                                                                         |
| [**SourceListForceResolution**](patch-sourcelistforceresolution.md) | 清除來源清單中上次使用的來源。 這會在下一次需要來源時強制來源清單解析。<br/> |



 

### <a name="properties"></a>屬性

**Patch** 物件具有這些屬性。



| 屬性                                                  | 描述                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Context**](patch-context.md)<br/>               | 此修補程式實例的內容是 MSIINSTALLCONTEXT 值。<br/>                                   |
| [**MediaDisks**](patch-mediadisks.md)<br/>         | 列舉此 patch 實例的所有媒體磁片。<br/>                                         |
| [**PatchCode**](patch-patchcode.md)<br/>           | 傳回修補程式碼。<br/>                                                                         |
| [**PatchProperty**](patch-patchproperty.md)<br/>   | 取得套用至特定產品實例之特定 patch 的相關屬性資訊。<br/> |
| [**ProductCode**](patch-productcode.md)<br/>       | 傳回產品代碼。<br/>                                                                       |
| [**SourceListInfo**](patch-sourcelistinfo.md)<br/> | 取得和設定來源資訊屬性。 這是讀取或寫入屬性。<br/>              |
| [**來源**](patch-sources.md)<br/>               | 列舉此 patch 實例的所有來源。<br/>                                             |
| [**狀態**](patch-state.md)<br/>                   | 修補程式的安裝狀態。<br/>                                                                |
| [**UserSid**](patch-usersid.md)<br/>               | 傳回此 patch 實例可用之帳戶下的使用者 SID。<br/>                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003、Windows XP 和 Windows 2000 上的安裝程式3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows安裝程式腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




