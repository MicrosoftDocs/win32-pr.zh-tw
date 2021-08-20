---
description: 表示 Shell 資料夾。 此物件包含屬性和方法，可讓您取得資料夾的相關資訊。
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: '資料夾物件 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: baf180149419178b489f3ba00042c561268b36e7b7ed7b0e2afab54b68f78466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032616"
---
# <a name="folder-object"></a>Folder 物件

表示 Shell 資料夾。 此物件包含屬性和方法，可讓您取得資料夾的相關資訊。

## <a name="members"></a>成員

**資料夾** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**資料夾** 物件有這些方法。



| 方法                                      | 描述                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**CopyHere**](folder-copyhere.md)         | 將專案或專案複製到資料夾。<br/>                                                                            |
| [**GetDetailsOf**](folder-getdetailsof.md) | 抓取資料夾中專案的詳細資料。 例如，其大小、類型或上次修改的時間。<br/> |
| [**項目**](folder-items.md)               | 抓取 [**FolderItems**](folderitems.md) 物件，該物件表示資料夾中的專案集合。<br/>    |
| [**MoveHere**](folder-movehere.md)         | 將專案或專案移至此資料夾。<br/>                                                                          |
| [**NewFolder**](folder-newfolder.md)       | 建立新的資料夾。<br/>                                                                                           |
| [**ParseName**](folder-parsename.md)       | 建立並傳回 [**FolderItem**](folderitem.md) 物件，該物件表示指定的專案。<br/>                 |



 

### <a name="properties"></a>屬性

**資料夾** 物件具有這些屬性。



| 屬性                                               | 存取類型          | 描述                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [**Application**](folder-application.md)<br/>   | 唯讀<br/> | 包含資料夾的應用程式物件。<br/> |
| [**父代**](folder-parent.md)<br/>             | 唯讀<br/> | 未實作。<br/>                          |
| [**ParentFolder**](folder-parentfolder.md)<br/> | 唯讀<br/> | 包含父 **資料夾** 物件。<br/>    |
| [**標題**](folder-title.md)<br/>               | 唯讀<br/> | 包含資料夾的標題。<br/>         |



 

## <a name="remarks"></a>備註

> [!Note]  
> 並非所有的方法都會針對所有資料夾執行。 例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。 如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                 |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl> |



 

 




