---
description: 擴充資料夾物件以支援離線資料夾。
title: 'Folder2 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: 8db899fc52cc3511d1af82013fc6c4c87544f1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973209"
---
# <a name="folder2-object"></a>Folder2 物件

擴充 [**資料夾**](folder.md) 物件以支援離線資料夾。

## <a name="members"></a>成員

**Folder2** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Folder2** 物件有這些方法。



| 方法                                                                 | 描述                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**DismissedWebViewBarricade**](folder2-dismissedwebviewbarricade.md) | 呼叫以回應使用者所關閉的 web view barricade。<br/> |
| [**同步**](folder2-synchronize.md)                             | 同步處理資料夾中的所有離線檔案。<br/>                             |



 

### <a name="properties"></a>屬性

**Folder2** 物件具有這些屬性。



| 屬性                                                                            | 存取類型          | Description                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**HaveToShowWebViewBarricade**](folder2-havetoshowwebviewbarricade.md)<br/> | 唯讀<br/> | 目前不支援。<br/>                                       |
| [**OfflineStatus**](folder2-offlinestatus.md)<br/>                           | 唯讀<br/> | 包含資料夾的離線狀態。<br/>                     |
| [**自我**](folder2-self.md)<br/>                                             | 唯讀<br/> | 包含資料夾的 [**FolderItem**](folderitem.md) 物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**資料夾**](folder.md)
</dt> </dl>

 

 




