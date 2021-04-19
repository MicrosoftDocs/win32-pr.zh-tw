---
description: 下一個方法會取得列舉順序中的下一個指定元素數目。
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'IEnumMedia：： Next 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04b92220d8fe93058533427ff8cc7bcc7ad7a02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991353"
---
# <a name="ienummedianext-method"></a>IEnumMedia：： Next 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**下一個** 方法會取得列舉順序中的下一個指定元素數目。

## <a name="syntax"></a>語法


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*celt* \[在\]
</dt> <dd>

要求的元素數目。

</dd> <dt>

*pVal* \[擴展\]
</dt> <dd>

[**ITMedia**](itmedia.md)介面的指標。

</dd> <dt>

*pceltFetched* \[擴展\]
</dt> <dd>

實際提供專案數目的指標。 如果 *celt* 是1，則可能為 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                     | 意義                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 方法傳回 *celt* 元素數目。<br/>         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | 剩餘的元素數目小於 *celt*。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl> | *PVal* 參數不是有效的指標。<br/>       |



 

## <a name="remarks"></a>備註

TAPI 會呼叫 **IEnumMedia：： Next** 所傳回的 [**ITMedia**](itmedia.md)介面上的 **AddRef** 方法。 應用程式必須在 **ITMedia** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




