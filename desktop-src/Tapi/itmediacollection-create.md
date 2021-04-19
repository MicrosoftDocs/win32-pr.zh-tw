---
description: Create 方法會使用預設屬性來建立新的媒體，然後將它新增至集合中指定的索引處，並傳回 ITMedia 介面的指標。
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'ITMediaCollection：： Create 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996485"
---
# <a name="itmediacollectioncreate-method"></a>ITMediaCollection：： Create 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Create** 方法會使用預設屬性來建立新的媒體，然後將它新增至集合中指定的索引處，並傳回 [**ITMedia**](itmedia.md)介面的指標。

## <a name="syntax"></a>語法


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

新專案的索引。 索引的最小值是1，而索引的最大值是目前的專案數 + 1。

</dd> <dt>

*ppMedia* \[擴展\]
</dt> <dd>

已建立 [**ITMedia**](itmedia.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpMedia* 參數不是有效的指標。<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *索引* 參數無效。<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

大部分 C 和 c + + 清單都是以0為基礎，但是此索引是以1為基礎，Visual Basic 相容性，這表示第一個專案的索引編號為1。

TAPI 會在 **ITMediaCollection：： Create** 所傳回的 [**ITMedia**](itmedia.md)介面上呼叫 **AddRef** 方法。 應用程式必須在 [**ITMedia**](itmedia.md)介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




