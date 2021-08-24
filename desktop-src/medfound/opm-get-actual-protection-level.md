---
description: 傳回所指定保護機制的全域保護層級。
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: 'OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5d895c037fedfa97bbafab8331d685af9a7f1ce81489b8d600bd903aa2a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101917"
---
# <a name="opm_get_actual_protection_level"></a>OPM \_ 取得 \_ 實際的 \_ 保護 \_ 層級

傳回所指定保護機制的全域保護層級。



| 需求 | 值 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ 實際的 \_ 保護 \_ 層級                                                                                                                                       |
| 輸入資料   | 要查詢的保護機制，指定為32位整數。 此值會被解釋為 [OPM 保護類型旗標](opm-protection-type-flags.md)的成員。 |
| 傳回資料  | [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構                                                                                               |



 

## <a name="remarks"></a>備註

全域保護層級是目前正在連接器上套用的保護層級，而不管圖形驅動程式如何指示套用保護。 例如，應用程式可以藉由呼叫 **ChangeDisplaySettingsEx** 函數來設定 ACP 保護層級。 在此情況下，全域保護層級會反映這項設定，即使未透過輸出保護管理員要求 (OPM) 也一樣。

保護層級會在 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員中傳回。 此值的意義取決於所查詢的保護機制。 針對每個保護機制， **ulInformation** 的值是來自不同列舉的旗標，如下表所示。



| 保護機制 | 列舉型別                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**OPM \_ ACP \_ 保護 \_ 等級**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [CGMS-保護旗標](cgms-a-protection-flags.md)            |
| DPCP                 | [**OPM \_ DPCP \_ 保護 \_ 等級**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| 觀看                 | [**OPM \_ HDCP \_ 保護 \_ 等級**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryGlobalProtectionLevel 查詢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> </dl>

 

 




