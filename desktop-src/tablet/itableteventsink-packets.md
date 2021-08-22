---
description: 手寫筆在數位板上移動時發生。
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: ITabletEventSink：:P ackets 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 29b118771fb5217ed13c01ef9376ad9b426e1ecd74a4bf931d8412a0b47e913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712118"
---
# <a name="itableteventsinkpackets-method"></a>ITabletEventSink：:P ackets 方法

手寫筆在數位板上移動時發生。

## <a name="syntax"></a>語法


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tcid* \[在\]
</dt> <dd>

Tablet 的識別碼。

</dd> <dt>

*cPkts* \[在\]
</dt> <dd>

封包數目。

</dd> <dt>

*cbPkts* \[在\]
</dt> <dd>

封包緩衝區的大小

</dd> <dt>

*pbPkts* \[在\]
</dt> <dd>

封包緩衝區。

</dd> <dt>

*pnSerialNumbers* \[在\]
</dt> <dd>

序號陣列。

</dd> <dt>

*Cid* 
</dt> <dd>

手寫筆的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | 描述                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletEventSink 介面**](itableteventsink.md)
</dt> </dl>

 

 




