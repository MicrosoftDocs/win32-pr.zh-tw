---
title: 'WM_APPCOMMAND 訊息 (Winuser .h) '
description: 通知視窗使用者所產生的應用程式命令事件，例如，按一下 [應用程式命令] 按鈕，或在鍵盤上輸入應用程式命令鍵。
ms.assetid: ffcdfc44-dbfa-42d4-8749-b33bf0e4de0c
keywords:
- WM_APPCOMMAND 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_APPCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 667b2974015edd8b8d3ac0505f4eb4d6c64d1da5b82737ec7d9bb89cc3e8776e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248002"
---
# <a name="wm_appcommand-message"></a>WM \_ APPCOMMAND 訊息

通知視窗使用者所產生的應用程式命令事件，例如，按一下 [應用程式命令] 按鈕，或在鍵盤上輸入應用程式命令鍵。


```C++
#define WM_APPCOMMAND                   0x0319
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

使用者按一下按鈕或按下按鍵的視窗控制碼。 這可以是接收訊息之視窗的子視窗。 如需有關處理此訊息的詳細資訊，請參閱「備註」一節。

</dd> <dt>

*lParam* 
</dt> <dd>

使用下列程式碼來取得包含在 *lParam* 參數中的資訊。


```
cmd  = GET_APPCOMMAND_LPARAM(lParam);

uDevice = GET_DEVICE_LPARAM(lParam);

