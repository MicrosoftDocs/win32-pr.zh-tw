---
description: 連線方法會使用指定的網路介面卡，將 NPP 連接到網路，並提供連線的設定資訊。
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'IDelaydC：：連線方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e91db1dae0c67c5f35e46841867d3d3e15058cf0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477301"
---
# <a name="idelaydcconnect-method"></a>IDelaydC：：連線方法

**連線** 方法會使用指定的網路介面卡，將 NPP 連接到網路，並提供連線的設定資訊。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hInputBlob* \[在\]
</dt> <dd>

BLOB 的控制碼，指定您要連接的 NIC 以及該連接的設定資訊。

</dd> <dt>

*StatusCallbackProc* \[在\]
</dt> <dd>

使用者回呼函式的位址，用來接收狀態更新（例如觸發程式）。 如果未使用回呼函式，請將此參數和 *UserCoNtext* 參數設定為 **Null**。

</dd> <dt>

*UserCoNtext* \[在\]
</dt> <dd>

呼叫使用者的回呼函數時傳遞的值。 這個參數的值通常是 HWND 或 ' this ' 指標。 如果未指定回呼函數，請將此參數和 *StatusCallbackProc* 參數設定為 **Null**。

</dd> <dt>

*hErrorBlob* \[擴展\]
</dt> <dd>

錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值會是下列其中一個錯誤碼 (其中包含內部 **IDelaydC：： Configure** 呼叫) 所傳回的錯誤：




| 傳回碼 | Description | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | NPP COM 物件的這個實例已連線到網路。<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | 設定 BLOB 已損毀。 此錯誤是由 <strong>IDelaydC：： Configure</strong> 呼叫所產生。<br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | <em>HInputBlob</em>所指定的輸入 BLOB 缺少執行這項作業所需的專案。 此錯誤可能是由<strong>IDelaydC：：連線</strong>或<strong>IDelaydC：： Configure</strong>呼叫所產生。 查看 <em>hErrorBlob</em> 傳回的錯誤 BLOB，以判斷找不到哪個專案。<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | 尚未呼叫 <strong>CreateBlob</strong> 函數。 此錯誤是由 <strong>IDelaydC：： Configure</strong> 呼叫所產生。<br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | 字串不是以 null 結束。 此錯誤是由 <strong>IDelaydC：： Configure</strong> 呼叫所產生。<br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | 輸入 BLOB 的觸發程式部分已損毀。 此錯誤是由 <strong>IDelaydC：： Configure</strong> 呼叫所產生。<br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | <em>HInputBlob</em>中指定的物件不是 BLOB。 此錯誤是由 <strong>IDelaydC：： Configure</strong> 呼叫所產生。<br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | 未在登錄中設定預設的 capture 目錄。 使用下列路徑來設定 capture 目錄。 <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | 沒有可執行此作業的記憶體。 此錯誤是由 <strong>IDelaydC：： Configure</strong> 呼叫所產生。<br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | 要求已超時。此錯誤是由 <strong>IDelaydC：： Configure</strong> 呼叫所產生。<br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | <em>HInputBlob</em>中指定的 BLOB 版本號碼不正確。 此錯誤是由 <strong>IDelaydC：： Configure</strong> 呼叫所產生。<br /> | 




 

## <a name="remarks"></a>備註

呼叫 **連線** 方法時，NPP 會使用 *hInputBlob* 所提供的 BLOB，自動呼叫 **IDelaydC：： Configure** 。 請注意， **IDelaydC：： Configure** 的呼叫所傳回的任何錯誤碼都會回傳，並由 **IDelaydC：：連線** 呼叫傳回。

您必須先呼叫這個方法，才能開始捕獲框架。 請注意，當您使用此方法連接到網路時，您必須繼續使用 **IDelaydC** 介面方法來捕捉畫面格。

您可以藉由呼叫 **GetNPPBlobFromUI**、 **GetNPPBlobTable** 和 **SelectNPPBlobFromTable** 來取得 *hInputBlob* 參數所指定的輸入 BLOB。

*HErrorBlob* 中傳回的錯誤 BLOB 包含開發人員或應用程式可用於進行疑難排解的錯誤資訊。 *HErrorBlob* 所傳回的錯誤 BLOB 包含網路監視器無法在 *hInputBlob* 中指定的輸入 BLOB 中瞭解或尋找的專案。 例如，如果傳回 NMERR \_ BLOB \_ 專案不存在，則會在 \_ \_ \_ 傳回的錯誤 BLOB 中包含網路監視器找不到的專案。



| 如需下列資訊                          | 請參閱                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| 取得代表 NIC 的輸入 BLOB | [選取網路介面卡](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC：： Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC：:D isconnect](idelaydc-disconnect.md)
</dt> <dt>

[IDelaydC：： Start](idelaydc-start.md)
</dt> </dl>

 

 




