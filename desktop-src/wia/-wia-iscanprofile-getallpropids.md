---
description: 取得設定檔中的所有可用屬性識別碼。
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'IScanProfile：： GetAllPropIDs 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966758"
---
# <a name="iscanprofilegetallpropids-method"></a>IScanProfile：： GetAllPropIDs 方法

取得設定檔中的所有可用屬性識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*num* \[in、out\]
</dt> <dd>

類型： **ULONG \** _

要求或傳回的屬性識別碼數目。

</dd> <dt>

_ppid * \[ out\]
</dt> <dd>

類型： **PROPID \** _

屬性識別碼陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofile。h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