dwKeys = GET_KEYSTATE_LPARAM(lParam);
```



應用程式命令是 *cmd*，它可以是下列值之一。



| 值                                                                                                                                                                                                                                                                                                                  | 意義                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPCOMMAND_BASS_BOOST"></span><span id="appcommand_bass_boost"></span><dl> <dt>**APPCOMMAND \_低音 \_ 增強**</dt> <dt>20</dt> </dl>                                                                         | 開啟和關閉低音增強功能。<br/>                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BASS_DOWN"></span><span id="appcommand_bass_down"></span><dl> <dt>**APPCOMMAND \_低音 \_**</dt> <dt>19</dt> </dl>                                                                            | 降低低音。<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BASS_UP"></span><span id="appcommand_bass_up"></span><dl> <dt>**APPCOMMAND \_低音 \_ UP**</dt> <dt>21</dt> </dl>                                                                                  | 提高低音。<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_BACKWARD"></span><span id="appcommand_browser_backward"></span><dl> <dt>**APPCOMMAND \_\_向後瀏覽器**</dt> <dt>1</dt> </dl>                                                        | 向後導覽。<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_BROWSER_FAVORITES"></span><span id="appcommand_browser_favorites"></span><dl> <dt>**APPCOMMAND \_流覽 \_ 器**</dt>我的最愛 <dt>6</dt> </dl>                                                     | 開啟我的最愛。<br/>                                                                                                                                                                                                                                                                 |
| <span id="APPCOMMAND_BROWSER_FORWARD"></span><span id="appcommand_browser_forward"></span><dl> <dt>**APPCOMMAND \_瀏覽器 \_ 向前**</dt> <dt>2</dt> </dl>                                                           | 向前導覽。<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_BROWSER_HOME"></span><span id="appcommand_browser_home"></span><dl> <dt>**APPCOMMAND \_瀏覽器 \_ 首頁**</dt> <dt>7</dt> </dl>                                                                    | 流覽首頁。<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_BROWSER_REFRESH"></span><span id="appcommand_browser_refresh"></span><dl> <dt>**APPCOMMAND \_流覽 \_ 器**</dt>重新整理 <dt>3</dt> </dl>                                                           | 重新整理頁面。<br/>                                                                                                                                                                                                                                                                   |
| <span id="APPCOMMAND_BROWSER_SEARCH"></span><span id="appcommand_browser_search"></span><dl> <dt>**APPCOMMAND \_瀏覽器 \_ 搜尋**</dt> <dt>5</dt> </dl>                                                              | 開啟 [搜尋]。<br/>                                                                                                                                                                                                                                                                    |
| <span id="APPCOMMAND_BROWSER_STOP"></span><span id="appcommand_browser_stop"></span><dl> <dt>**APPCOMMAND \_瀏覽器 \_ 停止**</dt> <dt>4</dt> </dl>                                                                    | 停止下載。<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_CLOSE"></span><span id="appcommand_close"></span><dl> <dt>**APPCOMMAND \_收盤**</dt> <dt>31</dt> </dl>                                                                                         | 關閉視窗 (而不是應用程式) 。<br/>                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_COPY"></span><span id="appcommand_copy"></span><dl> <dt>**APPCOMMAND \_複製**</dt> <dt>36</dt> </dl>                                                                                            | 複製選取專案。<br/>                                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_CORRECTION_LIST"></span><span id="appcommand_correction_list"></span><dl> <dt>**APPCOMMAND \_更正 \_ 清單**</dt> <dt>45</dt> </dl>                                                          | 當語音輸入期間未正確識別單字時，會顯示更正清單。 <br/>                                                                                                                                                                                       |
| <span id="APPCOMMAND_CUT"></span><span id="appcommand_cut"></span><dl> <dt>**APPCOMMAND \_剪**</dt>下 <dt>37</dt> </dl>                                                                                               | 剪下選取專案。<br/>                                                                                                                                                                                                                                                              |
| <span id="APPCOMMAND_DICTATE_OR_COMMAND_CONTROL_TOGGLE"></span><span id="appcommand_dictate_or_command_control_toggle"></span><dl> <dt>**APPCOMMAND \_聽寫 \_ 或 \_ 命令 \_ 控制項 \_ 切換**</dt> <dt>43</dt> </dl> | 在兩種語音輸入模式之間切換：聽寫和命令/控制 (提供命令給應用程式或存取功能表) 。 <br/>                                                                                                                                               |
| <span id="APPCOMMAND_FIND"></span><span id="appcommand_find"></span><dl> <dt>**APPCOMMAND \_尋找**</dt> <dt>28</dt> </dl>                                                                                            | 開啟 [ **尋找** ] 對話方塊。<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_FORWARD_MAIL"></span><span id="appcommand_forward_mail"></span><dl> <dt>**APPCOMMAND \_轉寄 \_ 郵件**</dt> <dt>40</dt> </dl>                                                                   | 轉寄郵件訊息。<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_HELP"></span><span id="appcommand_help"></span><dl> <dt>**APPCOMMAND \_**</dt>說明 <dt>27</dt> </dl>                                                                                            | 開啟 [ **說明** ] 對話方塊。<br/>                                                                                                                                                                                                                                                       |
| <span id="APPCOMMAND_LAUNCH_APP1"></span><span id="appcommand_launch_app1"></span><dl> <dt>**APPCOMMAND \_啟動 \_ APP1**</dt> <dt>17</dt> </dl>                                                                      | 開始 App1。<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_APP2"></span><span id="appcommand_launch_app2"></span><dl> <dt>**APPCOMMAND \_啟動 \_ APP2**</dt> <dt>18</dt> </dl>                                                                      | 開始 App2。<br/>                                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_LAUNCH_MAIL"></span><span id="appcommand_launch_mail"></span><dl> <dt>**APPCOMMAND \_啟動 \_ 郵件**</dt> <dt>15</dt> </dl>                                                                      | 開啟 [郵件]。<br/>                                                                                                                                                                                                                                                                      |
| <span id="APPCOMMAND_LAUNCH_MEDIA_SELECT"></span><span id="appcommand_launch_media_select"></span><dl> <dt>**APPCOMMAND \_啟動 \_ 媒體 \_ 選取**</dt> <dt>16</dt> </dl>                                             | 移至媒體選取模式。<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_MEDIA_CHANNEL_DOWN"></span><span id="appcommand_media_channel_down"></span><dl> <dt>**APPCOMMAND \_媒體 \_ 頻道已 \_ 關閉**</dt> <dt>52</dt> </dl>                                                | 減少頻道值，例如電視或無線電調諧器。 <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_CHANNEL_UP"></span><span id="appcommand_media_channel_up"></span><dl> <dt>**APPCOMMAND \_媒體 \_ 頻道已 \_ 達**</dt> <dt>51</dt> </dl>                                                      | 將通道值遞增，例如電視或無線電調諧器。 <br/>                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_FAST_FORWARD"></span><span id="appcommand_media_fast_forward"></span><dl> <dt>**APPCOMMAND \_媒體 \_ FAST \_ 轉寄**</dt> <dt>49</dt> </dl>                                                | 提高串流播放的速度。 這可以透過許多方式來執行，例如，使用固定速度或透過一連串逐漸增加的速度來切換。 <br/>                                                                                                               |
| <span id="APPCOMMAND_MEDIA_NEXTTRACK"></span><span id="appcommand_media_nexttrack"></span><dl> <dt>**APPCOMMAND \_MEDIA \_ NEXTTRACK**</dt> <dt>11</dt> </dl>                                                          | 移至下一個曲目。<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_MEDIA_PAUSE"></span><span id="appcommand_media_pause"></span><dl> <dt>**APPCOMMAND \_媒體 \_ 暫停**</dt> <dt>47</dt> </dl>                                                                      | 暫停： 如果已經暫停，則不採取任何進一步的動作。 這是沒有狀態的直接暫停命令。 如果有離散的 [播放] 和 [暫停] 按鈕，應用程式應該對此命令採取動作，以及 **APPCOMMAND \_ MEDIA \_ Play \_ 暫停**。 <br/>                               |
| <span id="APPCOMMAND_MEDIA_PLAY"></span><span id="appcommand_media_play"></span><dl> <dt>**APPCOMMAND \_MEDIA \_ PLAY**</dt> <dt>46</dt> </dl>                                                                         | 在目前的位置開始播放。 如果已經暫停，則會繼續。 這是沒有狀態的直接播放命令。 如果有離散的 [ **播放** ] 和 [ **暫停** ] 按鈕，應用程式應該對此命令採取動作，以及 **APPCOMMAND \_ MEDIA \_ Play \_ 暫停**。<br/> |
| <span id="APPCOMMAND_MEDIA_PLAY_PAUSE"></span><span id="appcommand_media_play_pause"></span><dl> <dt>**APPCOMMAND \_MEDIA \_ PLAY \_ 暫停**</dt> <dt>14</dt> </dl>                                                      | 播放或暫停播放。 如果有離散的 [ **播放** ] 和 [ **暫停** ] 按鈕，應用程式應該對此命令採取動作，以及 **APPCOMMAND \_ media \_ Play** 和 **APPCOMMAND \_ 媒體 \_ 暫停**。<br/>                                                                          |
| <span id="APPCOMMAND_MEDIA_PREVIOUSTRACK"></span><span id="appcommand_media_previoustrack"></span><dl> <dt>**APPCOMMAND \_媒體 \_ PREVIOUSTRACK**</dt> <dt>12</dt> </dl>                                              | 移至上一個曲目。<br/>                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_MEDIA_RECORD"></span><span id="appcommand_media_record"></span><dl> <dt>**APPCOMMAND \_媒體 \_ 記錄**</dt> <dt>48</dt> </dl>                                                                   | 開始錄製目前的資料流程。<br/>                                                                                                                                                                                                                                             |
| <span id="APPCOMMAND_MEDIA_REWIND"></span><span id="appcommand_media_rewind"></span><dl> <dt>**APPCOMMAND \_媒體 \_**</dt>倒轉 <dt>50</dt> </dl>                                                                   | 以較高的速度從資料流程中往上移。 這可以透過許多方式來執行，例如，使用固定速度或透過一連串逐漸增加的速度來切換。 <br/>                                                                                                   |
| <span id="APPCOMMAND_MEDIA_STOP"></span><span id="appcommand_media_stop"></span><dl> <dt>**APPCOMMAND \_媒體 \_ 停止**</dt> <dt>13</dt> </dl>                                                                         | 停止播放。<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_MIC_ON_OFF_TOGGLE"></span><span id="appcommand_mic_on_off_toggle"></span><dl> <dt>**APPCOMMAND \_\_ \_ 關閉 \_ 切換44的 MIC**</dt> <dt></dt> </dl>                                                  | 切換麥克風。<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_DOWN"></span><span id="appcommand_microphone_volume_down"></span><dl> <dt>**APPCOMMAND \_麥克風 \_ 音量 \_ 減少**</dt> <dt>25</dt> </dl>                                    | 減少麥克風音量。<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_MUTE"></span><span id="appcommand_microphone_volume_mute"></span><dl> <dt>**APPCOMMAND \_麥克風 \_ 音量 \_ 靜音**</dt> <dt>24</dt> </dl>                                    | 將麥克風靜音。<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_MICROPHONE_VOLUME_UP"></span><span id="appcommand_microphone_volume_up"></span><dl> <dt>**APPCOMMAND \_麥克風 \_ 音量 \_ 增加**</dt> <dt>26</dt> </dl>                                          | 增加麥克風音量。<br/>                                                                                                                                                                                                                                                     |
| <span id="APPCOMMAND_NEW"></span><span id="appcommand_new"></span><dl> <dt>**APPCOMMAND \_新**</dt> <dt>29</dt> </dl>                                                                                               | 建立新的視窗。<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_OPEN"></span><span id="appcommand_open"></span><dl> <dt>**APPCOMMAND \_開啟**</dt> <dt>30</dt> </dl>                                                                                            | 開啟視窗。<br/>                                                                                                                                                                                                                                                                  |
| <span id="APPCOMMAND_PASTE"></span><span id="appcommand_paste"></span><dl> <dt>**APPCOMMAND \_貼**</dt>上 <dt>38</dt> </dl>                                                                                         | 貼上<br/>                                                                                                                                                                                                                                                                           |
| <span id="APPCOMMAND_PRINT"></span><span id="appcommand_print"></span><dl> <dt>**APPCOMMAND \_列印**</dt> <dt>33</dt> </dl>                                                                                         | 列印目前的檔。<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_REDO"></span><span id="appcommand_redo"></span><dl> <dt>**APPCOMMAND \_重做**</dt> <dt>35</dt> </dl>                                                                                            | 重做上一個動作。<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_REPLY_TO_MAIL"></span><span id="appcommand_reply_to_mail"></span><dl> <dt>**APPCOMMAND \_回復 \_ \_ 郵件**</dt> <dt>39</dt> </dl>                                                               | 回復郵件訊息。<br/>                                                                                                                                                                                                                                                        |
| <span id="APPCOMMAND_SAVE"></span><span id="appcommand_save"></span><dl> <dt>**APPCOMMAND \_儲存**</dt> <dt>32</dt> </dl>                                                                                            | 儲存目前的檔。<br/>                                                                                                                                                                                                                                                          |
| <span id="APPCOMMAND_SEND_MAIL"></span><span id="appcommand_send_mail"></span><dl> <dt>**APPCOMMAND \_傳送 \_ 郵件**</dt> <dt>41</dt> </dl>                                                                            | 傳送電子郵件訊息。<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_SPELL_CHECK"></span><span id="appcommand_spell_check"></span><dl> <dt>**APPCOMMAND \_拼寫 \_ 檢查**</dt> <dt>42</dt> </dl>                                                                      | 起始拼寫檢查。<br/>                                                                                                                                                                                                                                                         |
| <span id="APPCOMMAND_TREBLE_DOWN"></span><span id="appcommand_treble_down"></span><dl> <dt>**APPCOMMAND \_高音 \_ 中斷**</dt> <dt>22</dt> </dl>                                                                      | 減少高音。<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_TREBLE_UP"></span><span id="appcommand_treble_up"></span><dl> <dt>**APPCOMMAND \_高音 \_ UP**</dt> <dt>23</dt> </dl>                                                                            | 提高高音。<br/>                                                                                                                                                                                                                                                            |
| <span id="APPCOMMAND_UNDO"></span><span id="appcommand_undo"></span><dl> <dt>**APPCOMMAND \_復原**</dt> <dt>34</dt> </dl>                                                                                            | 復原上一個動作。<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_DOWN"></span><span id="appcommand_volume_down"></span><dl> <dt>**APPCOMMAND \_音量 \_ 減少**</dt> <dt>9</dt> </dl>                                                                       | 減少音量。<br/>                                                                                                                                                                                                                                                               |
| <span id="APPCOMMAND_VOLUME_MUTE"></span><span id="appcommand_volume_mute"></span><dl> <dt>**APPCOMMAND \_音量 \_ 靜音**</dt> <dt>8</dt> </dl>                                                                       | 將音量靜音。<br/>                                                                                                                                                                                                                                                                |
| <span id="APPCOMMAND_VOLUME_UP"></span><span id="appcommand_volume_up"></span><dl> <dt>**APPCOMMAND \_\_高容量**</dt> <dt>10</dt> </dl>                                                                            | 引發磁片區。<br/>                                                                                                                                                                                                                                                               |



 

*UDevice* 元件表示產生輸入事件的輸入裝置，而且可以是下列其中一個值。



| 值                                                                                                                                                                                                                                 | 意義                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="FAPPCOMMAND_KEY"></span><span id="fappcommand_key"></span><dl> <dt>**FAPPCOMMAND \_金鑰**</dt> <dt>0</dt> </dl>            | 使用者按下按鍵。<br/>                                                                           |
| <span id="FAPPCOMMAND_MOUSE"></span><span id="fappcommand_mouse"></span><dl> <dt>**FAPPCOMMAND \_滑鼠**</dt> <dt>0x8000</dt> </dl> | 使用者按下滑鼠按鍵。<br/>                                                                  |
| <span id="FAPPCOMMAND_OEM"></span><span id="fappcommand_oem"></span><dl> <dt>**FAPPCOMMAND \_OEM**</dt> <dt>0x1000</dt> </dl>       | 無法辨識的硬體來源產生事件。 它可能是滑鼠或鍵盤事件。<br/> |



 

*DwKeys* 元件會指出不同的虛擬機器碼是否已關閉，而且可以是下列其中一個或多個值。



| 值                                                                                                                                                                                                               | 意義                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_控制項**</dt> <dt>0x0008</dt> </dl>    | CTRL 鍵已關閉。<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_LBUTTON**</dt> <dt>0x0001</dt> </dl>    | 左邊的滑鼠按鍵已關閉。<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_MBUTTON**</dt> <dt>0x0010</dt> </dl>    | 中間的滑鼠按鍵已關閉。<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_RBUTTON**</dt> <dt>0x0002</dt> </dl>    | 滑鼠右鍵已關閉。<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_SHIFT**</dt> <dt>0x0004</dt> </dl>          | SHIFT 鍵已關閉。<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_XBUTTON1**</dt> <dt>0x0020</dt> </dl> | 第一個 X 按鈕已關閉。<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_XBUTTON2**</dt> <dt>0x0040</dt> </dl> | 第二個 X 按鈕已關閉。<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回 **TRUE**。 如需處理傳回值的詳細資訊，請參閱「備註」一節。

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)在處理 [**Wm \_ XBUTTONUP**](wm-xbuttonup.md)或 [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)訊息時，或當使用者輸入應用程式命令索引鍵時，會產生 **wm \_ APPCOMMAND** 訊息。

如果子視窗沒有處理這個訊息，而是呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)， **DefWindowProc** 就會將訊息傳送至其父視窗。 如果最上層視窗不會處理此訊息，而是呼叫 **DefWindowProc**， **DefWindowProc** 將會呼叫 Shell 攔截碼與 **HSHELL \_ APPCOMMAND** 的相同。

若要取得游標的座標（如果訊息是由滑鼠按一下所產生），應用程式可以呼叫 [**GetMessagePos**](/windows/desktop/api/winuser/nf-winuser-getmessagepos)。 應用程式可以藉由檢查 *lParam* 是否包含 **FAPPCOMMAND \_ 滑鼠**，來測試訊息是否由滑鼠所產生。

與其他 windows 訊息不同的是，應用程式在處理應用程式時，應該會從這個訊息傳回 **TRUE** 。 這樣做會允許在早于 Windows 2000 的 Windows 系統上模擬此訊息的軟體，以判斷視窗程式是否已處理訊息或呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)來處理訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**取得 \_ APPCOMMAND \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_appcommand_lparam)
</dt> <dt>

[**取得 \_ 裝置 \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_device_lparam)
</dt> <dt>

[**取得 \_ KEYSTATE \_ LPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_lparam)
</dt> <dt>

[**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
</dt> <dt>

[**WM \_ XBUTTONUP**](wm-xbuttonup.md)
</dt> <dt>

[**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
</dt> <dt>

**概念**
</dt> <dt>

[滑鼠輸入](mouse-input.md)
</dt> </dl>

 

