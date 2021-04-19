---
description: 如果目前已暫止封裝的進程，則繼續執行。
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: IPackageDebugSettings：： Resume 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971213"
---
# <a name="ipackagedebugsettingsresume-method"></a>IPackageDebugSettings：： Resume 方法

如果目前已暫止封裝的進程，則繼續執行。

## <a name="syntax"></a>語法


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*packageFullName* \[在\]
</dt> <dd>

類型： **LPCWSTR**

封裝的完整名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

每個進程都會收到 [**繼續**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) 的事件。 這對開發人員而言非常有用，可逐步瞭解其應用程式如何回應此事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                          |
| Idl<br/>                      | <dl> <dt>Shobjidl.h .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
