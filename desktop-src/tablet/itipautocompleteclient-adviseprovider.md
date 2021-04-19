---
description: 向用戶端註冊提供者，以讓用戶端呼叫應用程式的自動完成提供者物件。
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'ITipAutocompleteClient：： AdviseProvider 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981619"
---
# <a name="itipautocompleteclientadviseprovider-method"></a>ITipAutocompleteClient：： AdviseProvider 方法

向用戶端註冊提供者，以讓用戶端呼叫應用程式的自動完成提供者物件。

## <a name="syntax"></a>語法


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWndField* \[在\]
</dt> <dd>

提供自動完成功能的欄位的視窗控制碼。

</dd> <dt>

*pIACProvider* \[在\]
</dt> <dd>

自動完成提供者介面的介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                       |
| 標頭<br/>                   | <dl> <dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITipAutocompleteClient 介面**](itipautocompleteclient.md)
</dt> <dt>

[**ITipAutocompleteClient：： UnadviseProvider 方法**](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[文字輸入面板參考](text-input-panel-reference.md)
</dt> </dl>

 

 




