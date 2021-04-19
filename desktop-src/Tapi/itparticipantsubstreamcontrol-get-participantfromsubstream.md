---
description: Get \_ ParticipantFromSubStream 方法可讓應用程式探索哪些參與者與指定的子串流相關聯。
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'ITParticipantSubStreamControl：： get_ParticipantFromSubStream 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999630"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a>ITParticipantSubStreamControl：： get \_ ParticipantFromSubStream 方法

\[**取得 \_ParticipantFromSubStream** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ ParticipantFromSubStream** 方法可讓應用程式探索哪些參與者與指定的子串流相關聯。

## <a name="syntax"></a>語法


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pITSubStream* \[在\]
</dt> <dd>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)介面的指標。

</dd> <dt>

*ppParticipant* \[擴展\]
</dt> <dd>

[**ITParticipant**](itparticipant.md)介面指標的陣列指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                     | Description                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>            | 方法成功。<br/>                                                       |
| <dl> <dt>**E \_ 指標**</dt> </dl>       | *PITSubStream* 或 *ppParticipant* 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | *PITSubStream* 參數未指向有效的介面。<br/>         |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | 沒有任何與子流相關聯的參與者。<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | 記憶體不足，無法執行操作。<br/>                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

