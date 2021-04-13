---
title: 視窗命令
description: Window 命令會控制顯示視窗。
ms.assetid: 613dfedb-5ca8-45da-a4ba-ce465b933451
keywords:
- 視窗命令 Windows 多媒體
topic_type:
- apiref
api_name:
- window
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21dde3304fa1445b0eaac68950cdfb91f48e5986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465217"
---
# <a name="window-command"></a>視窗命令

Window 命令會控制顯示視窗。 您可以使用這個命令來變更視窗的顯示特性，或是提供驅動程式用來取代預設顯示視窗的目的地視窗。 數位影片和影片重迭裝置會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("window %s %s %s"), 
  lpszDeviceID, 
  lpszWindowFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszWindowFlags"></span><span id="lpszwindowflags"></span><span id="LPSZWINDOWFLAGS"></span>*lpszWindowFlags*
</dt> <dd>

用來控制顯示視窗的旗標。 下表列出可辨識視窗命令的裝置類型，以及每種類型所使用的旗標。



| 值        | 意義                                                                                                                                        | 意義                                                                                                                                   |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | 處理 *hwnd* 狀態 hidestate minimizestate restorestate showshow 最大化                                                                    | 顯示 minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normaltext *caption*                                             |
| overlay      | fixedhandle defaulthandle *hwnd* state hidestate iconicstate maximizedstate minimizestate minimizedstate no actionstate noactivatestate normal | 狀態 restorestate showshow maximizedshow minimizedshow [**min**](min.md) noactiveshow nashow noactivateshow normalstretchtext *caption* |



 

下表列出可在 **lpszWindowFlags** 參數中指定的旗標，以及它們的意義。



| 值                            | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fixed                            | 停用影像的延展。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 控制碼預設值                   | 指定裝置應該將顯示視窗設回 [開啟](open.md) 操作期間建立的預設視窗。 針對影片重迭裝置，指定裝置應該建立並管理它自己的目的地視窗。                                                                                                                                                                                                                                                                                                                                                  |
| 處理 *hwnd*                    | 指定要使用的目的地視窗的控制碼，而非預設視窗。 *Hwnd* 參數包含與 [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa)函數所傳回的視窗控制碼相等的 ASCII 數值。 有兩個裝置實例可以使用相同的視窗控制碼，前提是每個實例都會更新視窗中的影片和影像圖元，如同其他實例不存在一樣。 當使用 [setvideo](setvideo.md) "off" 停用影片輸出時， [update](update.md) 命令會讓目的地矩形成為純色。 |
| 顯示最大化                   | 將目的地視窗最大化。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 顯示 [**最小**](min.md) noactive | 將目的地視窗顯示為圖示。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 顯示最小化                   | 將目的地視窗最小化。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 顯示 na                          | 顯示目前狀態的目的地視窗;目前作用中的視窗會保持作用中狀態。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 顯示 noactivate                  | 以最新的大小和位置顯示目的地視窗;目前作用中的視窗會保持作用中狀態。                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 顯示正常                      | 以原始大小和位置啟用並顯示目的地視窗。  (這與「狀態還原」旗標相同。 )                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 狀態隱藏                       | 隱藏目的地視窗。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 狀態 iconic                     | 將目的地視窗顯示為圖示。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 狀態最大化                  | 將目的地視窗最大化。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 狀態最小化                   | 將目的地視窗最小化，並在視窗管理員的清單中啟用最上層視窗。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 最小化狀態                  | 將目的地視窗最小化。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 無動作狀態                  | 顯示目前狀態的目的地視窗。 目前作用中的視窗會保持作用中狀態。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 狀態 noactivate                 | 以最新的大小和狀態顯示目的地視窗。 使用中視窗還是維持作用中的狀態。                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 狀態正常                     | 以原始大小和位置啟用並顯示目的地視窗。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 狀態還原                    | 以原始大小和位置啟用並顯示目的地視窗。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 狀態顯示                       | 顯示目的地視窗。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Stretch - 自動縮放                          | 啟用延展影像。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 文字 *標題*                   | 指定目的地視窗的標題。 如果此文字包含內嵌空白，則整個標題必須以引號括住。 預設視窗的預設標題為空白。                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 若為數位視訊裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

影片重迭裝置通常會在開啟時建立並顯示視窗。 如果您的應用程式提供視窗給驅動程式，則您的應用程式會負責管理傳送至視窗的訊息。

由於您可以使用 [ [狀態](status.md) ] 命令抓取驅動程式顯示視窗的控制碼，因此您也可以使用標準的視窗管理員函式 (例如 [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow)) 來操作視窗。

## <a name="examples"></a>範例

下列命令會顯示並設定「電影」播放視窗的標題。

``` syntax
window movie text "Welcome to the Movies" state show
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> <dt>

[open](open.md)
</dt> <dt>

[玩](play.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[update](update.md)
</dt> </dl>

 

