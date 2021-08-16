---
description: 子類別中的所有控制項，以及對話方塊視窗本身的子類別。
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Ctl3dSubclassDlgEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: aeacdf75e20e2d3521405c20b52d29a466c5fe9a063d70e5acb3c0597934ab9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162129"
---
# <a name="ctl3dsubclassdlgex-function"></a>Ctl3dSubclassDlgEx 函式

子類別中的所有控制項，以及對話方塊視窗本身的子類別。

## <a name="syntax"></a>語法


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndDlg* 
</dt> <dd>

對話方塊視窗的控制碼。

</dd> <dt>

*grbit* 
</dt> <dd>

要子類別化的控制項類型。 這個值可以是下列任何一項。



| 值                                                                                                                                                                                                                                     | 意義                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <dt>**CTL3D \_按鈕**</dt> <dt>0x0001</dt> </dl>                 | 子類別按鈕。<br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <dt>**CTL3D \_清單方塊**</dt> <dt>0x0002</dt> </dl>           | 子類別清單方塊。<br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <dt>**CTL3D \_編輯**</dt> <dt>0x0004</dt> </dl>                       | 子類別編輯控制項。<br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <dt>**CTL3D \_COMBOS**</dt> <dt>0x0008</dt> </dl>                    | 子類別下拉式方塊。<br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <dt>**CTL3D \_STATICTEXTS**</dt> <dt>0x0010</dt> </dl>     | 子類別靜態文字控制項。<br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <dt>**CTL3D \_STATICFRAMES**</dt> <dt>0x0020</dt> </dl>  | 子類別靜態框架。<br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <dt>**CTL3D \_所有**</dt> <dt>0xffff</dt> </dl>                             | 將所有控制項子類別化。<br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <dt>**CTL3D \_NODLGWINDOW**</dt> <dt>0x00010000</dt> </dl> | 請勿將交談視窗子類別化。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

此函數在以 c + + 為基礎的應用程式中特別有用。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
