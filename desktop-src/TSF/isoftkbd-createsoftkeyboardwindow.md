---
title: 'ISoftKbd CreateSoftKeyboardWindow 方法 (Softkbdc .h) '
description: ISoftKbd CreateSoftKeyboardWindow 方法會建立一個軟鍵盤視窗。
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- CreateSoftKeyboardWindow 方法文字服務架構
- CreateSoftKeyboardWindow 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，CreateSoftKeyboardWindow 方法
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508995"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a>ISoftKbd：： CreateSoftKeyboardWindow 方法

**ISoftKbd：： CreateSoftKeyboardWindow** 方法會建立一個軟鍵盤視窗。

## <a name="syntax"></a>語法


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hOwner* \[在\]
</dt> <dd>

要包含軟鍵盤的視窗控制碼。

</dd> <dt>

*標題列 \_ 類型* \[\]
</dt> <dd>

[螢幕小鍵盤] 視窗的標題列類型。 可能的類型是由 [**標題列 \_ 類型**](titlebar-type.md) 列舉所定義。

</dd> <dt>

*xPos* \[在\]
</dt> <dd>

軟鍵盤視窗左上角的 x 位置。

</dd> <dt>

*yPos* \[在\]
</dt> <dd>

軟鍵盤視窗左上角的 y 位置。

</dd> <dt>

*寬度* \[在\]
</dt> <dd>

軟鍵盤視窗的寬度。

</dd> <dt>

*高度* \[在\]
</dt> <dd>

軟鍵盤視窗的高度。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 一或多個參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[**ISoftKbd：:D estroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[**標題列 \_ 類型**](titlebar-type.md)
</dt> </dl>

 

 





