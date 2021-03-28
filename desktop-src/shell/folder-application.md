---
description: 包含資料夾的應用程式物件。
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: '資料夾。應用程式屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468605"
---
# <a name="folderapplication-property"></a>資料夾。應用程式屬性

包含資料夾的應用程式物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
Application = Folder.Application
```



## <a name="property-value"></a>屬性值

應用程式物件的物件參考。

## <a name="remarks"></a>備註

如果可以存取該物件， **應用程式** 屬性會傳回包含 WebBrowser 控制項之應用程式所支援的 automation 物件。 否則，此屬性會傳回 WebBrowser 控制項的 automation 物件。

使用這個屬性搭配 **Set** 和 **CreateObject** 命令，或使用 **GetObject** 命令來建立和操作 Internet Explorer 應用程式的實例。

> [!Note]  
> 並非所有的方法都會針對所有資料夾執行。 例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。 如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                 |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl> |



 

 




