---
description: Get \_ ParticipantTypedInfo 方法會取得所需資訊類型的 BSTR 標記法，例如 PTI \_ EMAILADDRESS。
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'ITParticipant：： get_ParticipantTypedInfo 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989499"
---
# <a name="itparticipantget_participanttypedinfo-method"></a>ITParticipant：： get \_ ParticipantTypedInfo 方法

\[**取得 \_ParticipantTypedInfo** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ ParticipantTypedInfo** 方法會取得所需資訊類型的 **BSTR** 標記法，例如 PTI \_ EMAILADDRESS。

## <a name="syntax"></a>語法


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*InfoType* \[在\]
</dt> <dd>

[**參與者 \_所 \_**](participant-typed-info.md) 需資訊類型的類型資訊描述元。

</dd> <dt>

*ppInfo* \[擴展\]
</dt> <dd>

所需資訊的 **BSTR** 標記法指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                    | Description                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>           | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 失敗**</dt> </dl>         | 將資訊儲存到 *ppInfo* 失敗。<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | *InfoType* 參數無效。<br/>               |
| <dl> <dt>**E \_ 指標**</dt> </dl>      | *PpInfo* 參數不是有效的指標。<br/>       |
| <dl> <dt>**TAPI \_ E \_ NOITEM**</dt> </dl> | TAPI 沒有指定類型的資訊。<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | 記憶體不足，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppInfo* 參數的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**參與者 \_ 輸入 \_ 資訊**](participant-typed-info.md)
</dt> <dt>

[**媒體類型**](tapimediatype--constants.md)
</dt> </dl>

 

