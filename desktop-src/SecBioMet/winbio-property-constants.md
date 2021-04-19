---
title: 'WINBIO_PROPERTY 常數 (Winbio \_ 類型 .h) '
description: 指定要在 WinBioGetProperty 函式中查詢或在 WinBioSetProperty 函數中變更的屬性。
ms.assetid: 4F595ADB-18B7-442A-8CED-595E7823F37D
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_SAMPLE_HINT
- WINBIO_PROPERTY_EXTENDED_SENSOR_INFO
- WINBIO_PROPERTY_EXTENDED_ENGINE_INFO
- WINBIO_PROPERTY_EXTENDED_STORAGE_INFO
- WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS
- WINBIO_PROPERTY_ANTI_SPOOF_POLICY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b3c0ce75b2f26105dc356a7b5dcde27f562fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967768"
---
# <a name="winbio_property-constants"></a>WINBIO \_ 屬性常數

下列常數是 **WINBIO \_ 屬性 \_ 識別碼** 值，可用來指定要在 [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)函數的 *PropertyId* 參數中查詢的屬性。 某些屬性也可以使用 [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty) 函式中的相同參數來設定。 查詢的結果會在這些函式的 *PropertyBuffer* 參數中傳回或指定，而結果的類型和大小會隨著查詢的屬性而不同。



| 常數/值                                                                                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PROPERTY_SAMPLE_HINT"></span><span id="winbio_property_sample_hint"></span><dl> <dt>**WINBIO \_屬性 \_ 範例 \_ 提示**</dt> <dt>1</dt> </dl>                                               | 這個唯讀生物特徵辨識屬性會估計完成註冊範本所需的良好生物識別範例最大數目。 屬性查詢的結果會以包含提示的 **ULONG** 值傳回。<br/> 當查詢這個屬性時，傳遞的 *SessionHandle* 和 *UnitId* 參數必須是有效的、 *Identity* 參數必須是 **Null**，且 *SubFactor* 參數必須是 **WINBIO \_ 子類型 \_ NO \_ 資訊**。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="WINBIO_PROPERTY_EXTENDED_SENSOR_INFO"></span><span id="winbio_property_extended_sensor_info"></span><dl> <dt>**WINBIO \_屬性 \_ 擴充 \_ 感應器 \_ 資訊**</dt> <dt>2</dt> </dl>                   | 這個唯讀生物特徵辨識屬性包含有關連線到特定生物特徵辨識單位之感應器元件的功能和屬性的延伸資訊。 屬性查詢的結果會以 [**WINBIO \_ 擴充 \_ 感應器 \_ 資訊**](winbio-extended-sensor-info.md) 結構的形式傳回。<br/> 當查詢這個屬性時，傳遞的 *SessionHandle* 和 *UnitId* 參數必須是有效的、 *Identity* 參數必須是 **Null**，且 *SubFactor* 參數必須是 **WINBIO \_ 子類型 \_ NO \_ 資訊**。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="WINBIO_PROPERTY_EXTENDED_ENGINE_INFO"></span><span id="winbio_property_extended_engine_info"></span><dl> <dt>**WINBIO \_屬性 \_ 擴充 \_ 引擎 \_ 資訊**</dt> <dt>3</dt> </dl>                   | 這個唯讀生物特徵辨識屬性包含有關連接到特定生物特徵辨識單位之引擎元件的功能和屬性的延伸資訊。 屬性查詢的結果會以 [**WINBIO \_ 延伸 \_ 引擎 \_ 資訊**](winbio-extended-engine-info.md) 結構的形式傳回。<br/> 當查詢這個屬性時，傳遞的 *SessionHandle* 和 *UnitId* 參數必須是有效的、 *Identity* 參數必須是 **Null**，且 *SubFactor* 參數必須是 **WINBIO \_ 子類型 \_ NO \_ 資訊**。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="WINBIO_PROPERTY_EXTENDED_STORAGE_INFO"></span><span id="winbio_property_extended_storage_info"></span><dl> <dt>**WINBIO \_屬性 \_ 擴充 \_ 存放裝置 \_ 資訊**</dt> <dt>4</dt> </dl>                | 這個唯讀生物特徵辨識屬性包含連接到特定生物識別單位之儲存體元件的功能和屬性的擴充資訊。 屬性查詢的結果會以 [**WINBIO \_ 延伸 \_ 儲存體 \_ 資訊**](winbio-extended-storage-info.md) 結構的形式傳回。<br/> 當查詢這個屬性時，傳遞的 *SessionHandle* 和 *UnitId* 參數必須是有效的、 *Identity* 參數必須是 **Null**，且 *SubFactor* 參數必須是 **WINBIO \_ 子類型 \_ NO \_ 資訊**。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS"></span><span id="winbio_property_extended_enrollment_status"></span><dl> <dt>**WINBIO \_屬性 \_ 延伸 \_ 註冊 \_ 狀態**</dt> <dt>5</dt> </dl> | 這個唯讀生物特徵辨識屬性包含特定生物特徵辨識單位上進行中註冊狀態的延伸資訊。 屬性查詢的結果會以 [**WINBIO \_ 延伸 \_ 儲存體 \_ 資訊**](winbio-extended-storage-info.md) 結構的形式傳回。 如果 BU 沒有進行中的註冊，傳回結構的 **templatestatus.archived** 成員就會有 **WINBIO \_ E \_ 無效 \_** 作業的值。<br/> 當查詢這個屬性時，傳遞的 *SessionHandle* 和 *UnitId* 參數必須是有效的、 *Identity* 參數必須是 **Null**，且 *SubFactor* 參數必須是 **WINBIO \_ 子類型 \_ NO \_ 資訊**。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PROPERTY_ANTI_SPOOF_POLICY"></span><span id="winbio_property_anti_spoof_policy"></span><dl> <dt>**WINBIO \_屬性 \_ 反 \_ 詐騙 \_ 原則**</dt> <dt>1</dt> </dl>                            | 此讀寫生物特徵辨識屬性包含特定使用者帳戶的 lnk-antispoofing 原則值。 屬性作業會以 [**WINBIO 的 \_ 反詐騙 \_ \_ 原則**](winbio-anti-spoof-policy.md) 結構來指定或傳回。<br/> 當查詢這個屬性時，傳遞的 *SessionHandle* 參數必須是有效的、 *UnitId* 參數必須是零、 *Identity* 參數必須是帳戶安全識別碼 (SID) 值，才能進行查詢或變更 (若要使用與 *SessionHandle* 相關聯的 sid 值，請指定 **Null**) ，而且 *SubFactor* 參數必須 **WINBIO \_ 子類型 \_ NO \_ 資訊**。<br/> 如果使用萬用字元識別來查詢這個屬性，則會傳回此原則的系統預設值。 未具許可權使用者只能修改自己的原則設定。 如果未具許可權使用者嘗試使用代表其他使用者帳戶的身分 *識別* 參數來呼叫 [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)函式，或包含萬用字元識別碼值，則屬性寫入嘗試將會失敗。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



 

 





