---
description: 設定平板電腦內容的共用記憶體通訊。
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: ITabletCoNtextP：： UseNamedSharedMemoryCommunications 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985462"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a>ITabletCoNtextP：： UseNamedSharedMemoryCommunications 方法

設定平板電腦內容的共用記憶體通訊。

## <a name="syntax"></a>語法


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pid* \[在\]
</dt> <dd>

存取共用記憶體之用戶端的處理序識別碼。

</dd> <dt>

*pszCallerSid* \[在\]
</dt> <dd>

函數呼叫端的安全識別碼。

</dd> <dt>

*pszCallerIntegritySid* \[在\]
</dt> <dd>

可以驗證呼叫函數完整性的安全識別碼。

</dd> <dt>

*pdwEventMoreDataId* \[擴展\]
</dt> <dd>

用來建立事件名稱的整數。 此事件表示是否有更多資料。

</dd> <dt>

*pdwEventClientReadyId* \[擴展\]
</dt> <dd>

用來建立事件名稱的整數。 此事件表示用戶端已準備好接收資料。 此事件會在處理新資料之後收到信號。

</dd> <dt>

*pdwMutexAccessId* \[擴展\]
</dt> <dd>

共用記憶體的存取識別碼指標。

</dd> <dt>

*pdwFileMappingId* \[擴展\]
</dt> <dd>

識別共用記憶體的整數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

**UseNamedSharedMemoryCommunications** 方法是 Tablet PC 共用記憶體通訊協定的一部分。 沒有較高許可權的用戶端會在安全識別碼中傳遞 (SID) 和完整性層級安全識別碼 (IL SID) ，讓平板電腦服務可以使用 (ACL) 的存取控制清單來存取共用記憶體物件。 如果用戶端有更高的許可權，則應該使用 UseSharedMemoryCommunications，也就是當服務已經有更高的許可權時，所呼叫的 API。

[**SHAREDMEMORY \_ 標頭**](sharedmemory-header.md)結構會儲存共用記憶體標頭。

[**SHAREDMEMORY \_ 標頭**](sharedmemory-header.md)結構是從檔案對應所參考的資料進行轉換。 原始的封包資料會遵循 **SHAREDMEMORY \_ 標頭**。 當引發 *pdwEventClientReadyId* 所參考的事件時，可以從共用記憶體讀取原始的封包資料。

下列清單描述用來存取和使用共用記憶體的事件順序。

1.  用戶端會引發 clientReady 事件。
2.  用戶端會等候 moreData 事件。
3.  用戶端會取得 mutex。
4.  用戶端會從標頭後面的共用記憶體區段讀取封包資料。 序號會顯示在封包資料之後的共用記憶體中。
5.  用戶端會根據 **dwEvent** 的值來處理資料。
6.  用戶端寫入-1 (0xFFFFFFFF) **dwEvent**。
7.  用戶端釋放 mutex。
8.  用戶端會引發 clientReady 事件。

事件名稱的建立方式是將此方法的輸出格式化。 下列定義可以搭配 sprintf 使用，或其對等專案來建立事件名稱。


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



在每個定義中，% d 區段會取代為處理序識別碼，而% u 區段會取代為 *pdwEventMoreDataId* 或 *pdwEventClientReadyId* 中傳回的整數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[**ITabletCoNtextP**](itabletcontextp.md)
</dt> </dl>

 

 




