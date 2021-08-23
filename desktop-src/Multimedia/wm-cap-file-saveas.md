---
title: 'WM_CAP_FILE_SAVEAS 訊息 (Vfw .h) '
description: WM \_ CAP 檔案 \_ 的 \_ SAVEAS 訊息會將 capture 檔案的內容複寫到另一個檔案。 您可以使用 capFileSaveAs 宏明確地傳送此訊息。
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a200b8e73d81072961ec4e6aa7c8e1dd989bf2d8c3e0480c75908a8761ee93b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687008"
---
# <a name="wm_cap_file_saveas-message"></a>WM \_ CAP \_ FILE \_ SAVEAS 訊息

**WM CAP 檔案的 \_ \_ \_ SAVEAS** 訊息會將 capture 檔案的內容複寫到另一個檔案。 您可以使用 [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) 宏明確地傳送此訊息。


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*
</dt> <dd>

以 null 結束的字串指標，其中包含用來複製檔案的目的地檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

如果發生錯誤，且使用 [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md) 訊息設定錯誤回呼函式，則會呼叫錯誤回呼函式。

## <a name="remarks"></a>備註

此訊息不會變更目前 capture 檔案的名稱或內容。

如果複製作業因為磁片已滿錯誤而失敗，則會自動刪除目的地檔案。

通常會針對預期的最大 capture 區段預先配置 capture 檔案，而且只會使用其中一部分來捕捉資料。 此訊息只會複製包含 capture 資料之檔案的部分。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> <dt>

[影片捕獲訊息](video-capture-messages.md)
</dt> </dl>

 

 





