---
description: 表示 Shell 資料夾中的專案。 此物件包含屬性和方法，可讓您取得專案的相關資訊。
title: 'FolderItem 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a1c66c594a60682ad359ffbcdcd0bf045601051d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468600"
---
# <a name="folderitem-object"></a>FolderItem 物件

表示 Shell 資料夾中的專案。 此物件包含屬性和方法，可讓您取得專案的相關資訊。

## <a name="members"></a>成員

**FolderItem** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**FolderItem** 物件有這些方法。



| 方法                                      | 描述                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InvokeVerb**](folderitem-invokeverb.md) | 在專案上執行動詞。<br/>                                                                                                                     |
| [**動詞**](folderitem-verbs.md)           | 抓取專案的 [**FolderItemVerbs**](folderitemverbs.md) 物件。 此物件是可以在專案上執行的動詞集合。<br/> |



 

### <a name="properties"></a>屬性

**FolderItem** 物件具有這些屬性。



| 屬性                                                   | 存取類型           | Description                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitem-application.md)<br/>   | 唯讀<br/>  | 包含資料夾專案的 [**應用程式**](folderitem-application.md) 物件。<br/>                                                                                                                   |
| [**GetFolder**](folderitem-getfolder.md)<br/>       | 唯讀<br/>  | 如果專案是資料夾，則包含專案的 [**資料夾**](folder.md) 物件。<br/>                                                                                                                           |
| [**GetLink**](folderitem-getlink.md)<br/>           | 唯讀<br/>  | 如果專案是快捷方式，則包含專案的 [**ShellLinkObject**](shelllinkobject-object.md) 物件。<br/>                                                                                                |
| [**IsBrowsable**](folderitem-isbrowsable.md)<br/>   | 唯讀<br/>  | 指出專案是否可裝載于瀏覽器或 Windows 檔案總管框架內。<br/>                                                                                                                         |
| [**IsFileSystem**](folderitem-isfilesystem.md)<br/> | 唯讀<br/>  | 指出專案是否為檔案系統的一部分。<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | 唯讀<br/>  | 指出專案是否為資料夾。<br/>                                                                                                                                                                      |
| [**IsLink**](folderitem-islink.md)<br/>             | 唯讀<br/>  | 指出專案是否為快捷方式。<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | 讀取/寫入<br/> | 設定或取得上次修改檔案的日期和時間。 [**ModifyDate**](folderitem-modifydate.md) 可以用來取得上次修改資料夾的日期和時間，但無法加以設定。<br/> |
| [**Name**](folderitem-name.md)<br/>                 | 讀取/寫入<br/> | 設定或取得專案的名稱。<br/>                                                                                                                                                                           |
| [**父代**](folderitem-parent.md)<br/>             | 唯讀<br/>  | 取得物件，該物件表示專案的父系。<br/>                                                                                                                                                  |
| [**路徑**](folderitem-path.md)<br/>                 | 唯讀<br/>  | 包含專案的完整路徑和名稱。<br/>                                                                                                                                                                 |
| [**大小**](folderitem-size.md)<br/>                 | 唯讀<br/>  | 包含專案的大小。<br/>                                                                                                                                                                               |
| [**類型**](folderitem-type.md)<br/>                 | 唯讀<br/>  | 包含專案類型的字串表示。<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 




