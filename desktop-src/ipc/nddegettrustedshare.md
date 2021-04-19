---
description: 抓取受信任共用的伺服器使用者清單中，與 DDE 共用相關聯的選項。
ms.assetid: e5f2b4f8-f922-4734-9fe3-8a74a7f5f619
title: 'NDdeGetTrustedShare 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetTrustedShare
- NDdeGetTrustedShareA
- NDdeGetTrustedShareW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 1f8d7e79c48e0409d8040f6d44159c473dd58ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973001"
---
# <a name="nddegettrustedshare-function"></a>NDdeGetTrustedShare 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

抓取與在伺服器使用者的受信任共用清單中之 DDE 共用相關聯的選項。

## <a name="syntax"></a>語法


```C++
UINT NDdeGetTrustedShare(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _Out_ LPDWORD lpdwTrustOptions,
  _Out_ LPDWORD lpdwShareModId0,
  _Out_ LPDWORD lpdwShareModId1
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

DSDM 所在的伺服器名稱。

</dd> <dt>

*lpszShareName* \[在\]
</dt> <dd>

要查詢其信任狀態的共用名稱。 此參數不可以是 **Null**。

</dd> <dt>

*lpdwTrustOptions* \[擴展\]
</dt> <dd>

接收信任選項之變數的指標。 此參數不可以是 **Null**。 有下列信任選項可供使用。



| 值                                                                                                                                                                                                                                                       | 意義                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="NDDE_CMD_SHOW_MASK"></span><span id="ndde_cmd_show_mask"></span><dl> <dt>**NDDE \_CMD \_ 顯示 \_ 遮罩**</dt> <dt>0x0000FFFFL</dt> </dl>             | 如果 \_ \_ 已設定 NDDE TRUST CMD show，則用來取得用來覆寫「DDE 共用顯示」狀態之值的遮罩 \_ 。<br/> |
| <span id="NDDE_TRUST_CMD_SHOW"></span><span id="ndde_trust_cmd_show"></span><dl> <dt>**NDDE \_信任 \_ CMD \_ 顯示**</dt> <dt>0x10000000L</dt> </dl>          | 覆寫 [DDE 共用 DSDM] 中指定的顯示狀態。<br/>                                                   |
| <span id="NDDE_TRUST_SHARE_DEL"></span><span id="ndde_trust_share_del"></span><dl> <dt>**NDDE \_信任 \_ 共用 \_ DEL**</dt> <dt>0x20000000L</dt> </dl>       | 移除共用的受信任狀態。<br/>                                                                         |
| <span id="NDDE_TRUST_SHARE_INIT"></span><span id="ndde_trust_share_init"></span><dl> <dt>**NDDE \_信任 \_ 共用 \_ INIT**</dt> <dt>0x40000000L</dt> </dl>    | 如果應用程式已在使用者的內容中執行，則允許用戶端起始該應用程式。<br/>              |
| <span id="NDDE_TRUST_SHARE_START"></span><span id="ndde_trust_share_start"></span><dl> <dt>**NDDE \_信任 \_ 共用 \_ 開始**</dt> <dt>0x80000000L</dt> </dl> | 允許在使用者的內容中啟動應用程式。<br/>                                                 |



 

</dd> <dt>

*lpdwShareModId0* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收受信任共用修改識別碼的第一個部分。 此參數不可以是 **Null**。

</dd> <dt>

*lpdwShareModId1* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收受信任共用修改識別碼的第二個部分。 此參數不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。

如果函式失敗，則傳回值會是錯誤碼，您可以藉由呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)將其轉譯為文字錯誤訊息。

## <a name="remarks"></a>備註

受信任的共用修改識別碼會反映 DSDM 中的 DDE 共用在一開始授與信任狀態時的版本。 受信任的共用修改識別碼主要是用來移除淘汰的受信任共用。 不過，使用者不需要移除已淘汰的受信任共用。 網路 DDE 代理程式代表使用者移除已淘汰的共用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeGetTrustedShareW** (Unicode) 和 **NDdeGetTrustedShareA** (ANSI) <br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> <dt>

[**NDdeSetTrustedShare**](nddesettrustedshare.md)
</dt> </dl>

 

 




