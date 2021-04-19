---
description: 設定與設定檔相關聯之 Windows 映像取得 (WIA) 2.0 專案的類別 GUID。
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'IScanProfile：： SetItem 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996607"
---
# <a name="iscanprofilesetitem-method"></a>IScanProfile：： SetItem 方法

設定與設定檔相關聯之 Windows 映像取得 (WIA) 2.0 專案的類別 GUID。

## <a name="syntax"></a>語法


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*guidCategory* \[在\]
</dt> <dd>

類型： **GUID**

WIA 2.0 專案分類的 GUID。 這必須是其中一個 WIA \_ IPA \_ 專案 \_ 類別常數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

使用者可以使用 [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法來變更類別。

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

[掃描設定檔架構](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




