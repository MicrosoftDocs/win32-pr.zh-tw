---
description: 下列 Guid 支援 (CDM) 的內容解密模組。
title: 內容解密模組 (CDM) GUID
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984312"
---
# <a name="content-decryption-module-cdm-guids"></a>內容解密模組 (CDM) GUID

下列 Guid 支援 (CDM) 的內容解密模組。

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

用來從 [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) 執行取得介面的服務 GUID，例如 WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) 介面。 **IMFContentDecryptionModule** 的執行應該會執行 [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)並支援此服務 GUID。


## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>mfcontentdecryptionmodule。h</dt> </dl> |



## <a name="see-also"></a>另請參閱



- [媒體基礎常數](media-foundation-constants.md)
- [IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule
- [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




