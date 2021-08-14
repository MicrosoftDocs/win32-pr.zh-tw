---
title: 'WINBIO_OPERATION_TYPE 常數 (Winbio \_ 類型 .h) '
description: 指定要執行的非同步操作類型。
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39dd6e2656ad73623df9d6a92d514e90371bc3761563e5f24c41211680c2455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909947"
---
# <a name="winbio_operation_type-constants"></a>WINBIO \_ 運算 \_ 類型常數

[**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)中的 Windows 生物特徵辨識架構可以傳回下列常數，以指定要執行的非同步操作類型。

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**WINBIO \_ 操作 \_ 無**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



未識別任何作業。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO \_ 操作 \_ 開啟**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



生物識別會話已開啟。 如需詳細資訊，請參閱 [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO \_ 作業 \_ 關閉**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



生物識別會話已關閉。 如需詳細資訊，請參閱 [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO \_ 操作 \_ 驗證**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



已根據使用者身分識別來驗證生物識別範例。 如需詳細資訊，請參閱 [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO \_ 操作 \_ 識別**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



已捕獲並與現有範本比較的生物識別範例。 如需詳細資訊，請參閱 [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO \_ 操作 \_ 找出 \_ 感應器**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



已抓取生物特徵辨識單位的識別碼。 如需詳細資訊，請參閱 [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO \_ 操作 \_ 註冊 \_ 開始**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



已起始生物識別註冊順序。 如需詳細資訊，請參閱 [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO \_ OPERATION \_ 註冊 \_ 捕獲**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



已捕捉並將生物識別範例新增至範本。 如需詳細資訊，請參閱 [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO \_ 作業 \_ 註冊 \_ 認可**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



擱置的生物特徵辨識範本已完成。 如需詳細資訊，請參閱 [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**WINBIO \_ OPERATION \_ 註冊 \_ 捨棄**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



擱置的生物特徵辨識範本已捨棄。 如需詳細資訊，請參閱 [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**WINBIO \_ 作業 \_ 列舉 \_ 註冊**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



指定之範本的子因數已列舉。 如需詳細資訊，請參閱 [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO \_ 操作 \_ 刪除 \_ 範本**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



已從存放區刪除生物識別範本。 如需詳細資訊，請參閱 [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**WINBIO \_ OPERATION \_ CAPTURE \_ 範例**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



已捕捉到生物識別範例。 如需詳細資訊，請參閱 [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO \_ 操作 \_ 取得 \_ 屬性**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



已抓取生物識別會話、單位或範本屬性。 如需詳細資訊，請參閱 [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO \_ OPERATION \_ SET \_ 屬性**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



已設定生物識別會話、單位、範本或帳戶屬性。 如需詳細資訊，請參閱 [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO \_ 操作 \_ 取得 \_ 事件**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



未使用。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO \_ 操作 \_ 鎖定 \_ 單位**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



已鎖定可供會話獨佔使用的生物識別單位。 如需詳細資訊，請參閱 [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO \_ OPERATION \_ UNLOCK \_ UNIT**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



已釋放生物特徵辨識裝置上的會話鎖定。 如需詳細資訊，請參閱 [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**WINBIO \_ 操作 \_ 控制 \_ 單位**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



廠商定義的作業是在控制單位上執行。 如需詳細資訊，請參閱 [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**WINBIO \_ 操作 \_ 控制 \_ 單位 \_ 許可權**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



具有特殊許可權的廠商定義作業是在控制單位上執行。 如需詳細資訊，請參閱 [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO \_ OPERATION \_ OPEN \_ FRAMEWORK**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



已開啟生物特徵辨識架構的控制碼。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO \_ OPERATION \_ CLOSE \_ FRAMEWORK**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



生物識別架構的控制碼已關閉。 如需詳細資訊，請參閱 [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**WINBIO \_ 作業 \_ 列舉 \_ 服務 \_ 供應商**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



已列舉已安裝的生物識別服務提供者。 如需詳細資訊，請參閱 [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO \_ 作業 \_ 列舉 \_ 生物特徵辨識 \_ 單位**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



已列舉附加的生物特徵辨識單位。 如需詳細資訊，請參閱 [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**WINBIO \_ 作業 \_ 列舉 \_ 資料庫**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



已列舉註冊的資料庫。 如需詳細資訊，請參閱 [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO \_ 操作 \_ 單位 \_ 抵達**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



已建立生物特徵辨識單位。 如需詳細資訊，請參閱 [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**WINBIO \_ 操作 \_ 單位 \_ 移除**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



已刪除生物識別單位。 如需詳細資訊，請參閱 [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges)。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO \_ 作業 \_ 識別 \_ 和 \_ 發行 \_ 票證**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



保留的。 從 Windows 10 開始支援此值。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO \_ 操作 \_ 驗證 \_ 和 \_ 發行 \_ 票證**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



保留的。 從 Windows 10 開始支援此值。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**WINBIO \_ 作業 \_ 監視器 \_ 狀態**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



已開啟臉部辨識或鳶尾花監視機制。 如需詳細資訊，請參閱 [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)。 從 Windows 10 開始支援此值。


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO \_ 操作 \_ 註冊 \_ SELECT**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



由範例緩衝區中的資料所代表的一組個人的個人，已指定為要註冊的個人。 如需詳細資訊，請參閱 [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect)。 從 Windows 10 開始支援此值。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                                                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





