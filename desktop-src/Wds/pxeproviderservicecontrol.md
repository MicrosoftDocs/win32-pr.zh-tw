---
title: PxeProviderServiceControl 回呼函式
description: 當 WDS 服務收到服務控制程式代碼時呼叫。
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- PxeProviderServiceControl 回呼函式 Windows 部署服務
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967966"
---
# <a name="pxeproviderservicecontrol-callback-function"></a>PxeProviderServiceControl 回呼函式

當 WDS 服務收到服務控制程式代碼時呼叫。 藉由呼叫 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數，並將 *CallbackType* 參數設定為 **PXE \_ 回呼 \_ 服務 \_ 控制**，即可註冊此回呼函式。

## <a name="syntax"></a>語法


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtext* \[在\]
</dt> <dd>

傳遞至 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數的內容值。

</dd> <dt>

*dwControl* 
</dt> <dd>

控制程式代碼。 如需可能值的清單，請參閱 [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)函數的 *dwControl* 參數。

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

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

