---
description: ITMediaCollection：： get__NewEnum 方法-get \_ \_ NewEnum 方法會傳回集合的列舉值。
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: 'ITMediaCollection：： get__NewEnum 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6683ce0a00f0128cb959dd5a2c39e8b06382f65d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098356"
---
# <a name="itmediacollectionget__newenum-method"></a>ITMediaCollection：： get \_ \_ NewEnum 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ \_ NewEnum** 方法會傳回集合的列舉值。

## <a name="syntax"></a>語法


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[擴展\]
</dt> <dd>

集合之列舉值物件的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。

在傳回的 **IUnknown** 介面上呼叫 [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法，以取得集合上 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)列舉介面的指標。 **IEnumVARIANT** 提供數種方法，可讓您用來逐一查看集合。

如需詳細資訊，請參閱接下來的＜備註＞一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PVal* 參數不是有效的指標。<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

這個方法可以與 [**get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) 互換，不同之處在于它會傳回 **IUnknown** 而不是 [**IEnumMedia**](ienummedia.md)。

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

 

