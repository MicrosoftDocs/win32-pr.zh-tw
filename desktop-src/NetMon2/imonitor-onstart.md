---
description: OnStart 方法是可由監視器執行的選擇性方法。 MCSVC 會呼叫這個方法來要求監視啟動捕獲。
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'IMonitor：： OnStart 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112208"
---
# <a name="imonitoronstart-method"></a>IMonitor：： OnStart 方法

**OnStart** 方法是可由監視器執行的選擇性方法。 MCSVC 會呼叫這個方法來要求監視啟動捕獲。

## <a name="syntax"></a>語法


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pUnkNPP* \[在\]
</dt> <dd>

[IRTC](irtc.md)介面的[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標。 監視器可以使用這個介面來取得可用來判斷是否應該啟動 capture 的統計資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。 傳回 S \_ OK 時，MCSVC 會呼叫 [IRTC：： Start](irtc-start.md) 方法。

如果此方法不成功，則傳回值會是錯誤碼。 如果傳回任何錯誤碼，MCSVC 將不會啟動 capture。

## <a name="remarks"></a>備註

MCSVC 會先呼叫這個方法，然後呼叫 NPP 的 [IRTC：： start](irtc-start.md) 方法來啟動 capture。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IMonitor](imonitor.md)
</dt> <dt>

[網路封包提供者](network-packet-providers.md)
</dt> </dl>

 

