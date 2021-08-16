---
title: PxeProviderInitialize 回呼函式
description: 從提供者動態連結程式庫匯出 (DLL) ，它會初始化提供者，並讓它準備好接收用戶端要求。
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- PxeProviderInitialize 回呼函式 Windows 部署服務
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6eb7ba32049dc3ef70085a489b499d90b92ec6155323b650df0e2b2f839bbdf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098658"
---
# <a name="pxeproviderinitialize-callback-function"></a>PxeProviderInitialize 回呼函式

從提供者動態連結程式庫匯出 (DLL) ，它會初始化提供者，並讓它準備好接收用戶端要求。 需要提供者才能匯出 *PxeProviderInitialize* 函數。 對提供者的任何回呼都必須在處理 *PxeProviderInitialize* 期間，向 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)函式的呼叫註冊。 當此函式傳回時，提供者必須完全初始化並準備好處理用戶端要求。

## <a name="syntax"></a>語法


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProvider* \[在\]
</dt> <dd>

提供者實例的控制碼。 這個控制碼必須由提供者儲存，並在後續的呼叫中使用。 在呼叫 [*PxeProviderShutdown*](pxeprovidershutdown.md) 回呼函式之前，這個控制碼是有效的。

</dd> <dt>

*hProviderKey* \[在\]
</dt> <dd>

要儲存提供者設定資訊之登錄機碼的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果提供者初始化成功，回呼應該會傳回 **錯誤 \_ 成功**。 如果發生失敗，則應該傳回適當的錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                          |
| 最低支援的伺服器<br/> | Windows伺服器2008、Windows server 2003 （ \[ 僅限 SP2 桌面應用程式）\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows部署服務伺服器函式](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





