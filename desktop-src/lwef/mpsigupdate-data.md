---
title: 'MPSIGUPDATE_DATA 結構 (MpClient .h) '
description: 傳遞至簽章更新回呼函數的通知資料。
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA 結構舊版 Windows 環境功能
- PMPSIGUPDATE_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104538"
---
# <a name="mpsigupdate_data-structure"></a>MPSIGUPDATE \_ 資料結構

傳遞至簽章更新回呼函數的通知資料。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**dwPercentComplete**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

在所有已下載及/或已安裝的更新中，估計百分比。

</dd> <dt>

**dwTotalUpdates**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

要下載及/或安裝的更新總數。

</dd> <dt>

**dwCurrentUpdateIndex**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

以零為基底的索引值，指定目前正在下載及/或安裝所需的更新。

</dd> <dt>

**eType**
</dt> <dd>

類型： **MPSIGUPDATE \_ 類型**

</dd> <dd>

更新類型。 下列其中一個可能值：



| 值                                                                                                                                                                                                                             | 意義                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**MPSIGUPDATE \_ 類型 \_ 無**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**MPSIGUPDATE \_ 類型 \_ 受控**</dt> </dl>                                   | WSUS 更新。 Cancel 需要系統管理員許可權。<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**MPSIGUPDATE \_ 類型 \_ HTTP**</dt> </dl>                                            | HTTP 更新。 不需要取消的系統管理員許可權。<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**MPSIGUPDATE \_ 類型 \_ HTTP \_ SRV**</dt> </dl>                               | 來自服務的 HTTP。 Cancel 需要系統管理員許可權。<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**MPSIGUPDATE \_ 類型 \_ UNC**</dt> </dl>                                               | UNC 共用。 不需要取消的系統管理員許可權。<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**MPSIGUPDATE \_ 類型 \_ 非受控**</dt> </dl>                             | MU/WU 更新。 Cancel 需要系統管理員許可權。<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**MPSIGUPDATE \_ 類型 \_ 受控 \_ 平臺**</dt> </dl>       | 適用于平臺的 WSUS 更新。 Cancel 需要系統管理員許可權。<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**MPSIGUPDATE \_ 型別 \_ 非受控 \_ 平臺**</dt> </dl> | 適用于平臺的 MU/WU 更新。 Cancel 需要系統管理員許可權。<br/> |



 

</dd> <dt>

**階段**
</dt> <dd>

類型： **MP \_ 更新 \_ 階段**

</dd> <dd>

更新階段。 下列其中一個可能值：



| 值                                                                                                                                                                         | 意義                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**MP \_ 階段 \_ 不明**</dt> </dl>       | 更新階段未知。<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**MP \_ 搜尋 \_ 更新**</dt> </dl>       | 更新搜尋階段。<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**MP \_ 下載 \_ 更新**</dt> </dl> | 更新下載階段。<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**MP \_ 安裝 \_ 更新**</dt> </dl>    | 更新安裝階段。<br/>  |



 

</dd> <dt>

**路徑**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

更新路徑。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





