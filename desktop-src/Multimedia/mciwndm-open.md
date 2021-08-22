---
title: 'MCIWNDM_OPEN 訊息 (Vfw .h) '
description: MCIWNDM \_ 開啟的訊息會開啟 MCI 裝置，並將其與 MCIWnd 視窗建立關聯。
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bebf9573303e3560b385425e7642106120c41456a21c1c4b80bc158328a864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428898"
---
# <a name="mciwndm_open-message"></a>MCIWNDM \_ 開啟的訊息

**MCIWNDM \_ 開啟** 的訊息會開啟 MCI 裝置，並將其與 MCIWnd 視窗建立關聯。 若為使用資料檔案的 MCI 裝置，此宏也可以開啟指定的資料檔案、為要建立的新檔案命名，或顯示對話方塊，讓使用者選取要開啟的檔案。 您可以使用 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) 宏明確地傳送此訊息。


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

與要開啟的裝置或檔案相關聯的旗標。 MCIWNDOPENF \_ new 旗標會指定以 **szFile** 中指定的名稱建立新的檔案。

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*
</dt> <dd>

以 null 結束的字串指標，識別要開啟的檔案名或 MCI 裝置名稱。 針對此參數指定1，以顯示 [開啟] 對話方塊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





