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
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966533"
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
| 最低支援的伺服器<br/> | 僅限 windows Server 2008、Windows Server 2003 SP2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows 部署服務伺服器函數](windows-deployment-services-server-functions.md)
</dt> <dt>

[*PxeProviderShutdown*](pxeprovidershutdown.md)
</dt> </dl>

 

 





