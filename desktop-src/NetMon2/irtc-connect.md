---
description: IRTC：： Connect 方法-Connect 方法會使用指定的 NIC 將 NPP 連接到網路，並提供連線的設定資訊。
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'IRTC：： Connect 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110742"
---
# <a name="irtcconnect-method"></a>IRTC：： Connect 方法

**Connect** 方法會使用指定的 NIC 將 NPP 連接到網路，並提供連線的設定資訊。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
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

使用者狀態回呼函式的位址，此函式會接收狀態更新（例如觸發程式）。 這個參數可以設定為 **Null**。

</dd> <dt>

*FramesCallbackProc* \[在\]
</dt> <dd>

使用者的框架回呼函式位址，用來接收狀態更新（例如觸發程式）。 這個參數可以設定為 **Null**。

</dd> <dt>

*UserCoNtext* \[在\]
</dt> <dd>

呼叫使用者的狀態和框架回呼函數時傳遞的值。 如果同時指定兩個回呼函數，則必須使用相同的使用者內容值。 這個參數的值通常是 HWND 或 ' this ' 指標。

</dd> <dt>

*hErrorBlob* \[擴展\]
</dt> <dd>

錯誤 BLOB 的控制碼，其中包含其他錯誤資訊。 請參閱本主題底部的備註，以取得錯誤 BLOB 的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值會是下列其中一個錯誤碼 (其中包含內部 **IRTC：： Configure** 呼叫) 所傳回的錯誤：



| 傳回碼                                                                                                         | Description                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 已 \_ 連線**</dt> </dl>            | NPP COM 物件的這個實例已連線到網路。<br/>                                                                                                                                                                                                          |
| <dl> <dt>**NMERR \_ BLOB \_ 轉換 \_ 錯誤**</dt> </dl>       | 設定 BLOB 已損毀。 此錯誤是由 **IRTC：： Configure** 呼叫所產生。<br/>                                                                                                                                                                                       |
| <dl> <dt>**NMERR \_ BLOB \_ 專案 \_ 不 \_ \_ 存在**</dt> </dl> | *HInputBlob* 參數所指定的輸入 BLOB 缺少執行這項作業所需的專案。 此錯誤可能是由 **IRTC：： Connect** 或 **IRTC：： Configure** 呼叫所產生。 查看 *hErrorBlob* 傳回的錯誤 BLOB，以判斷找不到哪個專案。<br/> |
| <dl> <dt>**NMERR \_ BLOB \_ 未 \_ 初始化**</dt> </dl>        | 尚未呼叫 **CreateBlob** 函數。 此錯誤是由 **IRTC：： Configure** 呼叫所產生。<br/>                                                                                                                                                                         |
| <dl> <dt>**NMERR \_ BLOB \_ 字串 \_ 無效**</dt> </dl>         | 字串不是以 null 結束。 此錯誤是由 **IRTC：： Configure** 呼叫所產生。<br/>                                                                                                                                                                                       |
| <dl> <dt>**NMERR 不 \_ 合法的 \_ 觸發程式**</dt> </dl>              | 輸入 BLOB 的觸發程式部分已損毀。 此錯誤是由 **IRTC：： Configure** 呼叫所產生。<br/>                                                                                                                                                                        |
| <dl> <dt>**NMERR \_ 不正確 \_ BLOB**</dt> </dl>                 | *HInputBlob* 中指定的物件不是 BLOB。 此錯誤是由 **IRTC：： Configure** 呼叫所產生。<br/>                                                                                                                                                                      |
| <dl> <dt>**NMERR \_ \_ 記憶體不足 \_**</dt> </dl>               | 執行這項作業所需的記憶體無法使用。 此錯誤是由 **IRTC：： Configure** 呼叫所產生。<br/>                                                                                                                                                              |
| <dl> <dt>**NMERR \_ TIMEOUT**</dt> </dl>                       | 要求已超時。此錯誤是由 **IRTC：： Configure** 呼叫所產生。<br/>                                                                                                                                                                                               |
| <dl> <dt>**NMERR \_ 上層 \_ BLOB**</dt> </dl>                 | *HInputBlob* 中指定的 BLOB 版本號碼不正確。 此錯誤是由 **IRTC：： Configure** 呼叫所產生。<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>備註

呼叫 **Connect** 方法時，NPP 會使用 *hInputBlob* 所提供的 BLOB，自動呼叫 **IRTC：： Configure** 方法。 請注意， **IRTC：： Configure** 的呼叫所傳回的任何錯誤碼都會回傳，並由 **IRTC：： Connect** 呼叫傳回。

您必須先呼叫這個方法，才能開始捕獲框架。 請注意，當您使用這個方法連接到網路時，您必須繼續使用 **IRTC** 介面來捕捉畫面格。

呼叫此函式時，您必須指定狀態或框架回呼函式，即使它只作為預留位置。

*HInputBlob* 指定的輸入 BLOB 可以藉由呼叫 **GetNPPBlobFromUI**、 **GetNPPBlobTable** 和 **SelectNPPBlobFromTable** 方法來取得。

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

[IRTC](irtc.md)
</dt> <dt>

[IRTC：： Configure](irtc-configure.md)
</dt> <dt>

[IRTC：:D isconnect](irtc-disconnect.md)
</dt> <dt>

[IRTC：： Start](irtc-start.md)
</dt> </dl>

 

 




