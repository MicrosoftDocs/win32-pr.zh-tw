---
description: 取得與設定檔相關聯之 Windows 影像取得 (WIA) 2.0 專案的類別 GUID。
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'IScanProfile：： GetItem 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 5a7f52a2d89bbd35b59febb25528fe493c4b5646afc70251fc19978d6d6265db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451038"
---
# <a name="iscanprofilegetitem-method"></a>IScanProfile：： GetItem 方法

取得與設定檔相關聯之 Windows 影像取得 (WIA) 2.0 專案的類別 GUID。

## <a name="syntax"></a>語法


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pguidCategory* \[擴展\]
</dt> <dd>

類型： **GUID \***

WIA 2.0 專案分類的 GUID 指標。 這一律是其中一個 WIA \_ IPA \_ 專案 \_ 類別常數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofile。h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




