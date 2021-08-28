---
title: PxeProviderShutdown 回呼函式
description: 呼叫以關閉提供者。
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- PxeProviderShutdown 回呼函式 Windows 部署服務
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5efc7267a5b5e1c15d185b96419210f31981c56c887dd5a8ab7f1068eb4f20ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860788"
---
# <a name="pxeprovidershutdown-callback-function"></a>PxeProviderShutdown 回呼函式

呼叫以關閉提供者。 藉由呼叫 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數，並將 *CallbackType* 參數設定為 **PXE \_ 回呼 \_ SHUTDOWN**，即可註冊此函式。 呼叫此函式之後，傳遞給 [*PxeProviderInitialize*](pxeproviderinitialize.md)函數的 *hProvider* 控制碼將不再有效。

## <a name="syntax"></a>語法


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtext* \[在\]
</dt> <dd>

傳遞至 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數的內容值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果提供者關閉成功，回呼應該會傳回 **錯誤 \_ 成功**。 如果發生失敗，則應該傳回適當的錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                          |
| 最低支援的伺服器<br/> | Windows伺服器2008、Windows server 2003 （ \[ 僅限 SP2 桌面應用程式）\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows部署服務伺服器函式](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderInitialize*](pxeproviderinitialize.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





