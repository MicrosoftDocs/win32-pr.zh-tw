---
title: 復原命令
description: '[復原] 命令會反轉最新成功的複製、剪下、刪除、復原或貼上命令所採取的動作。 數位影片裝置辨識此命令。'
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- 復原命令 Windows 多媒體
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0814dff2c684095299b6820b8dc9a2464aa26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025461"
---
# <a name="undo-command"></a>復原命令

[復原] 命令會反轉最新成功的 [複製](copy.md)、 [剪](cut.md)下、 [刪除](delete.md)、復原或 [貼](paste.md) 上命令所採取的動作。 數位影片裝置辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」、「測試」或它們的組合。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

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

[copy](copy.md)
</dt> <dt>

[削減](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[粘貼](paste.md)
</dt> </dl>

 

