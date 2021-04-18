---
description: Get \_ LocalParticipantTypedInfo 方法會取得參與者資訊，例如電子郵件名稱或地理位置。
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'ITLocalParticipant：： get_LocalParticipantTypedInfo 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976162"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>ITLocalParticipant：： get \_ LocalParticipantTypedInfo 方法

**Get \_ LocalParticipantTypedInfo** 方法會取得參與者資訊，例如電子郵件名稱或地理位置。

## <a name="syntax"></a>語法


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*InfoType* \[在\]
</dt> <dd>

[**參與者 \_所 \_**](participant-typed-info.md) 需資訊類型的類型資訊識別碼。

</dd> <dt>

*ppInfo* \[擴展\]
</dt> <dd>

在成功傳回方法之後，將包含所需資訊的 **BSTR** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

應用程式必須使用 [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppInfo* 參數的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**參與者 \_ 輸入 \_ 資訊**](participant-typed-info.md)
</dt> </dl>

 

