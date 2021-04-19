---
description: Delete 方法會刪除對應至指定之索引的媒體。
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: 'ITMediaCollection：:D elete 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978772"
---
# <a name="itmediacollectiondelete-method"></a>ITMediaCollection：:D elete 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Delete** 方法會刪除對應至指定之索引的媒體。

## <a name="syntax"></a>語法


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要刪除之媒體的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                                                              | Description                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                                     | 方法成功。<br/>                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                             | *索引* 參數的值小於1或大於目前的專案數目。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                            | 記憶體不足，無法執行操作。<br/>                                          |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                                                   | 內部錯誤 (只有在先前的呼叫傳回) 錯誤時才會發生。<br/>                      |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>                                                | 尚未實作這個方法。<br/>                                                           |
| <dl> <dt>**\_錯誤碼中的 HRESULT \_ \_ (SDPBLB \_ 會議 \_ BLOB \_ 損毀)**</dt> </dl> | SDP blob 不存在。<br/>                                                                   |



 

## <a name="remarks"></a>備註

大部分 C 和 c + + 清單都是以0為基礎，但是此索引是以1為基礎，Visual Basic 相容性，這表示第一個專案的索引編號為1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




