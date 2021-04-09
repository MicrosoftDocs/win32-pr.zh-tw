---
title: 'WINBIO_BIR_PURPOSE 常數 (Winbio \_ 類型 .h) '
description: 指定 (BIR) 預定或適用的生物特徵辨識資訊記錄用途。
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934432"
---
# <a name="winbio_bir_purpose-constants"></a>WINBIO \_ BIR \_ 用途常數

[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)結構的 **目的** 成員會使用下列旗標，來指定要將生物特徵辨識資訊記錄 (BIR) 預定或適用的用途。



| 常數                                                                                                                                                                                                                                          | 描述                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**WINBIO \_ 沒有 \_ 任何 \_ 可用的用途**</dt> </dl>                                         | 未指定任何用途。<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**WINBIO \_ 用途 \_ 驗證**</dt> </dl>                                                            | 驗證使用者的身分識別。<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**WINBIO \_ 目的 \_ 識別**</dt> </dl>                                                      | 識別使用者。<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**WINBIO \_ 目的 \_ 註冊**</dt> </dl>                                                            | 註冊使用者。<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**WINBIO \_ 目的 \_ 註冊 \_ 以進行 \_ 驗證**</dt> </dl>       | 捕捉生物特徵辨識範例，並判斷範例是否對應到指定的使用者身分識別。<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**WINBIO \_ 目的 \_ 註冊 \_ 以供 \_ 識別**</dt> </dl> | 捕捉生物特徵辨識範例，並判斷它是否符合現有的生物特徵辨識範本。<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**WINBIO \_ 目的 \_ 審核**</dt> </dl>                                                               | 可以用來記錄或顯示的額外資訊。 所有函數的輸入都會忽略此值。 在輸出中，它只有在可辨識設備支援的情況下才可使用，而且您會在 [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)函數的 *Flags* 參數中指定 **\_ RAW WINBIO 資料 \_ 旗 \_** 標。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> <dt>

[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)
</dt> </dl>

 

 





