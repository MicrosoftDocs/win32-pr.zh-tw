---
description: 設定收集器的新使用中設定。
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Control 類別的 SetConfiguration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688568"
---
# <a name="setconfiguration-method-of-the-control-class"></a>Control 類別的 SetConfiguration 方法

設定收集器的新使用中設定。

## <a name="syntax"></a>語法


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Config* \[在\]
</dt> <dd>

要啟動的設定。

</dd> <dt>

*OldTimestampLow* \[在\]
</dt> <dd>

時間戳記的低序位位，指出目前使用中的設定是否已設定。 如果這個屬性未設定為0，則會啟用不可部分完成性檢查。

</dd> <dt>

*OldTimestampHigh* \[在\]
</dt> <dd>

時間戳記的高序位位，指出目前使用中的設定是否已設定。 如果這個屬性未設定為0，則會啟用不可部分完成性檢查。

</dd> <dt>

*NewTimestampLow* \[擴展\]
</dt> <dd>

當此方法傳回時，此參數會包含時間戳記的低序位位，指出設定新設定的時間。 如果這個屬性未設定為0，則會啟用不可部分完成性檢查。

</dd> <dt>

*NewTimestampHigh* \[擴展\]
</dt> <dd>

當此方法傳回時，此參數會包含時間戳記的高序位位，指出設定新設定的時間。 如果這個屬性未設定為0，則會啟用不可部分完成性檢查。

</dd> <dt>

*ErrorString* \[擴展\]
</dt> <dd>

當此方法傳回時，如果發生錯誤，此參數就會包含錯誤描述。

</dd> <dt>

*WarningString* \[擴展\]
</dt> <dd>

當此方法傳回時，此參數會包含任何作業的警告訊息。

</dd> <dt>

*InfoString* \[擴展\]
</dt> <dd>

當此方法傳回時，此參數會包含新的使用中設定的資訊。

</dd> <dt>

*ErrorType* \[擴展\]
</dt> <dd>

當此方法傳回時，如果發生錯誤，此參數會指出錯誤類型。

<dt>

0
</dt> <dd>

缺少新的設定。

</dd> <dt>

1
</dt> <dd>

新設定的格式無效。

</dd> <dt>

2
</dt> <dd>

新的設定無效。

</dd> <dt>

3
</dt> <dd>

開啟的通訊端造成錯誤。

</dd> <dt>

4
</dt> <dd>

發生檔案寫入錯誤。

</dd> <dt>

5
</dt> <dd>

發生不可部分完成性錯誤。

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

 

 




