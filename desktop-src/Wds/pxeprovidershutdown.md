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
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980288"
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
| 最低支援的伺服器<br/> | 僅限 windows Server 2008、Windows Server 2003 SP2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows 部署服務伺服器函數](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderInitialize*](pxeproviderinitialize.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





