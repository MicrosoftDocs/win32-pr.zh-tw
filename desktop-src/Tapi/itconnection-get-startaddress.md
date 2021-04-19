---
description: Get \_ StartAddress 方法會取得要用於會話的第一個位址。
ms.assetid: 3c4fec19-1b7d-4052-afd8-7aaf095907d0
title: 'ITConnection：： get_StartAddress 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84266d1874e7d04acb594bcfb9d99b440b0390b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000006"
---
# <a name="itconnectionget_startaddress-method"></a>ITConnection：： get \_ StartAddress 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ StartAddress** 方法會取得要用於會話的第一個位址。

## <a name="syntax"></a>語法


```C++
HRESULT get_StartAddress(
  [out] BSTR *ppStartAddress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppStartAddress* \[擴展\]
</dt> <dd>

包含會話起始位址之 **BSTR** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                      |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpStartAddress* 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>   |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                     |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                    |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppStartAddress* 參數的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

