---
description: 如果封裝目前正在執行，則暫停該封裝的進程。
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: IPackageDebugSettings：：暫止方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 0517ce3cca6a8e74f19b053897511062cefa252297d3a0e6633d4678c0deaa95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822811"
---
# <a name="ipackagedebugsettingssuspend-method"></a>IPackageDebugSettings：：暫止方法

如果封裝目前正在執行，則暫停該封裝的進程。

## <a name="syntax"></a>語法


```C++
HRESULT Suspend(
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

這個方法可以傳回其中一個值。



| 傳回碼                                                                                            | 描述                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 作業成功。<br/>              |
| <dl> <dt>**E 不 \_ 合法的 \_ STATECHANGE**</dt> </dl> | 進程目前未執行。<br/> |



 

## <a name="remarks"></a>備註

每個進程都會收到 [**暫停**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) 事件。 這對開發人員而言非常有用，可逐步瞭解其應用程式如何回應此事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                          |
| IDL<br/>                      | <dl> <dt>Shobjidl.h .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))
</dt> </dl>

 

 
