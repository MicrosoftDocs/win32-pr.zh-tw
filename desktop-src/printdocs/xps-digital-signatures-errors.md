---
description: 下表列出 XPS 數位簽章 API 中的方法可傳回的所有 HRESULT 值。
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: 'XPS 數位簽章 API 錯誤 (Xpsdigitalsignature .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320260"
---
# <a name="xps-digital-signature-api-errors"></a>XPS 數位簽章 API 錯誤

下表列出 XPS 數位簽章 API 中的方法可傳回的所有 **HRESULT** 值。 請注意，並非每個方法都可以傳回下表所列的每個傳回值。



| 傳回碼/值                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ 確定**</dt> </dl>                                                                                                                                                                 | 此方法已成功。<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_E \_ \_ SIGNATUREBLOCK \_ 標記**</dt> <dt>0x8052038b</dt>無效 </dl> | 讀取簽章標記時，簽章區塊的 XML 標記發生錯誤。<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_E \_ 標記 \_ 相容性 \_ 元素**</dt> <dt>0x80520389</dt> </dl> | [**XPS \_ 簽署 \_ 旗標**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags)值指定了不預期的標記相容性元素，但找到標記相容性元素。<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_E \_ 物件卸 \_ 離**</dt> <dt>0x8052038a</dt> </dl>                                            | 介面未與簽章管理員相關聯。<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_E \_ 套件 \_ 已 \_ 開啟**</dt> <dt>0x80520387</dt> </dl>                      | 已在 [簽章管理員] 中開啟 XPS 套件。 <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_E \_ 套件 \_ 未 \_ 開啟**</dt> <dt>0x80520386</dt> </dl>                                  | 尚未在 [簽章管理員] 中開啟 XPS 套件。 <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | 有兩個或多個簽章具有相同的識別碼。<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | 簽章要求識別碼在簽章區塊內不是唯一的。<br/>                                                                                                     |



 

## <a name="remarks"></a>備註

某些 XPS 數位簽章 API 方法會呼叫 [封裝](/previous-versions/windows/desktop/opc/packaging) API。 如需封裝 API 傳回值的相關資訊，請參閱 [封裝錯誤](/previous-versions/windows/desktop/opc/packaging-errors)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                            |
| 標頭<br/>                   | <dl> <dt>Xpsdigitalsignature。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>XpsDigitalSignature .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[COM 中的錯誤處理](../com/error-handling-in-com.md)
</dt> <dt>

[封裝錯誤](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[密碼編譯傳回值](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

