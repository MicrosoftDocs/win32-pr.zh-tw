---
description: 管理 Shell 連結。 這個物件讓 IShellLink 介面的許多功能可供腳本應用程式使用。
title: 'ShellLinkObject 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973737"
---
# <a name="shelllinkobject-object"></a>ShellLinkObject 物件

管理 Shell 連結。 這個物件讓 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 介面的許多功能可供腳本應用程式使用。

## <a name="members"></a>成員

**ShellLinkObject** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ShellLinkObject** 物件有這些方法。



| 方法                                                     | 描述                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetIconLocation**](shelllinkobject-geticonlocation.md) | 取得指派給連結的圖示位置。<br/>                                 |
| [**解決**](shelllinkobject-resolve.md)                 | 尋找 Shell 連結的目標，即使目標已移動或重新命名也一樣。<br/> |
| [**儲存**](shelllinkobject-save.md)                       | 儲存連結的所有變更。<br/>                                                      |
| [**SetIconLocation**](shelllinkobject-seticonlocation.md) | 設定指派給連結的圖示位置。<br/>                                 |



 

### <a name="properties"></a>屬性

**ShellLinkObject** 物件具有這些屬性。



| 屬性                                                                | 存取類型           | Description                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**引數**](shelllinkobject-arguments.md)<br/>               | 讀取/寫入<br/> | 包含連結的引數。<br/>                                                                   |
| [**描述**](shelllinkobject-description.md)<br/>           | 讀取/寫入<br/> | 取得或設定連結的描述。<br/>                                                      |
| [**熱鍵**](shelllinkobject-hotkey.md)<br/>                     | 讀取/寫入<br/> | 取得或設定連結的鍵盤快速鍵。<br/>                                               |
| [**路徑**](shelllinkobject-path.md)<br/>                         | 讀取/寫入<br/> | 取得或設定連結化物件的路徑。<br/>                                                      |
| [**ShowCommand**](shelllinkobject-showcommand.md)<br/>           | 讀取/寫入<br/> | 取得或設定連結命令的初始顯示狀態 (大小、最小化或最大化) 。<br/> |
| [**WorkingDirectory**](shelllinkobject-workingdirectory.md)<br/> | 讀取/寫入<br/> | 取得或設定連結中指定的工作目錄。<br/>                                      |



 

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

[Shell 連結](./links.md)
</dt> </dl>

 

 
