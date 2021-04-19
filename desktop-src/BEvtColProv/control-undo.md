---
description: 從先前的備份檔案還原收集器的使用中設定， (由從目前的原始時間戳記) 來判斷。
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Control 類別的 Undo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 285f1ec39ea52f6c388e324f72745d72f65207e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970903"
---
# <a name="undo-method-of-the-control-class"></a>Control 類別的 Undo 方法

從先前的備份檔案還原收集器的使用中設定， (由從目前的原始時間戳記) 來判斷。 如果設定是剛設定的，這表示還原該變更。 連續的呼叫將會復原到先前和先前的設定。 在成功時傳回1，錯誤則為0。

## <a name="syntax"></a>語法


```mof
Uint32 Undo(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OldTimestampLow* \[在\]
</dt> <dd>

設定先前設定的時間戳記。 如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。

</dd> <dt>

*OldTimestampHigh* \[在\]
</dt> <dd>

設定先前設定的時間戳記。 如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。

</dd> <dt>

*NewTimestampLow* \[擴展\]
</dt> <dd>

如果呼叫成功，則為設定新設定的時間戳記。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。

</dd> <dt>

*NewTimestampHigh* \[擴展\]
</dt> <dd>

如果呼叫成功，則為設定新設定的時間戳記。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。

</dd> <dt>

*OriginalTimestampLow* \[擴展\]
</dt> <dd>

第一次設定還原設定時的原始時間戳記。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。

</dd> <dt>

*OriginalTimestampHigh* \[擴展\]
</dt> <dd>

第一次設定還原設定時的原始時間戳記。 這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。

</dd> <dt>

*ErrorString* \[擴展\]
</dt> <dd>

包含錯誤說明的文字字串。

</dd> <dt>

*WarningString* \[擴展\]
</dt> <dd>

具有警告的文字字串。

</dd> <dt>

*InfoString* \[擴展\]
</dt> <dd>

包含設定相關資訊的文字字串。

</dd> <dt>

*ErrorType* \[擴展\]
</dt> <dd>

錯誤的類型：請注意，0或不存在表示成功。

<dt>

0
</dt> <dd>

成功。

</dd> <dt>

1
</dt> <dd>

錯誤引數格式

</dd> <dt>

2
</dt> <dd>

錯誤的引數值

</dd> <dt>

3
</dt> <dd>

資源 (通訊端) 開啟錯誤

</dd> <dt>

4
</dt> <dd>

持續性 (檔案寫入) 錯誤

</dd> <dt>

5
</dt> <dd>

不可部分完成性錯誤 (舊的時間戳記不相符) 

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

<dl> <dt>


</dt> <dd>

0

失敗

</dd> <dt>


</dt> <dd>

1

Success

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                       |
| 命名空間<br/>                | 根 \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**控制**](control.md)
</dt> </dl>

 

