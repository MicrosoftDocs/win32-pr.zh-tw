---
description: 在目前的使用者內容中，授與指定的 DDE 共用信任狀態。
ms.assetid: 508d3603-468c-4ecb-8e5c-0ab86c2ff3b4
title: 'NDdeSetTrustedShare 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeSetTrustedShare
- NDdeSetTrustedShareA
- NDdeSetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 459e1621848e212522064ff6f01316fc23183bc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510913"
---
# <a name="nddesettrustedshare-function"></a>NDdeSetTrustedShare 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

在目前使用者的內容中，授與指定的 DDE 共用信任狀態。

## <a name="syntax"></a>語法


```C++
UINT NDdeSetTrustedShare(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ DWORD  dwTrustOptions
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

要修改其 DSDM 的伺服器名稱。

</dd> <dt>

*lpszShareName* \[在\]
</dt> <dd>

要授與受信任狀態的共用名稱。 此參數不可以是 **Null**。

</dd> <dt>

*dwTrustOptions* \[在\]
</dt> <dd>

影響 DDE 共用之受信任狀態的選項。 此參數可以是下列其中一個值。



| 選項                                                                                                                                                                                                                                                      | 意義                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_CMD \_ 顯示 \_ 遮罩**</dt> <dt>0x0000FFFFL</dt> </dl>             | 如果 \_ \_ 已設定 NDDE TRUST CMD show，則用來取得用來覆寫「DDE 共用顯示」狀態之值的遮罩 \_ 。<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_信任 \_ CMD \_ 顯示**</dt> <dt>0x10000000L</dt> </dl>          | 覆寫 [DDE 共用 DSDM] 中指定的顯示狀態。<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_信任 \_ 共用 \_ DEL**</dt> <dt>0x20000000L</dt> </dl>       | 移除共用的受信任狀態。<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_信任 \_ 共用 \_ INIT**</dt> <dt>0x40000000L</dt> </dl>    | 如果應用程式已在使用者的內容中執行，則允許用戶端起始該應用程式。<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_信任 \_ 共用 \_ 開始**</dt> <dt>0x80000000L</dt> </dl> | 允許在使用者的內容中啟動應用程式。<br/>                                                 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。

如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。

## <a name="remarks"></a>備註

必須先使用 [**NDdeShareAdd**](nddeshareadd.md)建立 DDE 共用。

如果呼叫 **NDdeSetTrustedShare** 時， *dwTrustOptions* 設定為零，則受信任的共用會失去其受信任的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeSetTrustedShareW** (Unicode) 和 **NDdeSetTrustedShareA** (ANSI) <br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




