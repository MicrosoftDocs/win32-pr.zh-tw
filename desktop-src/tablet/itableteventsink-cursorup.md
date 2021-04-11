---
description: 發生于使用者從 tablet 數位板介面引發手寫筆時。
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: ITabletEventSink：： CursorUp 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195112"
---
# <a name="itableteventsinkcursorup-method"></a>ITabletEventSink：： CursorUp 方法

發生于使用者從 tablet 數位板介面引發手寫筆時。

## <a name="syntax"></a>語法


```C++
HRESULT CursorUp(
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

手寫筆資料，指出手寫筆從平板電腦中提起的位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

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

 

 




