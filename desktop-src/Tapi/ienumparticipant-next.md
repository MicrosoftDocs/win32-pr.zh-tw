---
description: 下一個方法會取得列舉順序中的下一個指定元素數目。 這種方法在 Visual Basic 和指令碼語言中是隱藏的。
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'IEnumParticipant：： Next 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996496"
---
# <a name="ienumparticipantnext-method"></a>IEnumParticipant：： Next 方法

\[**接下來** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**下一個** 方法會取得列舉順序中的下一個指定元素數目。 這種方法在 Visual Basic 和指令碼語言中是隱藏的。

## <a name="syntax"></a>語法


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*celt* \[在\]
</dt> <dd>

要求的元素數目。

</dd> <dt>

*ppElements* \[擴展\]
</dt> <dd>

[**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)介面的指標。

</dd> <dt>

*pceltFetched* \[擴展\]
</dt> <dd>

實際提供的元素數目指標。 如果 *celt* 是1，則可能為 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法傳回 *celt* 元素數目。<br/>           |
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | 剩餘的元素數目小於 *celt*。<br/>   |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpElements* 參數不是有效的指標。<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

TAPI 會呼叫 **IEnumParticipant：： Next** 所傳回的 [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)介面上的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)方法。 應用程式必須在 **ITAgentHandler** 介面上呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，才能釋放與其相關聯的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

