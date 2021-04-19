---
description: 提供 tablet 執行緒之間共用記憶體的存取。
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: ITabletCoNtextP：： UseSharedMemoryCommunications 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997210"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a>ITabletCoNtextP：： UseSharedMemoryCommunications 方法

提供 tablet 執行緒之間共用記憶體的存取。

## <a name="syntax"></a>語法


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pid* \[在\]
</dt> <dd>

處理序識別碼。

</dd> <dt>

*phEventMoreData* \[擴展\]
</dt> <dd>

當有新資料可供處理時，發出信號的事件處理常式。

</dd> <dt>

*phEventClientReady* \[擴展\]
</dt> <dd>

傳回的事件控制碼，用來指示用戶端已準備好接收資料。 在處理新資料之後收到信號。

</dd> <dt>

*phMutexAccess* \[擴展\]
</dt> <dd>

Mutex 授與共享記憶體的存取權。

</dd> <dt>

*phFileMapping* \[擴展\]
</dt> <dd>

共用記憶體區塊的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

**UseSharedMemoryCommunications** 方法是用來做為 Tablet PC 共用記憶體通訊協定的一部分。 由於 Wisptis 服務具有 (IL) 的高度完整性層級，因此它可以儲存和存取儲存在共用記憶體中的資料，而不需要提升其許可權。

[**SHAREDMEMORY \_ 標頭**](sharedmemory-header.md)結構會從檔案對應所參考的資料進行轉換，而原始封包資料則會遵循 **SHAREDMEMORY \_ 標頭**。 當引發 *pdwEventClientReady* 所參考的事件時，可以從共用記憶體讀取原始的封包資料。

下列清單描述用來存取和使用共用記憶體的事件順序。

-   用戶端會設定 clientReady 事件。
-   用戶端會等候 moreData 事件。
-   用戶端會取得 mutex。
-   用戶端會從共用記憶體區段的封包資料，讀取封包之後的標頭和序號之後的封包資料。
-   用戶端會根據 **dwEvent** 的值來處理資料。
-   用戶端寫入-1 (0xFFFFFFFF) **dwEvent**。
-   用戶端釋放 mutex。
-   用戶端會設定 clientReady 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletCoNtextP 介面**](itabletcontextp.md)
</dt> <dt>

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




