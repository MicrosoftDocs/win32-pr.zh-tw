---
description: 在中移除指定的子屬性清單 <Properties> 掃描設定檔的元素。
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'IScanProfile：： RemoveProperty 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113909"
---
# <a name="iscanprofileremoveproperty-method"></a>IScanProfile：： RemoveProperty 方法

在掃描設定檔的元素中移除指定的子屬性清單 `<Properties>` 。

## <a name="syntax"></a>語法


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*num* \[在\]
</dt> <dd>

類型： **ULONG**

由 *pid* 指向之陣列中的專案數。

</dd> <dt>

*pid* \[在\]
</dt> <dd>

類型： **PROPID \** _

要刪除之屬性識別碼陣列的指標。 每個都是 [WIA 屬性常數](-wia-wia-property-constants.md)。

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

 

 




