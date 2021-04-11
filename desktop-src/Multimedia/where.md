---
title: where 命令
description: Where 命令會捕獲指定來源或目的地區域的矩形。 這個矩形是使用 put 命令指定的。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- where 命令 Windows 多媒體
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934934"
---
# <a name="where-command"></a>where 命令

Where 命令會捕獲指定來源或目的地區域的矩形。 這個矩形是使用 [put](put.md) 命令指定的。 數位影片和影片重迭裝置會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*
</dt> <dd>

識別要抓取其維度之矩形的旗標。 下表列出可辨識 **where** 命令和每個型別所使用之旗標的裝置類型。



| 值        | 意義                                                       | 意義                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| digitalvideo | destinationdestination [**max**](max.md)frameframe maxsource | 來源 maxvideovideo maxwindowwindow 最大值 |
| overlay      | destinationframe                                              | sourcevideo                              |



 

下表列出可在 **lpszRequestRect** 參數中指定的旗標，以及它們的意義。



| 值                          | 意義                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 目的地                    | 抓取目的地位移和範圍。 若為影片重迭裝置，目的地矩形會定義顯示視窗工作區的區域，以顯示來自框架緩衝區的影像資料。                                                                                             |
| 目的地 [**最大值**](max.md) | 抓取用戶端矩形的目前大小。                                                                                                                                                                                                                                                  |
| 框架                          | 抓取框架緩衝區矩形的位移和範圍。 框架緩衝區矩形會定義接收傳入影片資料的框架緩衝區區域。 「影片」矩形中的影像會縮放到此區域。                                                                     |
| [**最大** 框架](max.md)       | 傳回框架緩衝區的大小上限。                                                                                                                                                                                                                                                        |
| source                         | 捕獲來源位移和範圍。 若為影片重迭裝置，來源矩形會定義在目的地視窗中顯示的框架緩衝區區域。 裝置會使用這個矩形來裁剪影像，再將它伸展，以符合顯示上的目的地矩形。 |
| 來源 [**最大值**](max.md)      | 抓取框架緩衝區的大小上限。                                                                                                                                                                                                                                                      |
| 影片                          | 捕獲影片矩形的位移和範圍。 影片矩形會定義傳送至框架緩衝區之傳入影片資料的區域。                                                                                                                                   |
| 影片 [**最大值**](max.md)       | 傳回輸入的大小上限。                                                                                                                                                                                                                                                               |
| 時間範圍                         | 抓取顯示視窗框架的目前大小和位置。                                                                                                                                                                                                                                 |
| 視窗 [**最大值**](max.md)      | 抓取整個顯示器的大小。                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 若為數位視訊裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函數的 *lpszReturnString* 參數中的矩形。 矩形描述此命令的 *lpszRequestRect* 參數中指定的區域。 矩形會指定為 *X1 Y1 X2 Y2*。 座標 *X1 Y1* 指定矩形的左上角，而座標 *X2 Y2* 指定寬度和高度。

## <a name="examples"></a>範例

下列命令會傳回 "movie" 裝置的顯示矩形。

``` syntax
where movie destination
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

[把](put.md)
</dt> </dl>

 

