---
description: 設定指定之子屬性的值。 <Properties> 掃描設定檔的元素。
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'IScanProfile：： SetProperty 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691104"
---
# <a name="iscanprofilesetproperty-method"></a>IScanProfile：： SetProperty 方法

在掃描設定檔的元素中，設定指定之子屬性的值 `<Properties>` 。

## <a name="syntax"></a>語法


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
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

_pvar * \[ in\]
</dt> <dd>

類型： **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

要指派給屬性之值陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： _ *HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

在陣列中， *pid* 指向的每個值是其中一個 [WIA 屬性常數](-wia-wia-property-constants.md)。 您可以擴充此識別系統。 請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)。

設定檔的變更不會儲存到磁片，直到應用程式呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法為止。

如果兩個應用程式會從相同的 XML 檔案建立掃描設定檔物件，而且每個應用程式都會將變更寫入其物件，則只有呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) last 的應用程式所做的變更會儲存到磁片。

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

 

 
