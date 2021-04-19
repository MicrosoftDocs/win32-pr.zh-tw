---
description: Put \_ name 方法會設定會話名稱。
ms.assetid: aba05cdb-a870-490e-8bb0-98b11780b112
title: 'ITSdp：:p ut_Name 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7383183b6b367d71d18070eedd5857740665fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992924"
---
# <a name="itsdpput_name-method"></a>ITSdp：:p 的內容 \_ 名稱方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Put \_ name** 方法會設定會話名稱。

## <a name="syntax"></a>語法


```C++
HRESULT put_Name(
  [in] BSTR pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

包含會話名稱之 **BSTR** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PName* 參數不是有效的指標。<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pName* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp：： get \_ Name**](itsdp-get-name.md)
</dt> </dl>

 

