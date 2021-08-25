---
title: 用戶端應用程式回呼函數
description: 兩種類型的回呼簽章。
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3e052df1821a5fd85bbba4ebbea3e6672d9e625b7d4258110fb19a5c234f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977098"
---
# <a name="client-application-callback-functions"></a>用戶端應用程式回呼函數

Windows 生物特徵辨識架構支援兩種類型的回呼簽章。 從 Windows 8 開始，支援下列回呼。 建議您針對所有新的應用程式執行此回呼。 不過，這項回呼無法在 Windows 7 中使用。



| 回呼                                                                                     | 描述                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PWINBIO \_ 非同步 \_ 完成 \_ 回呼**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | 通知用戶端應用程式，使用 [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) 或 [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) 啟動的非同步作業已完成。<br/> |



 

Windows 7 中引進了下列回呼函數。 我們建議您不要針對以 Windows 8 和更新版本的作業系統為目標的新應用程式執行這些應用程式。



| 回呼                                                                                 | 描述                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**PWINBIO \_ CAPTURE \_ 回呼**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | 傳回非同步 [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) 函數的結果。<br/> |
| [**PWINBIO \_ 註冊 \_ 捕獲 \_ 回呼**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | 傳回非同步 [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) 函數的結果。<br/> |
| [**PWINBIO \_ 事件 \_ 回呼**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | 傳回非同步 [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) 函數的結果。<br/>           |
| [**PWINBIO \_ 識別 \_ 回呼**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | 傳回非同步 [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) 函數的結果。<br/>           |
| [**PWINBIO \_ 找出 \_ 感應器 \_ 回呼**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | 傳回非同步 [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) 函數的結果。<br/>   |
| [**PWINBIO \_ 確認 \_ 回呼**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | 傳回非同步 [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) 函數的結果。<br/>               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端應用程式參考](client-application-reference.md)
</dt> </dl>

 

 





