---
title: 載入命令
description: Load 命令會以裝置特定的格式載入檔案。 數位影片和影片重迭裝置會辨識此命令。
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- Windows 多媒體載入命令
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c66822de727ea45e93839c710dae19739cba8adaac8b571846c1fa23ef0083c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139353"
---
# <a name="load-command"></a>載入命令

Load 命令會以裝置特定的格式載入檔案。 數位影片和影片重迭裝置會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*
</dt> <dd>

要載入的路徑和檔案名。 針對影片重迭裝置，這也可以包含資料的目標矩形。 若要指定目標矩形，請指定 "at"，後面接著 **X1 Y1 X2 Y2**，其中 **x1 y1** 指定矩形的左上角，而 **X2 Y2** 指定寬度和高度。 矩形相對於影片緩衝區來源。

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 若為數位視訊裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

當載入完成時，"vidboard" 裝置會傳送通知訊息。

## <a name="examples"></a>範例

下列命令會將檔案載入至 "vidboard" 裝置。

``` syntax
load vidboard c:\vid\fish.vid notify
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
</dt> </dl>

 

