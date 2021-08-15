---
title: info 命令
description: Info 命令會從裝置捕獲硬體描述。 所有 MCI 裝置都會辨識此命令。
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- 資訊命令 Windows 多媒體
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f15675923f37a80ce694a400f18113f5178a54a3f75664008644919c6d9fc128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690468"
---
# <a name="info-command"></a>info 命令

Info 命令會從裝置捕獲硬體描述。 所有 MCI 裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*
</dt> <dd>

識別所需資訊類型的旗標。 下表列出可辨識 **info** 命令的裝置類型，以及每種類型所使用的旗標。



| 值        | 意義                                                             | 意義                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| cdaudio      | 資訊 identityinfo upc                                               | product                                             |
| digitalvideo | 音訊 algorithmaudio qualityfileproductstill algorithmstill 品質 | usageversionvideo algorithmvideo qualitywindow text |
| overlay      | fileproduct                                                         | 視窗文字                                         |
| 排序器    | copyrightfile                                                       | nameproduct                                         |
| 錄影機          | product                                                             | version                                             |
| videodisk    | product                                                             |                                                     |
| waveaudio    | fileinput                                                           | outputproduct                                       |



 

下表列出可在 **lpszInfoType** 參數中指定的旗標，以及它們的意義。



| 值           | 意義                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 音訊演算法 | 傳回目前音訊壓縮演算法的名稱。                                                                                                                                       |
| 音訊品質   | 傳回目前音訊品質描述項的名稱。 如果應用程式將參數設定為未對應至已定義品質的特定值，這可能會傳回「未知」。       |
| 著作權       | 從著作權中繼事件中抓取 MIDI 檔案的著作權注意事項。                                                                                                                            |
| file            | 抓取複合裝置所使用的檔案名。 如果在沒有檔案的情況下開啟裝置，而且未使用 [load](load.md) 命令，則會傳回 null 字串。                  |
| 資訊身分識別   | 針對目前已在正在進行查詢的播放程式中載入的音訊 CD 產生唯一識別碼。                                                                                                        |
| 資訊 upc        | 產生在音訊 CD 上編碼 (UPC) 的通用產品程式碼。 UPC 是數位的字串。 它可能不適用於所有 Cd。                                                    |
| input           | 抓取目前輸入裝置的描述。 如果未設定輸入裝置，則會傳回「無」。                                                                                               |
| NAME            | 從 sequence/track name 中繼事件中抓取序列名稱。                                                                                                                               |
| output          | 抓取目前輸出裝置的描述。 如果未設定輸出裝置，則會傳回「無」。                                                                                             |
| product         | 抓取裝置的描述。 這種資訊通常包含產品名稱和型號。 字串長度將是31個字元或更少。                                               |
| 仍為演算法 | 傳回目前靜止影像壓縮演算法的名稱。                                                                                                                                 |
| 仍為品質   | 傳回目前靜止影像品質描述項的名稱。 如果應用程式將參數設定為未對應至已定義品質的特定值，這可能會傳回「未知」。 |
| usage           | 傳回字串，這個字串描述工作區中視覺效果或音訊資料的擁有者可能會加諸的使用限制。                                                                    |
| version         | 傳回設備磁碟機和硬體的版本層級。                                                                                                                                       |
| 影片演算法 | 傳回目前視訊壓縮演算法的名稱。                                                                                                                                       |
| 影片品質   | 傳回目前影片品質描述項的名稱。 如果應用程式將參數設定為未對應至已定義品質的特定值，這可能會傳回「未知」。       |
| 視窗文字     | 抓取裝置使用的視窗標題。                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="examples"></a>範例

下列命令會抓取與 "mysound" 裝置相關聯的硬體描述。

``` syntax
info mysound product
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> <dt>

[載入](load.md)
</dt> </dl>

 

