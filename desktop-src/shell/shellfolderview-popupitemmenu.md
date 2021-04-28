---
description: ShellFolderView. PopupItemMenu 方法-為指定的專案建立快捷方式功能表，並傳回選取的命令字串。
title: 'ShellFolderView. PopupItemMenu 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083386"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>ShellFolderView. PopupItemMenu 方法

為指定的專案建立快捷方式功能表，並傳回選取的命令字串。

## <a name="syntax"></a>語法


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vItem* \[在\]
</dt> <dd>

類型： **Variant**

將建立快捷方式功能表的 [**FolderItem**](folderitem.md) 物件。

</dd> <dt>

*vx* \[ in、optional\]
</dt> <dd>

類型： **Variant**

功能表的水準位置（以螢幕座標為單位）。

</dd> <dt>

*vy* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

功能表的垂直位置（以螢幕座標為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

接收命令字串的 **字串** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
