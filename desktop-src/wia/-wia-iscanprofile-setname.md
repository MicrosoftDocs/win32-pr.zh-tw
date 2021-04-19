---
description: 設定設定檔的易記名稱。
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'IScanProfile：： SetName 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977921"
---
# <a name="iscanprofilesetname-method"></a>IScanProfile：： SetName 方法

設定設定檔的易記名稱。

## <a name="syntax"></a>語法


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrName* \[在\]
</dt> <dd>

類型： **BSTR**

設定檔的易記名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法是必要的，因為設定檔的 GUID 不能用來向使用者顯示掃描設定檔。

使用者可以使用 [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法來變更設定檔的易記名稱。

設定檔的變更不會儲存到磁片，直到應用程式呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) 方法為止。

如果兩個應用程式會從相同的 XML 檔案建立掃描設定檔物件，而且每個應用程式都會將變更寫入其物件，則只有呼叫 [**IScanProfile：： Save**](-wia-iscanprofile-save.md) last 的應用程式所做的變更會儲存到磁片。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Scanprofile。h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles .idl</dt> </dl> |



 

 




