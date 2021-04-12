---
title: 'WM_GESTURE 訊息 (Winuser .h) '
description: 傳遞筆勢的相關資訊。
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- WM_GESTURE 訊息 Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384938"
---
# <a name="wm_gesture-message"></a>WM \_ 手勢訊息

傳遞筆勢的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

提供識別手勢命令和筆勢特定引數值的資訊。 這項資訊與在 [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)結構的 **ullArguments** 成員中傳遞的資訊相同。

</dd> <dt>

*lParam* 
</dt> <dd>

提供識別手勢命令和筆勢特定引數值之資訊的控制碼。 這項資訊是透過呼叫 [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)來取出。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回0。

如果應用程式未處理訊息，則必須呼叫 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)。 未這樣做會導致應用程式流失記憶體，因為觸控輸入控點將不會關閉，且不會釋放相關聯的進程記憶體。

## <a name="remarks"></a>備註

下表列出支援的手勢命令。



| 手勢識別碼            | 值 (*dwID*)  | Description                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GID \_ 開始**        | 1              | 表示正在開始泛型手勢。                                                                                                                                                                                                                                            |
| **GID \_ 結束**          | 2              | 指出泛型手勢結束。                                                                                                                                                                                                                                                     |
| **GID \_ 縮放**         | 3              | 表示縮放開始、縮放移動或縮放停用。 第一個 **GID \_ zoom** 命令訊息會開始縮放，但不會造成任何縮放。 第二個 **gid \_ zoom** 命令會觸發相對於第一個 **gid \_ 縮放** 中所含狀態的縮放比例。                                    |
| **GID \_ 平移**          | 4              | 表示移動流覽或平移開始。 第一個 **GID \_ pan** 命令表示平移開始，但不會執行任何移動。 使用第二個 **GID \_ PAN** 命令訊息，應用程式將會開始移動。                                                                            |
| **GID \_ 旋轉**       | 5              | 表示旋轉移動或旋轉開始。 第一個 **GID \_ 旋轉** 命令訊息表示旋轉移動或旋轉開始，但不會旋轉。 第二個 **gid \_ 輪替** 命令訊息將會觸發相對於第一個 **GID \_ 旋轉** 所含狀態的旋轉作業。 |
| **GID \_ TWOFINGERTAP** | 6              | 表示雙向點一下手勢。                                                                                                                                                                                                                                                    |
| **GID \_ PRESSANDTAP**  | 7              | 表示按下和點擊手勢。                                                                                                                                                                                                                                                 |



 

> [!Note]  
> 為了啟用舊版支援，必須使用 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)轉送具有 **GID \_ BEGIN** 和 **gid \_ END** 手勢命令的訊息。

 

下表指出在 *lParam* 和 *wParam* 參數中傳遞的手勢引數。



| 手勢識別碼            | 手勢        | *ullArgument*                                                                                                                                                                                                                                                                                                                                                                                            | [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)結構中的 *ptsLocation*                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **GID \_ 縮放**         | 放大/縮小    | 表示兩個點之間的距離。                                                                                                                                                                                                                                                                                                                                                           | 指出縮放的中心。                                                                                 |
| **GID \_ 平移**          | 移動瀏覽            | 表示兩個點之間的距離。                                                                                                                                                                                                                                                                                                                                                           | 表示平移的目前位置。                                                                        |
| **GID \_ 旋轉**       | 旋轉 (pivot)  | 如果已設定 **GF \_ 開始** 旗標，則表示旋轉的角度。 否則，這是自旋轉開始之後的角度變化。 這會經過簽署，以指出旋轉的方向。 使用 [**gid \_ \_ \_ 從 \_ 引數旋轉角度**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) 和 [**gid \_ 將 \_ 角度旋轉 \_ 為 \_ 引數**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) 宏，以取得和設定角度值。 | 這表示旋轉的中心，也就是目標物件周圍旋轉的靜止點。 |
| **GID \_ TWOFINGERTAP** | 雙手指點 | 表示兩個手指之間的距離。                                                                                                                                                                                                                                                                                                                                                          | 表示雙手指的中心。                                                                          |
| **GID \_ PRESSANDTAP**  | 點一下  | 指出第一個手指和第二個手指之間的差異。 此值會儲存在 **點** 結構中 *ullArgument* 的較低32位。                                                                                                                                                                                                                                             | 指出第一個手指關閉的位置。                                                       |



 

> [!Note]  
> 所有距離和位置都是以實體畫面座標來提供。

 

> [!Note]  
> *DwID* 和 *ullArgument* 參數只應視為隨附于 GID \_ \* 命令，而且應用程式不應加以修改。

 

## <a name="examples"></a>範例

下列程式碼說明如何取得與此訊息相關聯的手勢特定資訊。

> [!Note]  
> 您應該一律將未處理的訊息轉送至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) ，並應針對您在呼叫 [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle)時所處理的訊息關閉手勢輸入控制碼。 在此範例中，將隱藏預設的軌跡處理常式行為，因為每個手勢案例中的 TOUCHINPUT 控制碼已關閉。 如果您移除了上述程式碼中未處理訊息的案例，則預設的軌跡處理常式會在預設案例中轉送至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 來處理訊息。

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[通知](notifications.md)
</dt> <dt>

[Windows Touch 手勢程式設計指南](guide-multi-touch-gestures.md)
</dt> </dl>

 

