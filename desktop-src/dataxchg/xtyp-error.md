---
title: 'XTYP_ERROR 交易 (Ddeml .h) '
description: 當發生重大錯誤時，動態資料交換 (DDE) 回呼函式 DdeCallback 會接收 XTYP \_ 錯誤交易。
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- XTYP_ERROR 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967733"
---
# <a name="xtyp_error-transaction"></a>XTYP \_ 錯誤交易

當發生重大錯誤時，動態資料交換 (DDE) 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)會接收 **XTYP \_ 錯誤** 交易。


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>參數

<dl> <dt>

*uType* 
</dt> <dd>

交易類型。

</dd> <dt>

*uFmt* 
</dt> <dd>

未使用。

</dd> <dt>

*hconv* 
</dt> <dd>

與錯誤相關聯之交談的控制碼。 如果錯誤未與交談相關聯，此參數為 **Null** 。

</dd> <dt>

*hsz1* 
</dt> <dd>

未使用。

</dd> <dt>

*hsz2* 
</dt> <dd>

未使用。

</dd> <dt>

*hdata* 
</dt> <dd>

未使用。

</dd> <dt>

*dwData1* 
</dt> <dd>

低序位單字的錯誤碼。 目前僅支援下列錯誤碼。



| 值                                                                                                                                                                      | 意義                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**DMLERR \_ \_ 記憶體不足**</dt> </dl> | 記憶體偏低;建議、執行資料可能會遺失，或者系統可能會失敗。<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="remarks"></a>備註

應用程式無法封鎖此交易類型;會忽略 **CBR \_ 區塊** 傳回碼。 動態資料交換管理程式庫 (DDEML) 藉由移除非關鍵的資源來嘗試釋放記憶體。 已封鎖交談的應用程式應該將其解除封鎖。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Ddeml (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[動態資料交換管理程式庫總覽](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

