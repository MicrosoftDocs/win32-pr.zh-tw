---
description: 從 Microsoft 媒體基礎影片轉譯接收器取得 IMFDXGIDeviceManager。
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: IMFDXGIDeviceManagerSource：： GetManager 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974641"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a>IMFDXGIDeviceManagerSource：： GetManager 方法

從 Microsoft 媒體基礎影片轉譯接收器取得 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppManager* \[擴展\]
</dt> <dd>

[**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                       |
| Idl<br/>                      | <dl> <dt>Mfidl .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFDXGIDeviceManagerSource**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




