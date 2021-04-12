---
title: PxeProviderRecvRequest 回呼函式
description: 從用戶端收到要求時呼叫。
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- PxeProviderRecvRequest 回呼函式 Windows 部署服務
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384665"
---
# <a name="pxeproviderrecvrequest-callback-function"></a>PxeProviderRecvRequest 回呼函式

從用戶端收到要求時呼叫。 此函式的註冊方式是呼叫 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函式，並將 *CallbackType* 參數設定為 **PXE \_ 回呼 \_ 接收 \_ 要求**。

## <a name="syntax"></a>語法


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hClientRequest* \[在\]
</dt> <dd>

從用戶端收到的要求控制碼。

</dd> <dt>

*pPacket* \[在\]
</dt> <dd>

記憶體緩衝區的指標，其中包含已接收的封包。

</dd> <dt>

*uPacketLen* \[在\]
</dt> <dd>

*PPacket* 參數所指向之緩衝區的長度（以位元組為單位）。

</dd> <dt>

*pLocalAddress* \[在\]
</dt> <dd>

[**PXE \_ 位址**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)結構的指標，其中包含接收封包的本機位址。

</dd> <dt>

*pRemoteAddress* \[在\]
</dt> <dd>

包含封包來源位址之 [**PXE \_ 位址**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) 結構的指標。

</dd> <dt>

*pAction* \[擴展\]
</dt> <dd>

指定系統應該採取的動作。



| 值                                                                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <dt>**PXE \_BA \_ NBP**</dt> <dt>1</dt> </dl>                | 此提供者會使用包含網路開機程式路徑的標準 DHCP 回應封包，回復至用戶端。 傳回此動作表示提供者已成功呼叫 [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) 函數一次，以順利完成用戶端要求。<br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <dt>**PXE \_BA \_ 自訂**</dt> <dt>2</dt> </dl>       | 提供者使用不符合 DHCP 規格的自訂回應來回複用戶端。 傳回此動作表示提供者已成功呼叫 [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) 函數一次，以順利完成用戶端要求。<br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <dt>**PXE \_BA \_ 忽略**</dt> <dt>3</dt> </dl>       | 提供者不會想要服務用戶端要求，且不應將要求傳遞給下一個提供者。 所有與用戶端要求相關聯的資源都會釋出，並忽略用戶端要求。 如果提供者辨識用戶端，但要求的格式不正確，則也可以使用此值。<br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <dt>**PXE \_BA 已 \_ 拒絕**</dt> <dt>4</dt> </dl> | 提供者不想要服務用戶端要求。 系統會將要求傳遞給已註冊之提供者清單中的下一個提供者。 如果這是清單中的最後一個提供者，則會釋放與用戶端要求相關聯的所有資源，並忽略用戶端要求。<br/>                     |



 

</dd> <dt>

*pCoNtext* \[在\]
</dt> <dd>

傳遞至 [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) 函數的內容值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果提供者已成功處理用戶端要求，回呼應該會傳回 **錯誤 \_ 成功**，而 *pAction* 參數所指向的 **PXE \_ 開機 \_ 動作** 則包含此要求的適當開機動作。 如果提供者將以非同步方式處理用戶端要求，則回呼應該會傳回 **錯誤 \_ IO \_ 暫** 止，並在處理用戶端要求時呼叫 [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) 函數。 如果發生失敗，則應該傳回適當的錯誤碼，而系統將繼續進行，就像是指定了 **PXE \_ BA \_ 拒絕** 的開機動作一樣。

## <a name="remarks"></a>備註

提供者看到的封包類型可以使用 [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) 函式來變更。

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
</dt> <dt>

[**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





