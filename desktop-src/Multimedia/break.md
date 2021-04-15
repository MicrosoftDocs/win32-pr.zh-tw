---
title: break 命令
description: Break 命令會指定要中止使用 \ 0034 叫用之命令的索引鍵; wait \ 0034;國旗。 此命令是 MCI 系統命令;它是由 MCI 直接解讀。
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- 中斷命令 Windows 多媒體
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466785"
---
# <a name="break-command"></a>break 命令

Break 命令會指定索引鍵，以中止使用 "wait" 旗標叫用的命令。 此命令是 MCI 系統命令;它是由 MCI 直接解讀。

若要傳送此命令，請使用 *lpszCommand* 參數設定來呼叫 [**mciSendString**](/previous-versions//dd757161(v=vs.85))函式，如下所示。

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

MCI 裝置的識別碼。 開啟裝置時，會指派此識別碼或別名。

</dd> <dt>

<span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*
</dt> <dd>

下列其中一個旗標。



| 值                 | 意義                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| on *virtual key 程式碼* | 指定中止使用 "wait" 旗標啟動之命令的金鑰。 |
| 關                   | 停用目前的 break 鍵。                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

可以是「等候」、「通知」或兩者。 針對數位影片和 VCR 裝置，也可以指定「測試」。 如需這些旗標的詳細資訊，請參閱 [Wait、Notify 和 Test 旗標](the-wait-notify-and-test-flags.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="remarks"></a>備註

當啟用 break 鍵，且使用者按下 *lpszVirtKey* 參數中指定的虛擬金鑰程式碼所識別的金鑰時，裝置會將控制權傳回給應用程式。 可能的話，命令會繼續執行。

## <a name="examples"></a>範例

下列命令會將 F2 設定為 "mysound" 裝置的 break 鍵。

``` syntax
break mysound on 113
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
</dt> </dl>

 

