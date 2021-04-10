---
description: 取得值，這個值會指出設定檔是否為相關聯之 IWiaItem2 裝置的預設掃描設定檔。
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'IScanProfile：： IsDefault 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943585"
---
# <a name="iscanprofileisdefault-method"></a>IScanProfile：： IsDefault 方法

取得值，這個值會指出設定檔是否為相關聯之 [**IWiaItem2**](-wia-iwiaitem2.md) 裝置的預設掃描設定檔。

## <a name="syntax"></a>語法


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbDefault* \[擴展\]
</dt> <dd>

類型： **BOOL \** _

_ * BOOL * * 的指標。

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**真**


</dt> <dd>

設定檔是預設值。

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**假**


</dt> <dd>

設定檔不是預設值。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

如果設定檔包含元素，則 *pbDefault* 為 **TRUE** `<Default>` 。 如果沒有這樣的元素，則為 **FALSE** 。 元素沒有值。

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

 

 




