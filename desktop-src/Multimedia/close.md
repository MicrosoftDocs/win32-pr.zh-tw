---
title: '關閉命令 (Corecrt- \_ .h) '
description: Close 命令會關閉裝置或檔案，以及任何相關聯的資源。 當裝置或所有檔案的所有實例都已關閉時，MCI 會卸載裝置。 所有 MCI 裝置都會辨識此命令。
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- 關閉命令 Windows 多媒體
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02acd3ebe3d45a402ae565c6fcac121f712df4374924bcb0e02c3dcadf9ceeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807957"
---
# <a name="close-command"></a>關閉命令

Close 命令會關閉裝置或檔案，以及任何相關聯的資源。 當裝置或所有檔案的所有實例都已關閉時，MCI 會卸載裝置。 所有 MCI 裝置都會辨識此命令。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
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

可以是「等候」、「通知」或兩者。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

若要關閉應用程式所開啟的所有裝置，請為 *lpszDeviceID* 參數指定 "all" 裝置識別碼。

關閉 **cdaudio** 裝置會停止播放音訊。

**Windows 2000/XP：** 如果 **cdaudio** 裝置現正播放，關閉 **cdaudio** 裝置並不會導致音訊停止播放。 先傳送 [停止](stop.md) 命令。

## <a name="examples"></a>範例

下列命令會關閉 "mysound" 裝置。

``` syntax
close mysound
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Corecrt \_ 的 io。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 命令字串](mci-command-strings.md)
</dt> </dl>

 

