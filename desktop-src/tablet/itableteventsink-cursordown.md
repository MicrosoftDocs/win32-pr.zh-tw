---
description: 手寫筆提示接觸到數位化的平板電腦介面時發生。
ms.assetid: 7f4a441d-00d2-4120-8a8d-d3496cdc7e58
title: ITabletEventSink：： CursorDown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorDown
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 1f0ffbe8c300e3c227cd59d8ff391b8990873c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693344"
---
# <a name="itableteventsinkcursordown-method"></a>ITabletEventSink：： CursorDown 方法

手寫筆提示接觸到數位化的平板電腦介面時發生。

## <a name="syntax"></a>語法


```C++
HRESULT CursorDown(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tcid* \[在\]
</dt> <dd>

Tablet 的識別碼。

</dd> <dt>

 \[ 中的 cid\]
</dt> <dd>

手寫筆的識別碼。

</dd> <dt>

*nSerialNumber* \[在\]
</dt> <dd>

手寫筆的序號。

</dd> <dt>

*cbPkt* \[在\]
</dt> <dd>

手寫筆資料封包中的位元組數目。

</dd> <dt>

*pbPkt* \[在\]
</dt> <dd>

手寫筆資料，指出手寫筆接觸 tablet 的位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletEventSink 介面**](itableteventsink.md)
</dt> </dl>

 

 




