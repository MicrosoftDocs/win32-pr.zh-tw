---
description: 取得在中指定之子屬性的值。 <Properties> 掃描設定檔的元素。
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'IScanProfile：： GetProperty 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974140"
---
# <a name="iscanprofilegetproperty-method"></a>IScanProfile：： GetProperty 方法

取得掃描設定檔的元素中指定之子屬性的值 `<Properties>` 。

## <a name="syntax"></a>語法


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*num* \[在\]
</dt> <dd>

類型： **ULONG**

由 *pid* 和 *pvar* 指向的陣列中的專案數。

</dd> <dt>

*pid* \[在\]
</dt> <dd>

類型： **PROPID \** _

要設定之屬性識別碼陣列的指標。 陣列中的每個值都是 [WIA 屬性常數](-wia-wia-property-constants.md)。

</dd> <dt>

_pvar * \[ out\]
</dt> <dd>

類型： **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

值陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

\_如果沒有任何屬性值可供使用，則傳回 FALSE，否則傳回 s \_ OK 或 standard COM 錯誤碼。

## <a name="remarks"></a>備註

每個值的類型都必須與呼叫 [**IScanProfile：： SetProperty**](-wia-iscanprofile-setproperty.md)時所設定的類型相同。

在陣列中， *pid* 指向的每個值是其中一個 [WIA 屬性常數](-wia-wia-property-constants.md)。 您可以擴充此識別系統。 請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)。

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

**概念**
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> <dt>

[WIA 屬性常數](-wia-wia-property-constants.md)
</dt> <dt>

[定義自訂屬性](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
