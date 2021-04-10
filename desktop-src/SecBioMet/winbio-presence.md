---
title: 'WINBIO_PRESENCE 結構 (Winbio \_ 類型 .h) '
description: 包含正在監視的個人是否存在的相關資訊。
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- WINBIO_PRESENCE 結構 Windows 生物特徵辨識架構 API
- PWINBIO_PRESENCE 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a917f09f419ce8dd5eb59c9c277293261bffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103847"
---
# <a name="winbio_presence-structure"></a>WINBIO \_ 狀態結構

包含正在監視的個人是否存在的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_PRESENCE {
  WINBIO_BIOMETRIC_TYPE      Factor;
  WINBIO_BIOMETRIC_SUBTYPE   SubFactor;
  HRESULT                    Status;
  WINBIO_REJECT_DETAIL       RejectDetail;
  WINBIO_IDENTITY            Identity;
  ULONGLONG                  TrackingId;
  WINBIO_PROTECTION_TICKET   Ticket;
  WINBIO_PRESENCE_PROPERTIES Properties;
} WINBIO_PRESENCE, *PWINBIO_PRESENCE;
```



## <a name="members"></a>成員

<dl> <dt>

**因素**
</dt> <dd>

用來監視個人是否存在的生物特徵辨識因素。

</dd> <dt>

**SubFactor**
</dt> <dd>

用於監視個人是否存在之生物特徵辨識因素的生物特徵辨識 subfactor 限定詞。

</dd> <dt>

**狀態**
</dt> <dd>

個人的識別程式狀態。

</dd> <dt>

**RejectDetail**
</dt> <dd>

無法辨識個人的其他相關資訊，包括說明如何更正失敗的意見反應。

</dd> <dt>

**身分識別**
</dt> <dd>

在識別出個人之後，要監視其目前狀態的個人身分識別。

</dd> <dt>

**TrackingId**
</dt> <dd>

介面卡產生的整數，可唯一識別個人。 介面卡指派給特定個人的追蹤識別碼保證會是常數，只要該人停留在相機框架中即可。

</dd> <dt>

**票證**
</dt> <dd>

保留的。 由介面卡設定為0。

</dd> <dt>

**屬性**
</dt> <dd>

關於個人位置的因素特定資訊。

</dd> </dl>

## <a name="remarks"></a>備註

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)函式會建立 **WINBIO \_ 狀態** 結構的陣列，並將此陣列傳送至生物特徵辨識服務。 生物識別服務會使用陣列來更新其在電腦附近的內部模型。

根據這項更新的結果，生物特徵辨識服務可能會為具有作用中狀態監視器的任何用戶端產生 [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)函式的 [**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)結構。 **WINBIO \_ 非同步 \_ 結果。** 結構的作業成員包含 **WINBIO 作業 \_ \_ 監視器 \_ 存在**，以及 **WINBIO \_ 非同步 \_ 結果。MonitorPresence. ChangeType** 成員提供有關個人狀態的其他資訊。

當引擎介面卡與特定追蹤識別碼建立關聯的個人第一次出現在輸入資料流程時，生物特徵辨識服務會產生用戶端 [**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) 結構，其中 **WINBIO \_ 非同步 \_ 結果。MonitorPresence. ChangeType** 成員為 **WINBIO \_ 變更 \_ 類型 \_ 抵達**。 在 WINBIO 非同步結果的任何其他 **WINBIO \_ 非同步 \_ 結果** 結構之前，會將此結構傳送至您的應用程式回呼函數或應用程式訊息佇列 **\_ \_ 。MonitorPresence. PresenceArray** 包含 **WINBIO \_ 狀態** 結構，具有與 WINBIO 存在相同的值 **\_ 。TrackingId**。

WINBIO 非同步結果 **WINBIO \_ 存在** 性結構的陣列中，下列值的 **組合 \_ \_ 。MonitorPresence. PresenceArray** 成員表示某個人狀態的特定變更類型。

-   當個人在相機框架中顯示，但引擎仍在嘗試識別個人時， **WINBIO \_ 狀態** 結構的成員會有下表中的值。

    

    | 成員            | 值                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | 識別引擎個別的整數。 |
    | **狀態**        | **S \_ 確定**                                                |
    | **身分識別。類型** | **WINBIO \_ 識別碼 \_ 類型 \_ Null**                               |

    

     

    在此情況下，生物特徵辨識服務會延長個人的到期時間，而不會針對 WINBIO 非同步結果的追蹤識別碼產生用戶端 [**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) 結構 **\_ \_ 。MonitorPresence. ChangeType** 成員是 **WINBIO \_ 變更 \_ 類型 \_ 辨識**。

    第一次 [**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)結構時，會包含 **狀態** 成員為 **\_ OK** 和 Identity 的 WINBIO 目前狀態結構 **。** 在一或多個 **WINBIO \_ 非同步 \_ 結果** 結構包含 WINBIO 狀態結構且 **狀態** 成員為 **\_** **WINBIO \_ E \_ 錯誤 \_** 的 WINBIO 時，目前狀態監視器會為追蹤識別碼產生一個 WINBIO **\_ 非同步 \_ 結果** 結構，其中 **\_ \_ \_** **\_** **WINBIO \_ 非同步 \_ 結果。MonitorPresence. ChangeType** 成員為 **WINBIO \_ 變更 \_ 類型 \_ 追蹤**。 這會 **WINBIO \_ 非同步 \_ 結果** 結構，其中 **WINBIO \_ 非同步 \_ 結果。MonitorPresence. ChangeType** member 為 **WINBIO \_ 變更 \_ 類型 \_ 追蹤** ，會通知用戶端造成 **WINBIO \_ E \_ 錯誤的 \_ 捕獲** 錯誤的問題已解決。 如需 **WINBIO \_ 狀態** 結構具有 **WINBIO \_ E \_ 錯誤 \_ CAPTURE** 之 **狀態** 成員情況的詳細資訊，請參閱關於引擎介面卡如何提供意見反應給使用者，以在這些備註稍後更正辨識失敗的相關說明。

-   當您在相機框架中看到個人時，但引擎仍在嘗試識別個人，並且想要提供意見反應給使用者，以瞭解如何更正辨識失敗時， **WINBIO \_ 狀態** 結構的成員具有下表中的值。

    

    | 成員                                                                                                      | 值                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | 識別引擎個別的整數。                      |
    | **狀態**                                                                                                  | **WINBIO \_ 電子 \_ 錯誤 \_ 捕捉**                                                   |
    | **身分識別。類型**                                                                                           | **WINBIO \_ 識別碼 \_ 類型 \_ Null**                                                    |
    | **FacialFeatures. BoundingBox**，如果 **因素** 的值是 **WINBIO 型別臉部 \_ \_ \_ 特徵** | 相機框架內個人的臉部位置。           |
    | **鳶尾花. BoundingBox**，如果 **因素** 的值是 **WINBIO \_ 類型 \_ 鳶尾花**                       | 相機框架內的個人鳶尾花或 irises 位置。 |

    

     

    在此情況下，生物特徵辨識服務會擴充個人的到期時間，並針對 WINBIO 非同步結果的追蹤識別碼產生 [**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) 結構 **\_ \_ 。MonitorPresence. ChangeType** 成員為 **WINBIO \_ 變更 \_ 類型 \_ 追蹤**。

-   當個人在相機框架中顯示，且引擎介面卡決定個人的身分識別時， **WINBIO 目前 \_ 狀態** 結構的成員具有下表中的值。

    

    | 成員                        | 值                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | 識別引擎個別的整數。 |
    | **狀態**                    | **S \_ 確定**                                                |
    | **身分識別。類型**             | **WINBIO \_ 識別碼 \_ 類型 \_ SID**                                |
    | **AccountSid** | 個人 (SID) 的安全識別碼。         |

    

     

    在此情況下，生物特徵辨識服務會將追蹤識別碼與個別的 SID 產生關聯，並且針對 WINBIO 非同步結果的追蹤識別碼產生用戶端 [**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) 結構 **\_ \_ 。MonitorPresence. ChangeType** 成員是 **WINBIO \_ 變更 \_ 類型 \_ 辨識**。 生物特徵辨識服務不會針對追蹤識別碼產生額外的用戶端 **WINBIO \_ 非同步 \_ 結果** 結構，除非該人離開相機框架。

-   當您在相機框架中看到個人時，但引擎介面卡判斷個人未註冊時， **WINBIO 目前 \_ 狀態** 結構的成員具有下表中的值。

    

    | 成員            | 值                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | 識別引擎個別的整數。 |
    | **狀態**        | **WINBIO \_ E \_ 未知 \_ 識別碼**                               |
    | **身分識別。類型** | **WINBIO \_ 識別碼 \_ 類型 \_ Null**                               |

    

     

    在此情況下，生物特徵辨識服務會將個人的追蹤識別碼與未知的身分識別產生關聯，並且針對 WINBIO 非同步結果的追蹤識別碼產生用戶端 [**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) 結構 **\_ \_ 。MonitorPresence. ChangeType** 成員是 **WINBIO \_ 變更 \_ 類型 \_ 辨識**。 生物特徵辨識服務不會針對追蹤識別碼產生額外的用戶端 **WINBIO \_ 非同步 \_ 結果** 結構，除非該人離開相機框架。

當引擎介面卡與特定追蹤識別碼相關聯的個體離開相機框架，而停止出現在 [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) 函式所傳回的值中時，追蹤識別碼最後會過期。 當追蹤識別碼到期時，生物特徵辨識服務會產生用戶端 [**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) 結構，其中 **WINBIO \_ 非同步 \_ 結果。MonitorPresence. ChangeType** 成員為 **WINBIO \_ 變更 \_ 類型 \_**。 引擎介面卡可防止生物識別服務使用 **WINBIO \_ 變更 \_ 類型 \_** 的值產生此結構，方法是在 **EngineAdapterIdentifyAll** 傳回的陣列中包含 **WINBIO \_ 存在** 性結構，其中 **WINBIO \_ 存在。狀態** 成員是 **\_ [確定]** 和 [ **WINBIO] \_ 狀態。Identity。類型** 成員是 **WINBIO \_ 識別碼 \_ 類型為 \_ Null** ，如稍早在這些備註中所述。 此動作會延長追蹤識別碼的到期時間，而不會造成任何用戶端活動。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 





